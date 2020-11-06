---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507831"
---
# Start-AzureRmStreamAnalyticsJob

## Sinossi
Avvia un processo di analisi del flusso.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureRmStreamAnalyticsJob** distribuisce in modo asincrono e avvia un processo di analisi del flusso in Azure.

## ESEMPI

### ESEMPIO 1: avviare un processo di analisi del flusso
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Questo comando avvia il processo StreamingJob e specifica che il flusso di eventi di output dovrebbe iniziare in timestamp 2014-07-03T01:00Z.

## PARAMETRI

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

### -Nome
Specifica il nome del processo di analisi di Azure Stream da avviare.

```yaml
Type: String
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

- JobStartTime: questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare quando il processo viene avviato.
- CustomTime-questo valore indica che il punto di partenza del flusso di eventi di output deve iniziare in corrispondenza di un'ora personalizzata specificata nel parametro *OutputStartTime* . 
 --LastOutputEventTime-questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare dall'ultimo tempo di output dell'evento.

Se la proprietà è assente, il valore predefinito è JobStartTime.

```yaml
Type: String
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
Questo valore è un indicatore di data e ora formattato ISO-8601 che indica il punto di partenza del flusso di eventi di output oppure $Null per indicare che il flusso di eventi di output verrà avviato ogni volta che si avvia il processo di flusso.
Questa proprietà deve avere un valore se *OutputStartMode* è impostato su CustomTime.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.

```yaml
Type: String
Parameter Sets: (All)
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

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### System. Object

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[New-AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Stop-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


