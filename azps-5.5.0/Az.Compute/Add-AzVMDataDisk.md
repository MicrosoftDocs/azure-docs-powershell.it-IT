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
# <span data-ttu-id="6620b-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6620b-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="6620b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6620b-102">SYNOPSIS</span></span>
<span data-ttu-id="6620b-103">Aggiunge un disco dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="6620b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6620b-104">SYNTAX</span></span>

### <span data-ttu-id="6620b-105">VmNormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6620b-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6620b-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6620b-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6620b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6620b-107">DESCRIPTION</span></span>
<span data-ttu-id="6620b-108">Il cmdlet **Add-AzVMDataDisk** aggiunge un disco dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="6620b-109">È possibile aggiungere un disco dati quando si crea una macchina virtuale oppure aggiungere un disco dati a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="6620b-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="6620b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6620b-110">EXAMPLES</span></span>

### <span data-ttu-id="6620b-111">Esempio 1: Aggiungere dischi dati a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6620b-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="6620b-112">Il primo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="6620b-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6620b-113">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6620b-114">I tre comandi seguenti assegnano i percorsi di tre dischi dati alle variabili $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="6620b-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="6620b-115">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6620b-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="6620b-116">I tre comandi finali aggiungono ognuno un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6620b-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6620b-117">Il comando specifica il nome e la posizione del disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="6620b-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="6620b-118">L'URI di ogni disco è archiviato in $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="6620b-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="6620b-119">Esempio 2: Aggiungere un disco dati a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="6620b-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6620b-120">Il primo comando recupera la macchina virtuale denominata VirtualMachine07 usando il cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="6620b-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="6620b-121">Il comando archivia la macchina virtuale nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="6620b-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6620b-122">Il secondo comando aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6620b-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6620b-123">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6620b-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="6620b-124">Esempio 3: Aggiungere un disco dati a una nuova macchina virtuale da un'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="6620b-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="6620b-125">Il primo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="6620b-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6620b-126">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6620b-127">I due comandi seguenti assegnano i percorsi per l'immagine dei dati e i dischi di dati alle variabili $DataImageUri e $DataDiskUri variabili.</span><span class="sxs-lookup"><span data-stu-id="6620b-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="6620b-128">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6620b-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="6620b-129">I comandi finali aggiungono un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6620b-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6620b-130">Il comando specifica il nome e la posizione del disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="6620b-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="6620b-131">Esempio 4: Aggiungere dischi dati a una nuova macchina virtuale da un'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="6620b-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="6620b-132">Il primo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="6620b-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6620b-133">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6620b-134">I comandi seguenti assegnano i percorsi del disco dati alla $DataDiskUri variabile.</span><span class="sxs-lookup"><span data-stu-id="6620b-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="6620b-135">Questo approccio viene usato per migliorare la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6620b-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="6620b-136">Il comando finale aggiunge un disco dati alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6620b-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6620b-137">Il comando specifica il nome e la posizione del disco e altre proprietà del disco.</span><span class="sxs-lookup"><span data-stu-id="6620b-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="6620b-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6620b-138">PARAMETERS</span></span>

