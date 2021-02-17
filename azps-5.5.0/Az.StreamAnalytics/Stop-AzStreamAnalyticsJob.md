---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182911"
---
# Stop-AzStreamAnalyticsJob

## SYNOPSIS
Interrompe un processo di Analisi di flusso.

## SINTASSI

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Stop-AzStreamAnalyticsJob** interrompe in modo asincrono l'esecuzione di un processo di Analisi di flusso in Azure e deassegna le risorse che erano state usate.
La definizione e i metadati del processo rimangono disponibili all'interno dell'abbonamento sia tramite le API portale di Azure che di gestione, in modo che il processo possa essere modificato e riavviato.
Non verrà addebitato alcun processo in stato Di interruzione.

## ESEMPI

### Esempio 1: Interrompere un processo in esecuzione
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Questo comando interrompe il processo StreamingJob.

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
Specifica il nome del processo di Analisi di flusso di Azure da interrompere.

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

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)


