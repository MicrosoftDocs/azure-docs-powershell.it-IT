---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507195"
---
# Set-AzsSubscription

## Sinossi
Creare o aggiornare un abbonamento.

## SINTASSI

### Set (impostazione predefinita)
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceId
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Creare o aggiornare un abbonamento.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

Creare o aggiornare un abbonamento.

## PARAMETRI

### -DisplayName
Nome dell'abbonamento.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Posbbily della quota di rete modificata restituita da Get-AzsNetworkQuota.

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Posizione
Posizione in cui la risorsa è posizione.

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Idofferta
Identificatore dell'offerta sotto l'ambito di un provider delegato.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Stato sottoscrizione.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Identificatore dell'abbonamento.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Elenco di coppie chiave-valore.

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID tenant
Identificatore del tenant della directory.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digitare
Tipo di risorsa.

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel

## Note

## COLLEGAMENTI CORRELATI

