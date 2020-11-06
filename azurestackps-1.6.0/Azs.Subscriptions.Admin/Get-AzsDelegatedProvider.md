---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491569"
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
Identificatore DelegatedProvider.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription

## Note

## COLLEGAMENTI CORRELATI

