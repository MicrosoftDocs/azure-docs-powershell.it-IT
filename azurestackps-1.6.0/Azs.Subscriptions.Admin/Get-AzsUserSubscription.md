---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491005"
---
# Get-AzsUserSubscription

## Sinossi
Ottenere l'elenco degli abbonamenti agli utenti come operator.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## Descrizione
Ottenere l'elenco degli abbonamenti agli utenti come operator.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsUserSubscription
```

Ottenere l'elenco degli abbonamenti agli utenti come operator.

## PARAMETRI

### -Filtro
Parametro di filtro OData.

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Parametro ID abbonamento.

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
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

