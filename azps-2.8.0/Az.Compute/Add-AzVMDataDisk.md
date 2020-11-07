---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 79d8852fb3827e7856610d79ea7fb5f0a17543c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675478"
---
# <span data-ttu-id="7706b-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7706b-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="7706b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7706b-102">SYNOPSIS</span></span>
<span data-ttu-id="7706b-103">Aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="7706b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7706b-104">SYNTAX</span></span>

### <span data-ttu-id="7706b-105">VmNormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7706b-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7706b-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7706b-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7706b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7706b-107">DESCRIPTION</span></span>
<span data-ttu-id="7706b-108">Il cmdlet **Add-AzVMDataDisk** aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="7706b-109">È possibile aggiungere un disco di dati quando si crea una macchina virtuale oppure si può aggiungere un disco di dati a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="7706b-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="7706b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7706b-110">EXAMPLES</span></span>

### <span data-ttu-id="7706b-111">Esempio 1: aggiungere dischi di dati a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7706b-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="7706b-112">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7706b-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7706b-114">I tre comandi seguenti assegnano percorsi di tre dischi di dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="7706b-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="7706b-115">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7706b-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7706b-116">I tre comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7706b-117">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="7706b-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="7706b-118">L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="7706b-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="7706b-119">Esempio 2: aggiungere un disco di dati a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="7706b-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7706b-120">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="7706b-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="7706b-121">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7706b-122">Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7706b-123">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7706b-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="7706b-124">Esempio 3: aggiungere un disco di dati a una nuova macchina virtuale da un'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="7706b-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="7706b-125">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7706b-126">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7706b-127">I due comandi successivi assegnano i percorsi per l'immagine dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="7706b-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="7706b-128">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7706b-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="7706b-129">I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7706b-130">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="7706b-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="7706b-131">Esempio 4: aggiungere dischi di dati a una nuova macchina virtuale da un'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="7706b-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="7706b-132">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7706b-133">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7706b-134">I comandi successivi assegnano i percorsi del disco dati alla variabile $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="7706b-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="7706b-135">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7706b-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="7706b-136">Il comando finale consente di aggiungere un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7706b-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7706b-137">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="7706b-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="7706b-138">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7706b-138">PARAMETERS</span></span>

### <span data-ttu-id="7706b-139">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="7706b-139">-Caching</span></span>
<span data-ttu-id="7706b-140">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="7706b-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7706b-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7706b-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7706b-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7706b-142">ReadOnly</span></span>
- <span data-ttu-id="7706b-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7706b-143">ReadWrite</span></span>
- <span data-ttu-id="7706b-144">None il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7706b-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="7706b-145">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="7706b-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="7706b-146">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="7706b-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7706b-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7706b-147">-CreateOption</span></span>
<span data-ttu-id="7706b-148">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="7706b-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="7706b-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7706b-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7706b-150">Allegare.</span><span class="sxs-lookup"><span data-stu-id="7706b-150">Attach.</span></span>
<span data-ttu-id="7706b-151">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="7706b-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="7706b-152">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="7706b-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="7706b-153">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="7706b-154">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="7706b-154">Empty.</span></span>
<span data-ttu-id="7706b-155">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="7706b-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="7706b-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="7706b-156">FromImage.</span></span>
<span data-ttu-id="7706b-157">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="7706b-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="7706b-158">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="7706b-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="7706b-159">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="7706b-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7706b-160">-DefaultProfile</span></span>
<span data-ttu-id="7706b-161">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7706b-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7706b-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7706b-162">-DiskSizeInGB</span></span>
<span data-ttu-id="7706b-163">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-163">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="7706b-164">-Lun</span><span class="sxs-lookup"><span data-stu-id="7706b-164">-Lun</span></span>
<span data-ttu-id="7706b-165">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="7706b-165">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="7706b-166">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7706b-166">-ManagedDiskId</span></span>
<span data-ttu-id="7706b-167">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="7706b-167">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7706b-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="7706b-168">-Name</span></span>
<span data-ttu-id="7706b-169">Specifica il nome del disco di dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7706b-169">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="7706b-170">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="7706b-170">-SourceImageUri</span></span>
<span data-ttu-id="7706b-171">Specifica l'URI di origine del disco associato a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7706b-171">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="7706b-172">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7706b-172">-StorageAccountType</span></span>
<span data-ttu-id="7706b-173">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="7706b-173">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="7706b-174">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="7706b-174">-VhdUri</span></span>
<span data-ttu-id="7706b-175">Specifica l'URI (Uniform Resource Identifier) per il file del disco rigido virtuale (VHD) da creare quando si usa un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="7706b-175">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="7706b-176">Questo cmdlet copia l'oggetto BLOB (Binary Large Object) dell'immagine in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="7706b-176">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="7706b-177">Questa è la posizione da cui avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-177">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="7706b-178">-VM</span><span class="sxs-lookup"><span data-stu-id="7706b-178">-VM</span></span>
<span data-ttu-id="7706b-179">Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="7706b-179">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="7706b-180">Puoi usare il cmdlet **Get-AzVM** per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-180">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="7706b-181">Puoi usare il cmdlet **New-AzVMConfig** per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7706b-181">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="7706b-182">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7706b-182">-WriteAccelerator</span></span>
<span data-ttu-id="7706b-183">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="7706b-183">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="7706b-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7706b-184">CommonParameters</span></span>
<span data-ttu-id="7706b-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7706b-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7706b-186">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7706b-186">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7706b-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7706b-187">INPUTS</span></span>

### <span data-ttu-id="7706b-188">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7706b-188">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7706b-189">System. String</span><span class="sxs-lookup"><span data-stu-id="7706b-189">System.String</span></span>

### <span data-ttu-id="7706b-190">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="7706b-190">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="7706b-191">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7706b-191">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7706b-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7706b-192">OUTPUTS</span></span>

### <span data-ttu-id="7706b-193">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7706b-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7706b-194">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7706b-194">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7706b-195">Note</span><span class="sxs-lookup"><span data-stu-id="7706b-195">NOTES</span></span>

## <span data-ttu-id="7706b-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7706b-196">RELATED LINKS</span></span>

[<span data-ttu-id="7706b-197">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7706b-197">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="7706b-198">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7706b-198">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7706b-199">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7706b-199">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
