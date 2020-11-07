---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676421"
---
# Get-AzStreamAnalyticsJob

## Sinossi
Ottiene le informazioni sui processi di analisi del flusso.

## SINTASSI

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStreamAnalyticsJob** elenca tutti i processi di analisi dello Stream definiti nell'abbonamento di Azure o nel gruppo di risorse specificato o ottiene informazioni sul lavoro su un processo specifico all'interno di un gruppo di risorse.

## ESEMPI

### ESEMPIO 1: ottenere informazioni su tutti i processi in una sottoscrizione
```
PS C:\>Get-AzStreamAnalyticsJob
```

Questo comando restituisce informazioni su tutti i processi di analisi del flusso nell'abbonamento a Azure.

### ESEMPIO 2: ottenere informazioni su tutti i processi in un gruppo di risorse
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Questo comando restituisce informazioni su tutti i processi di analisi del flusso nel gruppo di risorse StreamAnalytics-default-West-US.

### ESEMPIO 3: ottenere informazioni su un processo specifico in un gruppo di risorse
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Questo comando restituisce informazioni sul processo di analisi del flusso di lavoro di StreamingJob nel gruppo di risorse StreamAnalytics-default-West-US.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Nome
Specifica il nome del processo di analisi di Azure Stream da recuperare.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NOEXPAND
Indica che il cmdlet recupererà il processo di analisi di Azure Stream, ma non restituirà informazioni sugli input, gli output e la trasformazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. Management. Automation. SwitchParameter

## OUTPUT

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob

## Note

## COLLEGAMENTI CORRELATI

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


