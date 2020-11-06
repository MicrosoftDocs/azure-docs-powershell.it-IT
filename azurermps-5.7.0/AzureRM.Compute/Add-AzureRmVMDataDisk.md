---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512728"
---
# <span data-ttu-id="32cb3-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="32cb3-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="32cb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="32cb3-103">Aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32cb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32cb3-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="32cb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="32cb3-106">Il cmdlet **Add-AzureRmVMDataDisk** aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="32cb3-107">È possibile aggiungere un disco di dati quando si crea una macchina virtuale oppure si può aggiungere un disco di dati a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="32cb3-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="32cb3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32cb3-108">EXAMPLES</span></span>

### <span data-ttu-id="32cb3-109">Esempio 1: aggiungere dischi di dati a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="32cb3-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="32cb3-110">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32cb3-111">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="32cb3-112">I tre comandi seguenti assegnano percorsi di tre dischi di dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="32cb3-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="32cb3-113">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="32cb3-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="32cb3-114">I tre comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="32cb3-115">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="32cb3-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="32cb3-116">L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="32cb3-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="32cb3-117">Esempio 2: aggiungere un disco di dati a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="32cb3-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="32cb3-118">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="32cb3-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="32cb3-119">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="32cb3-120">Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="32cb3-121">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="32cb3-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="32cb3-122">Esempio 3: aggiungere un disco di dati a una nuova macchina virtuale da un'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="32cb3-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="32cb3-123">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32cb3-124">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="32cb3-125">I due comandi successivi assegnano i percorsi per l'immagine dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="32cb3-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="32cb3-126">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="32cb3-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="32cb3-127">I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="32cb3-128">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="32cb3-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="32cb3-129">Esempio 4: aggiungere dischi di dati a una nuova macchina virtuale da un'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="32cb3-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="32cb3-130">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32cb3-131">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="32cb3-132">I comandi successivi assegnano i percorsi del disco dati alla variabile $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="32cb3-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="32cb3-133">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="32cb3-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="32cb3-134">Il comando finale consente di aggiungere un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32cb3-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="32cb3-135">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="32cb3-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="32cb3-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32cb3-136">PARAMETERS</span></span>

### <span data-ttu-id="32cb3-137">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="32cb3-137">-Caching</span></span>
<span data-ttu-id="32cb3-138">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="32cb3-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="32cb3-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32cb3-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32cb3-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="32cb3-140">ReadOnly</span></span>
- <span data-ttu-id="32cb3-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="32cb3-141">ReadWrite</span></span>
- <span data-ttu-id="32cb3-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="32cb3-142">None</span></span>

<span data-ttu-id="32cb3-143">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="32cb3-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="32cb3-144">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="32cb3-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="32cb3-145">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="32cb3-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="32cb3-146">-CreateOption</span></span>
<span data-ttu-id="32cb3-147">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="32cb3-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="32cb3-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32cb3-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32cb3-149">Allegare.</span><span class="sxs-lookup"><span data-stu-id="32cb3-149">Attach.</span></span>
<span data-ttu-id="32cb3-150">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="32cb3-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="32cb3-151">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="32cb3-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="32cb3-152">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="32cb3-153">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="32cb3-153">Empty.</span></span>
<span data-ttu-id="32cb3-154">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="32cb3-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="32cb3-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="32cb3-155">FromImage.</span></span>
<span data-ttu-id="32cb3-156">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="32cb3-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="32cb3-157">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="32cb3-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="32cb3-158">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="32cb3-159">-DiskSizeInGB</span></span>
<span data-ttu-id="32cb3-160">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-161">-Lun</span><span class="sxs-lookup"><span data-stu-id="32cb3-161">-Lun</span></span>
<span data-ttu-id="32cb3-162">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="32cb3-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-163">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="32cb3-163">-ManagedDiskId</span></span>
<span data-ttu-id="32cb3-164">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="32cb3-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="32cb3-165">-Name</span></span>
<span data-ttu-id="32cb3-166">Specifica il nome del disco di dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="32cb3-166">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-167">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="32cb3-167">-SourceImageUri</span></span>
<span data-ttu-id="32cb3-168">Specifica l'URI di origine del disco associato a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32cb3-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="32cb3-169">-StorageAccountType</span></span>
<span data-ttu-id="32cb3-170">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="32cb3-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="32cb3-171">-VhdUri</span></span>
<span data-ttu-id="32cb3-172">Specifica l'URI (Uniform Resource Identifier) per il file del disco rigido virtuale (VHD) da creare quando si usa un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="32cb3-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="32cb3-173">Questo cmdlet copia l'oggetto BLOB (Binary Large Object) dell'immagine in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="32cb3-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="32cb3-174">Questa è la posizione da cui avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-175">-VM</span><span class="sxs-lookup"><span data-stu-id="32cb3-175">-VM</span></span>
<span data-ttu-id="32cb3-176">Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="32cb3-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="32cb3-177">Puoi usare il cmdlet **Get-AzureRmVM** per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="32cb3-178">Puoi usare il cmdlet **New-AzureRmVMConfig** per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32cb3-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cb3-179">CommonParameters</span></span>
<span data-ttu-id="32cb3-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cb3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cb3-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32cb3-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cb3-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32cb3-182">INPUTS</span></span>

### <span data-ttu-id="32cb3-183">Nessuno</span><span class="sxs-lookup"><span data-stu-id="32cb3-183">None</span></span>
<span data-ttu-id="32cb3-184">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="32cb3-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32cb3-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32cb3-185">OUTPUTS</span></span>

## <span data-ttu-id="32cb3-186">Note</span><span class="sxs-lookup"><span data-stu-id="32cb3-186">NOTES</span></span>

## <span data-ttu-id="32cb3-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32cb3-187">RELATED LINKS</span></span>

[<span data-ttu-id="32cb3-188">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="32cb3-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="32cb3-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32cb3-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="32cb3-190">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="32cb3-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
