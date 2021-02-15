---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183023"
---
# Get-AzStreamAnalyticsJob

## SYNOPSIS
Recupera informazioni sui processi di Analisi di flusso.

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

## DESCRIZIONE
Il cmdlet **Get-AzStreamAnalyticsJob** elenca tutti i processi di Analisi di flusso definiti nella sottoscrizione di Azure o nel gruppo di risorse specificato oppure ottiene informazioni su un processo specifico all'interno di un gruppo di risorse.

## ESEMPI

### ESEMPIO 1: Ottenere informazioni su tutti i processi di un abbonamento
```
PS C:\>Get-AzStreamAnalyticsJob
```

Questo comando restituisce informazioni su tutti i processi di Analisi di flusso nella sottoscrizione di Azure.

### ESEMPIO 2: Ottenere informazioni su tutti i processi in un gruppo di risorse
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Questo comando restituisce informazioni su tutti i processi di Analisi di flusso nel gruppo di risorse StreamAnalytics-Default-West-US.

### ESEMPIO 3: Ottenere informazioni su un processo specifico in un gruppo di risorse
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Questo comando restituisce informazioni sul processo StreamingJob del processo Analisi di flusso nel gruppo di risorse StreamAnalytics-Default-West-US.

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
Specifica il nome del processo di Analisi di flusso di Azure da recuperare.

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

### -NoExpand
Indica che il cmdlet recupererà il processo di Analisi di flusso di Azure, ma non restituirà informazioni su input, output e trasformazione.

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
Specifica il nome del gruppo di risorse a cui appartiene il processo di Analisi di flusso di Azure.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUT

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


