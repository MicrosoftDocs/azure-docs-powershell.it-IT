---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 4c00bfec7ab026478c4b05b55ce27b812af37486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957774"
---
# New-AzApplicationInsightsContinuousExport

## SYNOPSIS
Creare una nuova configurazione continua di Informazioni dettagliate sull'applicazione per una risorsa di Application Insights

## SINTASSI

### ComponentNameParameterSet (Impostazione predefinita)
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ComponentObjectParameterSet
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Creare una nuova configurazione continua di Informazioni dettagliate sull'applicazione per una risorsa di Application Insights

## ESEMPI

### Esempio 1: Creare una nuova configurazione di esportazione continua per una risorsa di Application Insights
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

Creare una nuova configurazione continua di informazioni sull'applicazione per esportare i tipi di documento "Richiesta" e "Traccia" per l'archiviazione che contengono "testcontainer" nell'account di archiviazione "teststorageaccount" nel gruppo di risorse "testgroup". Il token di firma di accesso condiviso deve essere valido e avere l'autorizzazione di scrittura per il contenitore, altrimenti la caratteristica di esportazione continua non funzionerà. Se il token di firma di accesso condiviso è scaduto, la caratteristica di esportazione continua smetterà di funzionare.

## PARAMETERS

### -ApplicationInsightsInsightsIn
Application Insights Component Object.

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -DocumentType
Tipi di documento che devono essere esportati.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome componente.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa componente Application Insights.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
ID account di archiviazione di destinazione.

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

### -StorageLocation
ID posizione di archiviazione di destinazione.

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

### -StorageSASUri
Uri della firma di accesso condiviso per l'archiviazione di destinazione.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights

### System.String

## OUTPUT

### Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration

## NOTE

## COLLEGAMENTI CORRELATI