### <span data-ttu-id="6620b-139">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="6620b-139">-Caching</span></span>
<span data-ttu-id="6620b-140">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="6620b-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="6620b-141">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="6620b-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6620b-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6620b-142">ReadOnly</span></span>
- <span data-ttu-id="6620b-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6620b-143">ReadWrite</span></span>
- <span data-ttu-id="6620b-144">Nessuno Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="6620b-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="6620b-145">Se si modifica questo valore, la macchina virtuale viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="6620b-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="6620b-146">Questa impostazione influisce sulla coerenza e sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="6620b-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="6620b-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6620b-147">-CreateOption</span></span>
<span data-ttu-id="6620b-148">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o un'immagine utente, crea un disco vuoto o collega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="6620b-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="6620b-149">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="6620b-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6620b-150">Allega.</span><span class="sxs-lookup"><span data-stu-id="6620b-150">Attach.</span></span>
<span data-ttu-id="6620b-151">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="6620b-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="6620b-152">Quando si specifica questa opzione, non specificare il *parametro SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="6620b-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="6620b-153">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da collegare come disco dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="6620b-154">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="6620b-154">Empty.</span></span>
<span data-ttu-id="6620b-155">Specificare questa opzione per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="6620b-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="6620b-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="6620b-156">FromImage.</span></span>
<span data-ttu-id="6620b-157">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="6620b-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="6620b-158">Quando si specifica questa opzione, è necessario specificare anche il parametro *SourceImageUri* per indicare alla piattaforma Azure la posizione del disco rigido da collegare come disco dati.</span><span class="sxs-lookup"><span data-stu-id="6620b-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="6620b-159">Il *parametro VhdUri* viene usato come posizione che identifica dove verrà archiviato il disco dati VHD quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="6620b-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6620b-160">-DefaultProfile</span></span>
<span data-ttu-id="6620b-161">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6620b-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6620b-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6620b-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6620b-163">Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="6620b-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="6620b-164">Può essere specificato solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="6620b-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="6620b-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6620b-165">-DiskSizeInGB</span></span>
<span data-ttu-id="6620b-166">Specifica le dimensioni in gigabyte di un disco vuoto da collegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="6620b-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="6620b-167">-Lun</span></span>
<span data-ttu-id="6620b-168">Specifica il numero di unità logiche (LUN) di un disco dati.</span><span class="sxs-lookup"><span data-stu-id="6620b-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="6620b-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6620b-169">-ManagedDiskId</span></span>
<span data-ttu-id="6620b-170">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="6620b-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="6620b-171">-Name</span><span class="sxs-lookup"><span data-stu-id="6620b-171">-Name</span></span>
<span data-ttu-id="6620b-172">Specifica il nome del disco dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6620b-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="6620b-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="6620b-173">-SourceImageUri</span></span>
<span data-ttu-id="6620b-174">Specifica l'URI di origine del disco allegato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6620b-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="6620b-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6620b-175">-StorageAccountType</span></span>
<span data-ttu-id="6620b-176">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="6620b-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="6620b-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="6620b-177">-VhdUri</span></span>
<span data-ttu-id="6620b-178">Specifica l'URI (Uniform Resource Identifier) del file del disco rigido virtuale da creare quando si usa l'immagine di una piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="6620b-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="6620b-179">Questo cmdlet copia l'oggetto binario binario di grandi dimensioni (BLOB) dell'immagine in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="6620b-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="6620b-180">Si tratta della posizione da cui avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="6620b-181">-VM</span><span class="sxs-lookup"><span data-stu-id="6620b-181">-VM</span></span>
<span data-ttu-id="6620b-182">Specifica l'oggetto macchina virtuale locale a cui aggiungere un disco dati.</span><span class="sxs-lookup"><span data-stu-id="6620b-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="6620b-183">È possibile usare il cmdlet **Get-AzVM** per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="6620b-184">È possibile usare il cmdlet **New-AzVMConfig** per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6620b-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="6620b-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6620b-185">-WriteAccelerator</span></span>
<span data-ttu-id="6620b-186">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="6620b-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="6620b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6620b-187">CommonParameters</span></span>
<span data-ttu-id="6620b-188">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6620b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6620b-189">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6620b-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6620b-190">INPUT</span><span class="sxs-lookup"><span data-stu-id="6620b-190">INPUTS</span></span>

### <span data-ttu-id="6620b-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6620b-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6620b-192">System.String</span><span class="sxs-lookup"><span data-stu-id="6620b-192">System.String</span></span>

### <span data-ttu-id="6620b-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="6620b-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="6620b-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6620b-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6620b-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6620b-195">OUTPUTS</span></span>

### <span data-ttu-id="6620b-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6620b-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6620b-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="6620b-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="6620b-198">NOTE</span><span class="sxs-lookup"><span data-stu-id="6620b-198">NOTES</span></span>

## <span data-ttu-id="6620b-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6620b-199">RELATED LINKS</span></span>

[<span data-ttu-id="6620b-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6620b-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="6620b-201">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="6620b-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6620b-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6620b-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
