---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: d644f0bdb770ec1c6b26656cb7bf8709ee369a05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866577"
---
# <span data-ttu-id="1f503-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f503-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="1f503-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f503-102">SYNOPSIS</span></span>
<span data-ttu-id="1f503-103">Aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f503-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f503-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f503-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f503-105">DESCRIPTION</span></span>
<span data-ttu-id="1f503-106">Il cmdlet **Add-AzureRmVMDataDisk** aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="1f503-107">È possibile aggiungere un disco di dati quando si crea una macchina virtuale oppure si può aggiungere un disco di dati a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="1f503-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="1f503-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f503-108">EXAMPLES</span></span>

### <span data-ttu-id="1f503-109">Esempio 1: aggiungere dischi di dati a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="1f503-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="1f503-110">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1f503-111">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="1f503-112">I tre comandi seguenti assegnano percorsi di tre dischi di dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="1f503-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="1f503-113">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f503-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="1f503-114">I tre comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1f503-115">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="1f503-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="1f503-116">L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="1f503-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="1f503-117">Esempio 2: aggiungere un disco di dati a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="1f503-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="1f503-118">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="1f503-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="1f503-119">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="1f503-120">Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="1f503-121">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1f503-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="1f503-122">Esempio 3: aggiungere un disco di dati a una nuova macchina virtuale da un'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="1f503-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="1f503-123">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1f503-124">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="1f503-125">I due comandi successivi assegnano i percorsi per l'immagine dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="1f503-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="1f503-126">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f503-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="1f503-127">I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1f503-128">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="1f503-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="1f503-129">Esempio 4: aggiungere dischi di dati a una nuova macchina virtuale da un'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="1f503-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="1f503-130">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1f503-131">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="1f503-132">I comandi successivi assegnano i percorsi del disco dati alla variabile $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="1f503-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="1f503-133">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f503-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="1f503-134">Il comando finale consente di aggiungere un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1f503-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1f503-135">Il comando specifica il nome e il percorso per il disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="1f503-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="1f503-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f503-136">PARAMETERS</span></span>

### <span data-ttu-id="1f503-137">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="1f503-137">-Caching</span></span>
<span data-ttu-id="1f503-138">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="1f503-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="1f503-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f503-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f503-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f503-140">ReadOnly</span></span>
- <span data-ttu-id="1f503-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f503-141">ReadWrite</span></span>
- <span data-ttu-id="1f503-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f503-142">None</span></span>

<span data-ttu-id="1f503-143">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1f503-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="1f503-144">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="1f503-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="1f503-145">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="1f503-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="1f503-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1f503-146">-CreateOption</span></span>
<span data-ttu-id="1f503-147">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="1f503-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="1f503-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f503-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f503-149">Allegare.</span><span class="sxs-lookup"><span data-stu-id="1f503-149">Attach.</span></span>
<span data-ttu-id="1f503-150">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="1f503-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="1f503-151">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="1f503-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="1f503-152">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="1f503-153">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="1f503-153">Empty.</span></span>
<span data-ttu-id="1f503-154">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="1f503-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="1f503-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="1f503-155">FromImage.</span></span>
<span data-ttu-id="1f503-156">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="1f503-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="1f503-157">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="1f503-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="1f503-158">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="1f503-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f503-159">-DefaultProfile</span></span>
<span data-ttu-id="1f503-160">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f503-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f503-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1f503-161">-DiskSizeInGB</span></span>
<span data-ttu-id="1f503-162">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="1f503-163">-Lun</span><span class="sxs-lookup"><span data-stu-id="1f503-163">-Lun</span></span>
<span data-ttu-id="1f503-164">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="1f503-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="1f503-165">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="1f503-165">-ManagedDiskId</span></span>
<span data-ttu-id="1f503-166">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="1f503-166">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="1f503-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f503-167">-Name</span></span>
<span data-ttu-id="1f503-168">Specifica il nome del disco di dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1f503-168">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="1f503-169">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="1f503-169">-SourceImageUri</span></span>
<span data-ttu-id="1f503-170">Specifica l'URI di origine del disco associato a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f503-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="1f503-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1f503-171">-StorageAccountType</span></span>
<span data-ttu-id="1f503-172">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="1f503-172">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="1f503-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="1f503-173">-VhdUri</span></span>
<span data-ttu-id="1f503-174">Specifica l'URI (Uniform Resource Identifier) per il file del disco rigido virtuale (VHD) da creare quando si usa un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="1f503-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="1f503-175">Questo cmdlet copia l'oggetto BLOB (Binary Large Object) dell'immagine in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="1f503-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="1f503-176">Questa è la posizione da cui avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-176">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="1f503-177">-VM</span><span class="sxs-lookup"><span data-stu-id="1f503-177">-VM</span></span>
<span data-ttu-id="1f503-178">Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="1f503-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="1f503-179">Puoi usare il cmdlet **Get-AzureRmVM** per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-179">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="1f503-180">Puoi usare il cmdlet **New-AzureRmVMConfig** per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f503-180">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="1f503-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1f503-181">-WriteAccelerator</span></span>
<span data-ttu-id="1f503-182">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="1f503-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f503-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f503-183">CommonParameters</span></span>
<span data-ttu-id="1f503-184">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f503-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f503-185">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f503-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f503-186">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f503-186">INPUTS</span></span>

### <span data-ttu-id="1f503-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1f503-187">PSVirtualMachine</span></span>
<span data-ttu-id="1f503-188">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1f503-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="1f503-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f503-189">OUTPUTS</span></span>

### <span data-ttu-id="1f503-190">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1f503-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1f503-191">Note</span><span class="sxs-lookup"><span data-stu-id="1f503-191">NOTES</span></span>

## <span data-ttu-id="1f503-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f503-192">RELATED LINKS</span></span>

[<span data-ttu-id="1f503-193">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f503-193">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="1f503-194">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1f503-194">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="1f503-195">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="1f503-195">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
