---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: 8583227cee19a9429a7dfe4cd6bd8678e72d33ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973853"
---
# Get-AzStreamAnalyticsQuota

## SYNOPSIS
Ottiene informazioni sulla quota dell'unità di trasmissione per un'area geografica.

## SINTASSI

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzStreamAnalyticsQuota** ottiene informazioni sulla quota di unità di flusso per un'area geografica.

## ESEMPI

### ESEMPIO 1: Ottenere informazioni sulla quota dell'unità di trasmissione per un'area geografica
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

Questo comando restituisce informazioni sulla quota di unità di streaming e sull'utilizzo nell'area degli Stati Uniti occidentali.

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

### -Location
Specifica il nome di un'area geografica o di una posizione del data center di Azure per cui ottenere informazioni sulle quote delle unità di streaming.
Per http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services un elenco delle aree geografiche di Azure supportate, vedere.

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

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota

## NOTE

## COLLEGAMENTI CORRELATI

[Cmdlet di Analisi di flusso di Azure](./Az.StreamAnalytics.md)


