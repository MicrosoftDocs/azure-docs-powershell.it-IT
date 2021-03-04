---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969502"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Aggiunge un disco dati a vmss.

## SINTASSI

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzVmssVMDataDisk** aggiunge un disco dati a vmss.

## ESEMPI

### Esempio 1: Aggiungere un disco dati gestito a vmss.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Il primo comando ottiene un disco gestito esistente.
Il comando successivo ottiene una VM Vmss esistente specificata dal nome del gruppo di risorse, dal nome della macchina virtuale e dall'ID dell'istanza.
Il comando successivo aggiunge il disco gestito alla macchina virtuale Vmss archiviata localmente in $VmssVM.
Il comando finale aggiorna vmss con il disco dati aggiunto.

## PARAMETERS

### -Memorizzazione nella cache
Specifica la modalità di memorizzazione nella cache del disco.
I valori accettabili per questo parametro sono:
- ReadOnly
- ReadWrite
- Nessuno Il valore predefinito è ReadWrite.
Se si modifica questo valore, la macchina virtuale viene riavviata.
Questa impostazione influisce sulla coerenza e sulle prestazioni del disco.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o un'immagine utente, crea un disco vuoto o collega un disco esistente.
I valori accettabili per questo parametro sono:
- Allega.
Specificare questa opzione per creare una macchina virtuale da un disco specializzato.
Quando si specifica questa opzione, non specificare il *parametro SourceImageUri.*
Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da collegare come disco dati alla macchina virtuale.
- Vuoto.
Specificare questa opzione per creare un disco dati vuoto.
- FromImage.
Specificare questa opzione per creare una macchina virtuale da un'immagine o da un disco generalizzato.
Quando si specifica questa opzione, è necessario specificare anche il parametro *SourceImageUri* per indicare alla piattaforma azure la posizione del disco rigido virtuale da collegare come disco dati.
Il *parametro VhdUri* viene usato come posizione che identifica la posizione in cui verrà archiviato il disco dati VHD quando viene usato dalla macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -DiskEncryptionSetId
Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.  Può essere specificato solo per il disco gestito.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Specifica le dimensioni in gigabyte di un disco vuoto da collegare a una macchina virtuale.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Specifica il numero di unità logiche (LUN) di un disco dati.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Specifica l'ID di un disco gestito.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Specifica il tipo di account di archiviazione del disco gestito.

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

### -VirtualMachineScaleSetVM
Specifica l'oggetto VM del set di scalabilità della macchina virtuale locale a cui aggiungere un disco dati.
È possibile usare il cmdlet **Get-AzVmssVM** per ottenere un oggetto VM per il set di scalabilità delle macchine virtuali.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## OUTPUT

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTE

## COLLEGAMENTI CORRELATI
