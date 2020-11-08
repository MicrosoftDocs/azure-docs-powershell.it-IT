---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030447"
---
# Get-AzsUserSubscription

## Sinossi
Ottenere l'elenco degli abbonamenti agli utenti come amministratore.

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
Ottenere l'elenco degli abbonamenti agli utenti come amministratore.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsUserSubscription
```

Ottenere l'elenco degli abbonamenti agli utenti come amministratore.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription

## Note

## COLLEGAMENTI CORRELATI

