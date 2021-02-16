---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199367"
---
# Add-AzVMDataDisk

## SYNOPSIS
Aggiunge un disco dati a una macchina virtuale.

## SINTASSI

### VmNormalDiskParameterSetName (impostazione predefinita)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzVMDataDisk** aggiunge un disco dati a una macchina virtuale.
È possibile aggiungere un disco dati quando si crea una macchina virtuale oppure aggiungere un disco dati a una macchina virtuale esistente.

## ESEMPI

### Esempio 1: Aggiungere dischi dati a una nuova macchina virtuale
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Il primo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
I tre comandi seguenti assegnano i percorsi di tre dischi dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.
Questo approccio è solo per la leggibilità dei comandi seguenti.
I tre comandi finali aggiungono ognuno un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e la posizione del disco e altre proprietà del disco.
L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.

### Esempio 2: Aggiungere un disco dati a una macchina virtuale esistente
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Il primo comando recupera la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzVM.](./Get-AzVM.md)
Il comando archivia la macchina virtuale nella $VirtualMachine variabile.
Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.

### Esempio 3: Aggiungere un disco dati a una nuova macchina virtuale da un'immagine utente generalizzata
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
I due comandi seguenti assegnano i percorsi per l'immagine dei dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri variabili.
Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.
I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e la posizione del disco e altre proprietà del disco.

### Esempio 4: Aggiungere dischi dati a una nuova macchina virtuale da un'immagine utente specializzata
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
I comandi seguenti assegnano i percorsi del disco dati alla $DataDiskUri variabile.
Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.
Il comando finale aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e la posizione del disco e altre proprietà del disco.

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
Position: 3
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
Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.
Quando si specifica questa opzione, è necessario specificare anche il parametro *SourceImageUri* per indicare alla piattaforma Azure la posizione del disco rigido da collegare come disco dati.
Il *parametro VhdUri* viene usato come posizione che identifica dove verrà archiviato il disco dati VHD quando viene usato dalla macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
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
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Specifica il numero di unità logiche (LUN) di un disco dati.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Specifica l'ID di un disco gestito.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome del disco dati da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Specifica l'URI di origine del disco allegato dal cmdlet.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Specifica il tipo di account di archiviazione del disco gestito.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Specifica l'URI (Uniform Resource Identifier) del file del disco rigido virtuale da creare quando si usa l'immagine di una piattaforma o un'immagine utente.
Questo cmdlet copia l'oggetto binario binario di grandi dimensioni (BLOB) dell'immagine in questa posizione.
Si tratta della posizione da cui avviare la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco dati.
È possibile usare il cmdlet **Get-AzVM** per ottenere un oggetto macchina virtuale.
È possibile usare il cmdlet **New-AzVMConfig** per creare un oggetto macchina virtuale.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
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

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTE

## COLLEGAMENTI CORRELATI

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AZVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
