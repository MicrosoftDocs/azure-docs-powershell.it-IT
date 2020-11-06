---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506987"
---
# New-AddonPlanDefinitionObject

## Sinossi
Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.

## SINTASSI

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## Descrizione
Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

Creare un nuovo oggetto definizione piano per il piano specificato con il limite di acquisizione di 500.

## PARAMETRI

### -MaxAcquisitionCount
Numero massimo di istanze che possono essere acquisite da un singolo abbonamento.
Se non specificato, il valore assunto è 1.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanId
Identificatore piano.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

