---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491294"
---
# Get-AzsOffer

## Sinossi
Ottenere l'elenco delle offerte pubbliche.

## SINTASSI

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## Descrizione
Ottenere l'elenco delle offerte pubbliche.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsOffer | fl
```

Ottenere l'elenco delle offerte pubbliche.

## PARAMETRI

### -Skip
Ignorare i primi elementi N specificati dal valore del parametro.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inizio pagina
Restituisce i primi N elementi come specificato dal valore del parametro.
Si applica dopo il parametro-Skip.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Subscription. Models. offer

## Note

## COLLEGAMENTI CORRELATI

