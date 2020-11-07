---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 510d0ee001e4c291dad3cc024f593d1f29c7ddca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860137"
---
# Get-UsageAggregates

## Sinossi
Ottiene i dettagli di utilizzo dell'abbonamento Azure segnalati.

## SINTASSI

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-UsageAggregates** ottiene i dati di utilizzo degli abbonamenti di Azure aggregati in base alle proprietà seguenti: 
- Orari di inizio e fine di quando è stato segnalato l'utilizzo.
- Precisione di aggregazione, giornaliera o oraria.
- Dettagli del livello di istanza per più istanze della stessa risorsa.
Per risultati coerenti, i dati restituiti si basano su quando i dettagli sull'utilizzo sono stati segnalati dalla risorsa Azure.
Per altre informazioni, vedi riferimenti alle API REST di Azure Billing https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) nella raccolta di Microsoft Developer Network Library).

## ESEMPI

### Esempio 1: recuperare i dati dell'abbonamento
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Questo comando recupera i dati di utilizzo segnalati per l'abbonamento tra 5/2/2015 e 5/5/2015.

## PARAMETRI

### -AggregationGranularity
Specifica la precisione di aggregazione dei dati.
I valori validi sono: ogni giorno e ogni ora.
Il valore predefinito è Daily.

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
Per un set di risultati di grandi dimensioni, le risposte vengono inpaginate usando i token di continuazione.
Il token di continuazione funge da segnalibro per lo stato di avanzamento.
Se non specifichi questo parametro, i dati vengono recuperati dall'inizio del giorno o dell'ora specificati in *ReportedStartTime*.
È consigliabile seguire il collegamento successivo nella pagina Response to anche se i dati.

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

### -ReportedEndTime
Specifica l'ora di fine segnalata per quando l'utilizzo delle risorse è stato registrato nel sistema di fatturazione di Azure.
Azure è un sistema distribuito che include più datacenter in tutto il mondo, quindi c'è un ritardo tra il momento in cui la risorsa è stata effettivamente consumata, ovvero il tempo di utilizzo delle risorse, e quando l'evento di utilizzo ha raggiunto il sistema di fatturazione, ovvero l'utilizzo delle risorse indicato nel tempo.
Per ottenere tutti gli eventi di utilizzo per un abbonamento segnalato per un periodo di tempo, è possibile eseguire una query in base al tempo segnalato.
Anche se si esegue una query in base al tempo segnalato, il cmdlet aggrega i dati di risposta in base al tempo di utilizzo delle risorse.
I dati sull'utilizzo delle risorse sono il perno utile per analizzare i dati.

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
Specifica l'ora di inizio riportata per quando l'utilizzo delle risorse è stato registrato nel sistema di fatturazione di Azure.

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

### -ShowDetails
Indica se questo cmdlet restituisce i dettagli a livello di istanza con i dati sull'utilizzo.
Il valore predefinito è $True.
Se $False, il servizio aggrega i risultati sul lato server e quindi restituisce meno gruppi aggregati.
Ad esempio, se stai usando tre siti Web, per impostazione predefinita otterrai tre voci per il consumo del sito Web.
Tuttavia, quando il valore è $False, tutti i dati per lo stesso **SubscriptionId** , **meterId** , **usageStartTime** e **usageEndTime** vengono compressi in una singola voce.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse

## Note

## COLLEGAMENTI CORRELATI