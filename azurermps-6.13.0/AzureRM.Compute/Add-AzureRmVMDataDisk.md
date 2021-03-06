---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519287"
---
# Add-AzureRmVMDataDisk

## Sinossi
Aggiunge un disco di dati a una macchina virtuale o a una VM vmss.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### VmNormalDiskParameterSetName (impostazione predefinita)
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### VmScaleSetVMParameterSetName
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmVMDataDisk** aggiunge un disco di dati a una macchina virtuale o a una VM vmss.
È possibile aggiungere un disco di dati quando si crea una macchina virtuale oppure si può aggiungere un disco di dati a una macchina virtuale esistente.

## ESEMPI

### Esempio 1: aggiungere dischi di dati a una nuova macchina virtuale
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.
I tre comandi seguenti assegnano percorsi di tre dischi di dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.
Questo approccio è solo per la leggibilità dei comandi seguenti.
I tre comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.
L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.

### Esempio 2: aggiungere un disco di dati a una macchina virtuale esistente
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .
Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.
Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.

### Esempio 3: aggiungere un disco di dati a una nuova macchina virtuale da un'immagine utente generalizzata
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.
I due comandi successivi assegnano i percorsi per l'immagine dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri rispettivamente.
Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.
I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.

### Esempio 4: aggiungere dischi di dati a una nuova macchina virtuale da un'immagine utente specializzata
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.
I comandi successivi assegnano i percorsi del disco dati alla variabile $DataDiskUri.
Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.
Il comando finale consente di aggiungere un disco dati alla macchina virtuale archiviata in $VirtualMachine.
Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.

### Esempio 5: aggiungere un disco di dati gestito a una VM vmss.
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Il primo comando ottiene un disco gestito esistente.
Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.
Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.
Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.

## PARAMETRI

### -Memorizzazione nella cache
Specifica la modalità di memorizzazione nella cache del disco.
I valori accettabili per questo parametro sono i seguenti:
- ReadOnly
- ReadWrite
- None il valore predefinito è ReadWrite.
La modifica di questo valore fa sì che la macchina virtuale venga riavviata.
Questa impostazione influenza la coerenza e le prestazioni del disco.

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
Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.
I valori accettabili per questo parametro sono i seguenti:
- Allegare.
Specificare questa opzione per creare una macchina virtuale da un disco specializzato.
Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .
Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.
- Vuoto.
Specificalo per creare un disco dati vuoto.
- FromImage.
Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.
Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.
Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.

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
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.

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
Specifica il numero di unità logica (LUN) per un disco di dati.

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

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome del disco di dati da aggiungere.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Specifica l'URI di origine del disco associato a questo cmdlet.

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
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Specifica l'URI (Uniform Resource Identifier) per il file del disco rigido virtuale (VHD) da creare quando si usa un'immagine della piattaforma o un'immagine utente.
Questo cmdlet copia l'oggetto BLOB (Binary Large Object) dell'immagine in questa posizione.
Questa è la posizione da cui avviare la macchina virtuale.

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

### -VirtualMachineScaleSetVM
Specifica l'oggetto VM del set di scale della macchina virtuale locale a cui aggiungere un disco di dati.
Puoi usare il cmdlet **Get-AzureRmVmssVM** per ottenere un oggetto VM set della scala della macchina virtuale.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco di dati.
Puoi usare il cmdlet **Get-AzureRmVM** per ottenere un oggetto macchina virtuale.
Puoi usare il cmdlet **New-AzureRmVMConfig** per creare un oggetto macchina virtuale.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
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
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

### System. String

### Microsoft. Azure. Management. Compute. Models. CachingTypes

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureRmVMDataDisk](./Remove-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
