---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: ce1183588458dc0213bff77493caf41a9b1d2766
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994641"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.

## SINTASSI

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzApiManagementRegion** aggiunge una nuova istanza del tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza fornita di **tipo Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Questo cmdlet non distribuisce da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di gestione delle API, passare l'istanza **di PsApiManagement** modificata a Set-AzApiManagement.

## ESEMPI

### Esempio 1: Aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Questo comando aggiunge due unità di SKU premium e l'area geografica Stati Uniti orientali **all'istanza PsApiManagement.**

### Esempio 2: Aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

Questo comando ottiene un **oggetto PsApiManagement,** aggiunge due unità di SKU premium per l'area geografica degli Stati Uniti orientali e quindi aggiorna la distribuzione.

## PARAMETERS

### -ApiManagement
Specifica **l'istanza PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.

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
Specifica la capacità di SKU dell'area di distribuzione.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione delle API.
Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi

```yaml
Type: System.String
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
- Sviluppatore
- Standard
- Premium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Specifica una configurazione di rete virtuale.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## OUTPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTE
* Il cmdlet scrive **l'istanza di PsApiManagement aggiornata** nella pipeline.

## COLLEGAMENTI CORRELATI

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)


