---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191039"
---
# Set-AzVmssRollingUpgradePolicy

## Sinossi
Imposta le proprietà dei criteri di aggiornamento a rotazione VMSS.

## SINTASSI

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Imposta le proprietà dei criteri di aggiornamento a rotazione VMSS.

## ESEMPI

### Esempio 1
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

Questo comando imposta 40% per MaxBatchInstance, 35% per MaxUnhealthyInstance, 30% per MaxUnhealthyUpgradedInstance e 30 secondi di pausa tra i batch per VMSS oggetto local $vmss.

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

### -MaxBatchInstancePercent
Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.
Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.
Se il valore non è specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.
Questo vincolo verrà controllato prima di iniziare qualsiasi batch.
Se il valore non è specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxUnhealthyUpgradedInstancePercent
La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.
Questo controllo avverrà dopo l'aggiornamento di ogni batch.
Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.
Se il valore non è specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.
La durata dell'ora deve essere specificata nel formato ISO 8601.
Il valore predefinito è 0 secondi (PT0S).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica l'oggetto VMSS.
Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. Int32

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Note

## COLLEGAMENTI CORRELATI
