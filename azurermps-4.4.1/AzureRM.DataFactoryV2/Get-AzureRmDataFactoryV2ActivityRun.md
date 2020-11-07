---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2000e489dcb5a0bab384ac0aad8a1ffbe53aba15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688334"
---
# Get-AzureRmDataFactoryV2ActivityRun

## Sinossi
Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByFactoryName (impostazione predefinita)
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-DataFactory] <PSDataFactory>
```


## Descrizione

Il cmdlet **Get-AzureRmDataFactoryV2ActivityRun** ottiene le informazioni sulle esecuzioni in Azure Data Factory per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato. È inoltre possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.

## ESEMPI

### Esempio 1: ottenere tutte le attività eseguite per un'esecuzione della pipeline
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}

```

Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nell'esecuzione della pipeline con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".

## PARAMETRI

### -ActivityName
Nome dell'attività.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Oggetto Data Factory.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Datafactoryname
Nome della factory di dati.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LinkedServiceName
Nome del servizio collegato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PipelineRunId
ID esecuzione della pipeline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunStartedAfter
Il periodo di tempo in cui viene avviata l'esecuzione della pipeline.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunStartedBefore
L'ora in cui è stata avviata l'esecuzione della pipeline.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stato
Lo stato dell'esecuzione della pipeline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INGRESSI

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
System. String


## OUTPUT

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun


## Note

## COLLEGAMENTI CORRELATI
[Invoke-AzureRmDataFactoryV2Pipeline]()

[Get-AzureRmDataFactoryV2PipelineRun]()

