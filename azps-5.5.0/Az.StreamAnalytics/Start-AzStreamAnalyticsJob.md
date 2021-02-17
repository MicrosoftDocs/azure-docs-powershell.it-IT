---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182918"
---
# Start-AzStreamAnalyticsJob

## SYNOPSIS
Avvia un processo di Analisi di flusso.

## SINTASSI

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Start-AzStreamAnalyticsJob** distribuisce e avvia in modo asincrono un processo di Analisi di flusso in Azure.

## ESEMPI

### Esempio 1: Avviare un processo di Analisi di flusso
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Questo comando avvia il processo StreamingJob e specifica che il flusso dell'evento di output deve iniziare con timestamp 2014-07-03T01:00Z.

## PARAMETERS

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

### -Name
Specifica il nome del processo di Analisi di flusso di Azure da avviare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartMode
Specifica la modalità di avvio per il processo.
I valori validi sono: 
- JobStartTime: questo valore indica che il punto di partenza del flusso dell'evento di output deve iniziare all'avvio del processo.
- CustomTime: questo valore indica che il punto di partenza del flusso dell'evento di output deve iniziare in corrispondenza di un'ora personalizzata specificata nel *parametro OutputStartTime.* 
 - LastOutputEventTime: questo valore indica che il punto di partenza del flusso dell'evento di output deve iniziare dall'ora di output dell'ultimo evento.
Se la proprietà non è presente, l'impostazione predefinita è JobStartTime.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
Specifica l'ora di inizio dell'output.
Questo valore può essere un indicatore data e ora formattato ISO-8601 che indica il punto di inizio del flusso dell'evento di output oppure $Null per indicare che il flusso dell'evento di output verrà avviato ogni volta che viene avviato il processo di streaming.
Questa proprietà deve avere un valore se *OutputStartMode* è impostato su CustomTime.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene il processo di Analisi di flusso di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


