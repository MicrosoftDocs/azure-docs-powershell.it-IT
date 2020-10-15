---
title: Gestire le risorse di Azure con Invoke-AzRestMethod
description: Come usare Azure PowerShell per gestire le risorse con il cmdlet Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001925"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="6e8ea-103">Gestire le risorse di Azure con Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="6e8ea-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="6e8ea-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) è un cmdlet di Azure PowerShell introdotto nella versione 4.4.0 del modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="6e8ea-105">Consente di creare richieste HTTP personalizzate per l'endpoint ARM (Azure Resource Management) usando il contesto Az.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="6e8ea-106">Questo cmdlet è utile quando si vuole gestire i servizi di Azure per le funzionalità non ancora disponibili nel modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="6e8ea-107">Come usare Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="6e8ea-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="6e8ea-108">Ad esempio, è possibile consentire l'accesso a Registro Azure Container (ACR) solo per reti specifiche o per negare l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="6e8ea-109">A partire dalla versione 4.5.0 del modulo Az PowerShell, questa funzionalità non è ancora disponibile nel [modulo PowerShell Az.ContainerRegistry](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="6e8ea-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="6e8ea-110">Tuttavia, può essere gestita provvisoriamente con `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="6e8ea-111">Uso di Invoke-AzRestMethod con operazioni GET</span><span class="sxs-lookup"><span data-stu-id="6e8ea-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="6e8ea-112">L'esempio seguente illustra come usare il cmdlet `Invoke-AzRestMethod` con un'operazione GET:</span><span class="sxs-lookup"><span data-stu-id="6e8ea-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

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

<span data-ttu-id="6e8ea-113">Per garantire la massima flessibilità, quasi tutti i parametri di `Invoke-AzRestMethod` sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="6e8ea-114">Tuttavia, quando si gestiscono le risorse incluse in un gruppo, è molto probabile che sia necessario specificare l'ID completo delle risorse o parametri come il gruppo di risorse, il provider di risorse e il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="6e8ea-115">I parametri `ResourceType` e `Name` possono assumere più valori se sono destinati a risorse per le quali è necessario specificare più nomi.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="6e8ea-116">Ad esempio, per modificare una ricerca salvata in un'area di lavoro Log Analytics, i parametri sono simili all'esempio seguente: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="6e8ea-117">Usando un mapping basato sulla posizione nella matrice, il cmdlet crea la risorsa seguente: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="6e8ea-118">Il parametro `APIVersion` consente di usare una versione API specifica, incluse quelle di anteprima.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="6e8ea-119">Le versioni API supportate per i provider di risorse di Azure sono disponibili nel repository GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="6e8ea-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="6e8ea-120">È possibile trovare la definizione della versione 2019-12-01-preview di Registro Azure Container nel percorso seguente: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="6e8ea-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="6e8ea-121">Uso di Invoke-AzRestMethod con operazioni PATCH</span><span class="sxs-lookup"><span data-stu-id="6e8ea-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="6e8ea-122">Con il cmdlet `Invoke-AzRestMethod` è possibile disabilitare l'accesso pubblico all'istanza di Registro Azure Container esistente denominata `myacr` nel gruppo di risorse `myresourcegroup`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="6e8ea-123">Per disabilitare l'accesso alla rete pubblica, è necessario eseguire una chiamata **PATCH** all'API che modifichi il valore del parametro `publicNetwokAccess` come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6e8ea-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

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

<span data-ttu-id="6e8ea-124">La proprietà `Payload` è una stringa JSON che mostra il percorso della proprietà da modificare.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="6e8ea-125">Tutti i parametri dell'API sono descritti nel file **rest-api-spec** associato a questa API.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="6e8ea-126">La definizione specifica del parametro publicNetworkAccess si trova nel [file JSON del registro contenitori](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) per la versione di anteprima 2019-12-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="6e8ea-127">Per consentire l'accesso al Registro di sistema solo da uno specifico indirizzo IP, il payload deve essere modificato come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6e8ea-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="6e8ea-128">Confronto con Get-AzResource, New-AzResource e Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6e8ea-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="6e8ea-129">I cmdlet `*-AzResource` consentono di personalizzare la chiamata API REST ad Azure specificando il tipo di risorsa, la versione dell'API e le proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="6e8ea-130">È però prima necessario creare le proprietà come `PSObject`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="6e8ea-131">Questo processo aggiunge un ulteriore livello di complessità e può facilmente diventare complicato.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="6e8ea-132">`Invoke-AzRestMethod` costituisce una soluzione semplice per gestire le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="6e8ea-133">Come illustrato nell'esempio precedente, è possibile creare una stringa JSON e usarla per personalizzare la chiamata all'API REST senza dover creare preventivamente `PSObjects`.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="6e8ea-134">Se si ha già familiarità con i cmdlet `*-AzResource`, è possibile continuare a usarli.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="6e8ea-135">Non è previsto alcun piano di interruzione del supporto.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="6e8ea-136">Con `Invoke-AzRestMethod` è stato aggiunto un nuovo cmdlet al toolkit.</span><span class="sxs-lookup"><span data-stu-id="6e8ea-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e8ea-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6e8ea-137">See Also</span></span>

* [<span data-ttu-id="6e8ea-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6e8ea-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="6e8ea-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="6e8ea-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="6e8ea-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6e8ea-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
