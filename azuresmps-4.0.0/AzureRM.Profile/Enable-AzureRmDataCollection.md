---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491177"
---
# Enable-AzureRmDataCollection

## Sinossi
Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di AzurePowerShell.
L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente.
Non vengono raccolti dati a meno che non si opti esplicitamente.

## SINTASSI

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.
In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.
Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.

Eseguire il cmdlet Enable-AzureRMDataCollection per abilitare la raccolta dati per l'utente corrente nel computer corrente.
In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.

Per disabilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Disable-AzureRmDataCollection.

## ESEMPI

### Esempio 1: abilitazione della raccolta dati per l'utente corrente
```
PS C:\> Enable-AzureRmDataCollection
```

Questo esempio Mostra come abilitare la raccolta dati per l'utente corrente.

## PARAMETRI

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Nessuno

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureRmDataCollection]()

