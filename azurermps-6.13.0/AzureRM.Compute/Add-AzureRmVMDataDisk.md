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
# <span data-ttu-id="53eab-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53eab-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="53eab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53eab-102">SYNOPSIS</span></span>
<span data-ttu-id="53eab-103">Aggiunge un disco di dati a una macchina virtuale o a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="53eab-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53eab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53eab-104">SYNTAX</span></span>

### <span data-ttu-id="53eab-105">VmNormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53eab-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53eab-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="53eab-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53eab-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="53eab-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53eab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53eab-108">DESCRIPTION</span></span>
<span data-ttu-id="53eab-109">Il cmdlet **Add-AzureRmVMDataDisk** aggiunge un disco di dati a una macchina virtuale o a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="53eab-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="53eab-110">È possibile aggiungere un disco di dati quando si crea una macchina virtuale oppure si può aggiungere un disco di dati a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="53eab-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="53eab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53eab-111">EXAMPLES</span></span>

### <span data-ttu-id="53eab-112">Esempio 1: aggiungere dischi di dati a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="53eab-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="53eab-113">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="53eab-114">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="53eab-115">I tre comandi seguenti assegnano percorsi di tre dischi di dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="53eab-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="53eab-116">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53eab-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="53eab-117">I tre comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="53eab-118">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="53eab-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="53eab-119">L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="53eab-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="53eab-120">Esempio 2: aggiungere un disco di dati a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="53eab-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="53eab-121">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="53eab-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="53eab-122">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="53eab-123">Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="53eab-124">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="53eab-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="53eab-125">Esempio 3: aggiungere un disco di dati a una nuova macchina virtuale da un'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="53eab-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="53eab-126">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="53eab-127">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="53eab-128">I due comandi successivi assegnano i percorsi per l'immagine dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="53eab-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="53eab-129">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53eab-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="53eab-130">I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="53eab-131">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="53eab-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="53eab-132">Esempio 4: aggiungere dischi di dati a una nuova macchina virtuale da un'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="53eab-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="53eab-133">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="53eab-134">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="53eab-135">I comandi successivi assegnano i percorsi del disco dati alla variabile $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="53eab-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="53eab-136">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53eab-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="53eab-137">Il comando finale consente di aggiungere un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="53eab-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="53eab-138">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="53eab-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="53eab-139">Esempio 5: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="53eab-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="53eab-140">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="53eab-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="53eab-141">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="53eab-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="53eab-142">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="53eab-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="53eab-143">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="53eab-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="53eab-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53eab-144">PARAMETERS</span></span>

### <span data-ttu-id="53eab-145">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="53eab-145">-Caching</span></span>
<span data-ttu-id="53eab-146">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="53eab-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="53eab-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="53eab-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53eab-148">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="53eab-148">ReadOnly</span></span>
- <span data-ttu-id="53eab-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53eab-149">ReadWrite</span></span>
- <span data-ttu-id="53eab-150">None il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="53eab-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="53eab-151">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="53eab-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="53eab-152">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="53eab-152">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="53eab-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="53eab-153">-CreateOption</span></span>
<span data-ttu-id="53eab-154">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="53eab-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="53eab-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="53eab-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53eab-156">Allegare.</span><span class="sxs-lookup"><span data-stu-id="53eab-156">Attach.</span></span>
<span data-ttu-id="53eab-157">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="53eab-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="53eab-158">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="53eab-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="53eab-159">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="53eab-160">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="53eab-160">Empty.</span></span>
<span data-ttu-id="53eab-161">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="53eab-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="53eab-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="53eab-162">FromImage.</span></span>
<span data-ttu-id="53eab-163">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="53eab-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="53eab-164">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="53eab-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="53eab-165">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="53eab-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eab-166">-DefaultProfile</span></span>
<span data-ttu-id="53eab-167">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53eab-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53eab-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="53eab-168">-DiskSizeInGB</span></span>
<span data-ttu-id="53eab-169">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="53eab-170">-Lun</span><span class="sxs-lookup"><span data-stu-id="53eab-170">-Lun</span></span>
<span data-ttu-id="53eab-171">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="53eab-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="53eab-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="53eab-172">-ManagedDiskId</span></span>
<span data-ttu-id="53eab-173">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="53eab-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="53eab-174">-Nome</span><span class="sxs-lookup"><span data-stu-id="53eab-174">-Name</span></span>
<span data-ttu-id="53eab-175">Specifica il nome del disco di dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="53eab-175">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="53eab-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="53eab-176">-SourceImageUri</span></span>
<span data-ttu-id="53eab-177">Specifica l'URI di origine del disco associato a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53eab-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="53eab-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="53eab-178">-StorageAccountType</span></span>
<span data-ttu-id="53eab-179">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="53eab-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="53eab-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="53eab-180">-VhdUri</span></span>
<span data-ttu-id="53eab-181">Specifica l'URI (Uniform Resource Identifier) per il file del disco rigido virtuale (VHD) da creare quando si usa un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="53eab-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="53eab-182">Questo cmdlet copia l'oggetto BLOB (Binary Large Object) dell'immagine in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="53eab-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="53eab-183">Questa è la posizione da cui avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-183">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="53eab-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="53eab-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="53eab-185">Specifica l'oggetto VM del set di scale della macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="53eab-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="53eab-186">Puoi usare il cmdlet **Get-AzureRmVmssVM** per ottenere un oggetto VM set della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="53eab-187">-VM</span><span class="sxs-lookup"><span data-stu-id="53eab-187">-VM</span></span>
<span data-ttu-id="53eab-188">Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="53eab-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="53eab-189">Puoi usare il cmdlet **Get-AzureRmVM** per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="53eab-190">Puoi usare il cmdlet **New-AzureRmVMConfig** per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53eab-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="53eab-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="53eab-191">-WriteAccelerator</span></span>
<span data-ttu-id="53eab-192">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="53eab-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="53eab-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eab-193">CommonParameters</span></span>
<span data-ttu-id="53eab-194">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eab-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eab-195">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53eab-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eab-196">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53eab-196">INPUTS</span></span>

### <span data-ttu-id="53eab-197">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="53eab-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="53eab-198">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="53eab-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="53eab-199">System. String</span><span class="sxs-lookup"><span data-stu-id="53eab-199">System.String</span></span>

### <span data-ttu-id="53eab-200">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="53eab-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="53eab-201">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="53eab-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="53eab-202">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53eab-202">OUTPUTS</span></span>

### <span data-ttu-id="53eab-203">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="53eab-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="53eab-204">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="53eab-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="53eab-205">Note</span><span class="sxs-lookup"><span data-stu-id="53eab-205">NOTES</span></span>

## <span data-ttu-id="53eab-206">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53eab-206">RELATED LINKS</span></span>

[<span data-ttu-id="53eab-207">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53eab-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="53eab-208">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="53eab-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="53eab-209">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="53eab-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
