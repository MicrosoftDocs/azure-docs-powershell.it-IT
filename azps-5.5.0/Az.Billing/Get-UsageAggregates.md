---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200942"
---
# Get-UsageAggregates

## SYNOPSIS
Recupera i dettagli di utilizzo della sottoscrizione di Azure riportati.

## SINTASSI

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-UsageAggregates** ottiene i dati di utilizzo aggregati della sottoscrizione di Azure in base alle proprietà seguenti: 
- Ora di inizio e di fine della registrazione dell'utilizzo.
- Precisione dell'aggregazione, giornaliera o oraria.
- Dettagli del livello di istanza per più istanze della stessa risorsa.
Per ottenere risultati coerenti, i dati restituiti si basano sulla data in cui la risorsa Azure ha riportato i dettagli sull'utilizzo.
Per altre informazioni, vedere il riferimento all'API REST per la fatturazione di Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( nella libreria Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network.

## ESEMPI

### Esempio 1: Recuperare i dati dell'abbonamento
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Questo comando recupera i dati di utilizzo segnalati per l'abbonamento tra il 2/5/2015 e il 5/5/2015.

## PARAMETERS

### -AggregationGranularity
Specifica la precisione di aggregazione dei dati.
I valori validi sono: Ogni giorno e Ogni ora.
Il valore predefinito è Giornaliero.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Specifica il token di continuazione recuperato dal corpo della risposta nella chiamata precedente.
Per un set di risultati di grandi dimensioni, le risposte vengono paginate usando token di continuazione.
Il token di continuazione funge da segnalibro per lo stato di avanzamento.
Se non si specifica questo parametro, i dati vengono recuperati dall'inizio del giorno o dell'ora specificata in *ReportedStartTime.*
È consigliabile seguire il collegamento successivo nella risposta alla pagina, anche se i dati sono.

```yaml
Type: System.String
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

### -ReportedEndTime
Specifica l'ora di fine segnalata per la registrazione dell'utilizzo delle risorse nel sistema di fatturazione di Azure.
Azure è un sistema distribuito che si estende su più data center in tutto il mondo, quindi c'è un ritardo tra il momento in cui la risorsa è stata effettivamente consumata, ovvero il tempo di utilizzo delle risorse e il momento in cui l'evento di utilizzo ha raggiunto il sistema di fatturazione, ovvero il tempo di utilizzo delle risorse segnalato.
Per ottenere tutti gli eventi di utilizzo per una sottoscrizione riportati per un periodo di tempo, eseguire una query in base al tempo segnalato.
Anche se si esegue una query in base al tempo segnalato, il cmdlet aggrega i dati delle risposte in base al tempo di utilizzo delle risorse.
I dati sull'utilizzo delle risorse sono il pivot utile per l'analisi dei dati.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Specifica l'ora di inizio segnalata per la registrazione dell'utilizzo delle risorse nel sistema di fatturazione di Azure.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mostra dettagli
Indica se questo cmdlet restituisce dettagli a livello di istanza con i dati di utilizzo.
Il valore predefinito è $True.
Se $False, il servizio aggrega i risultati sul lato server, quindi restituisce meno gruppi di aggregazione.
Ad esempio, se si eseguono tre siti Web, per impostazione predefinita vengono visualizzati tre elementi per l'utilizzo dei siti Web.
Tuttavia, quando il valore è $False, tutti i dati per lo stesso **subscriptionId,** **meterId,** **usageStartTime** e **usageEndTime** vengono compressi in una singola voce.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## NOTE

## COLLEGAMENTI CORRELATI
