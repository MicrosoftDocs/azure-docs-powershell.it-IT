---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030552"
---
# Get-AzsDelegatedProvider

## Sinossi
Ottenere l'elenco di delegatedProviders.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Ottieni
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## Descrizione
Ottenere l'elenco di delegatedProviders.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsDelegatedProvider
```

Ottenere un elenco di provider delegati.

### --------------------------ESEMPIO 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Ottenere un provider delegato specifico.

## PARAMETRI

### -DelegatedProviderId
{{Fill DelegatedProviderId Description}}

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription

## Note

## COLLEGAMENTI CORRELATI

