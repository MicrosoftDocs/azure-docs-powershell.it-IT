---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: e78a361bfb332bc2a8bcb226fae946a3abc0a05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676229"
---
# Disable-AzDataCollection

## Sinossi
Opta per la raccolta di dati per migliorare i cmdlet di AzurePowerShell. I dati non vengono raccolti a meno che non si opti esplicitamente.

## SINTASSI

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.
In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.
Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.
Eseguire il cmdlet Disable-AzDataCollection per disabilitare la raccolta dati per l'utente corrente.
In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.
Per abilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Enable-AzDataCollection.

## ESEMPI

### Esempio 1: disabilitazione della raccolta dati per l'utente corrente
```
PS C:\> Disable-AzDataCollection
```

Questo esempio Mostra come disabilitare la raccolta dati per l'utente corrente. 

## PARAMETRI

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### Nessuno

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI

[Enable-AzDataCollection](./Enable-AzDataCollection.md)

