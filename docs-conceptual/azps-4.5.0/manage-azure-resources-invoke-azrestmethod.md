---
title: Gestire le risorse di Azure con Invoke-AzRestMethod
description: Come usare Azure PowerShell per gestire le risorse con il cmdlet Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: 380fd818a3af2474ce192c7a1da8a6798795cf21
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/18/2020
ms.locfileid: "88512990"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Gestire le risorse di Azure con Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) è un cmdlet di Azure PowerShell introdotto nella versione 4.4.0 del modulo Az PowerShell. Consente di creare richieste HTTP personalizzate per l'endpoint ARM (Azure Resource Management) usando il contesto Az.

Questo cmdlet è utile quando si vuole gestire i servizi di Azure per le funzionalità non ancora disponibili nel modulo Az PowerShell.

## <a name="how-to-use-invoke-azrestmethod"></a>Come usare Invoke-AzRestMethod

Ad esempio, è possibile consentire l'accesso a Registro Azure Container (ACR) solo per reti specifiche o per negare l'accesso pubblico. Questa funzionalità non è ancora disponibile nel [modulo PowerShell Az.ContainerRegistry](/powershell/module/Az.ContainerRegistry/).
Tuttavia, può essere gestita provvisoriamente con `Invoke-AzRestMethod`.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Uso di Invoke-AzRestMethod con operazioni GET

L'esempio seguente illustra come usare il cmdlet `Invoke-AzRestMethod` con un'operazione GET:

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

Per garantire la massima flessibilità, quasi tutti i parametri di `Invoke-AzRestMethod` sono facoltativi.
Tuttavia, quando si gestiscono le risorse incluse in un gruppo, è molto probabile che sia necessario specificare l'ID completo delle risorse o parametri come il gruppo di risorse, il provider di risorse e il tipo di risorsa.

I parametri `ResourceType` e `Name` possono assumere più valori se sono destinati a risorse per le quali è necessario specificare più nomi. Ad esempio, per modificare una ricerca salvata in un'area di lavoro Log Analytics, i parametri sono simili all'esempio seguente: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Usando un mapping basato sulla posizione nella matrice, il cmdlet crea la risorsa seguente: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Il parametro `APIVersion` consente di usare una versione API specifica, incluse quelle di anteprima. Le versioni API supportate per i provider di risorse di Azure sono disponibili nel repository GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

È possibile trovare la definizione della versione 2019-12-01-preview di Registro Azure Container nel percorso seguente: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Uso di Invoke-AzRestMethod con operazioni PATCH

Con il cmdlet Invoke-AzRestMethod è possibile disabilitare l'accesso pubblico all'istanza di Registro Azure Container esistente denominata `myacr` nel gruppo di risorse `myresourcegroup`.

Per disabilitare l'accesso alla rete pubblica, è necessario eseguire una chiamata **PATCH** all'API che modifichi il valore del parametro `publicNetwokAccess` come illustrato nell'esempio seguente:

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

La proprietà `Payload` è una stringa JSON che mostra il percorso della proprietà da modificare.

Tutti i parametri dell'API sono descritti nel file **rest-api-spec** associato a questa API.
La definizione specifica del parametro publicNetworkAccess si trova nel [file JSON del registro contenitori](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) per la versione di anteprima 2019-12-01 dell'API.

Per consentire l'accesso al Registro di sistema solo da uno specifico indirizzo IP, il payload deve essere modificato come illustrato nell'esempio seguente:

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Confronto con Get-AzResource, New-AzResource e Remove-AzResource

I cmdlet `*-AzResource` consentono di personalizzare la chiamata API REST ad Azure specificando il tipo di risorsa, la versione dell'API e le proprietà da aggiornare. Tuttavia, le proprietà devono essere un elemento `PSObject` che può risultare difficile da creare.

`Invoke-AzRestMethod` offre un modo più semplice per gestire le risorse di Azure. Nell'esempio precedente è possibile vedere che il payload è una stringa JSON. Non è necessario eseguire la conversione da JSON a `PSObjects`.

Se si ha già familiarità con i cmdlet `*-AzResource`, è possibile continuare a usarli. Non è previsto alcun piano di interruzione del supporto. Con `Invoke-AzRestMethod` è stato aggiunto al gruppo un nuovo cmdlet.

## <a name="see-also"></a>Vedere anche

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)