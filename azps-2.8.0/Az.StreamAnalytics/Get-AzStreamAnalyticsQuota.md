---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: dd36a1dcf5b23c26f0936b3adb0f692335c03c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855966"
---
# Get-AzStreamAnalyticsQuota

## Sinossi
Ottiene informazioni sulla quota di unità di flusso per un'area geografica.

## SINTASSI

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStreamAnalyticsQuota** ottiene le informazioni sulla quota di unità di flusso per un'area geografica.

## ESEMPI

### ESEMPIO 1: ottenere informazioni sulla quota di unità di flusso per un'area geografica
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

Questo comando restituisce informazioni sulla quota di unità di flusso e sull'utilizzo nell'area ovest degli Stati Uniti.

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

### -Posizione
Specifica il nome di un'area di Azure o di un centro dati per cui ottenere informazioni sulle quote delle unità di flusso.
Vedere https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services per un elenco delle aree di Azure supportate.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota

## Note

## COLLEGAMENTI CORRELATI

[Cmdlet di analisi di Azure Stream](./Az.StreamAnalytics.md)


