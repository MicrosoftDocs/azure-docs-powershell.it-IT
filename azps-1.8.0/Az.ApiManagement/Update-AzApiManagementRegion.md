---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400706"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Aggiorna l'area di distribuzione esistente nell'istanza di PsApiManagement.

## SINTASSI

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Update-AzApiManagementRegion** aggiorna un'istanza esistente di tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in una raccolta di oggetti **AdditionalRegions** di un'istanza fornita di tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Questo cmdlet non distribuisce altro che aggiorna un'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di Gestione API, usare **PsApiManagementInstance modificata** al cmdlet Set-AzApiManagement.

## ESEMPI

### Esempio 1: Aumentare la capacità di Altre aree in un'istanza di PsApiManagement
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Questo comando ottiene il servizio SKU API Management Premium, con aree geografiche degli Stati Uniti centro meridionali e del Nord. Aumenta quindi la capacità dell'area nord centrale degli Stati Uniti a 2 usando **Update-AzApiManagementRegion.** Il cmdlet successivo Set-AzApiManagement applica la modifica di configurazione al servizio di gestione api.

## PARAMETERS

### -ApiManagement
Specifica **all'istanza PsApiManagement** di aggiornare un'area di distribuzione esistente.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Capacità
Specifica il nuovo valore di capacità di SKU per l'area di distribuzione.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifica la posizione dell'area di distribuzione da aggiornare.
Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione api.
Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica il nuovo valore di livello per l'area geografica di distribuzione.
I valori validi sono:
- Sviluppatore
- Standard
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Specifica una configurazione di rete virtuale per l'area geografica di distribuzione.
Il passaggio $null rimuove la configurazione di rete virtuale per l'area geografica.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku

### System.Int32

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## OUTPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)
