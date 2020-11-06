---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521940"
---
# Add-AzureRmApiManagementRegion

## Sinossi
Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmApiManagementRegion** aggiunge una nuova istanza di tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Questo cmdlet non distribuisce nulla da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di una gestione API, passare l'istanza di **PsApiManagement** modificata a Update-AzureRmApiManagementDeployment.

## ESEMPI

### Esempio 1: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Questo comando aggiunge due unità SKU Premium e l'area denominata East US all'istanza di **PsApiManagement** .

### Esempio 2: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

Questo comando ottiene un oggetto **PsApiManagement** , aggiunge due unità SKU Premium per l'area denominata East US e quindi aggiorna la distribuzione.

## PARAMETRI

### -ApiManagement
Specifica l'istanza di **PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Capacità
Specifica la capacità SKU dell'area di distribuzione.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.

Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Specifica il livello dell'area di distribuzione.
I valori validi sono: 

- Sviluppo
- Standard
- Premium

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Specifica una configurazione di rete virtuale.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PsApiManagement
Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Note
* Il cmdlet scrive l'istanza di **PsApiManagement** aggiornata in pipeline.

## COLLEGAMENTI CORRELATI

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)


