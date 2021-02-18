---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204723"
---
# <span data-ttu-id="9bbe6-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="9bbe6-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="9bbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbe6-103">Imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="9bbe6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bbe6-104">SYNTAX</span></span>

### <span data-ttu-id="9bbe6-105">DefaultParamSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bbe6-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bbe6-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="9bbe6-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bbe6-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bbe6-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bbe6-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="9bbe6-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bbe6-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bbe6-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bbe6-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9bbe6-110">DESCRIPTION</span></span>
<span data-ttu-id="9bbe6-111">Il cmdlet **Set-AzVMOSDisk** imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="9bbe6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bbe6-112">EXAMPLES</span></span>

### <span data-ttu-id="9bbe6-113">Esempio 1: Impostare le proprietà in una macchina virtuale dall'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="9bbe6-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="9bbe6-114">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9bbe6-115">Il secondo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9bbe6-116">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9bbe6-117">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="9bbe6-118">Il comando finale imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="9bbe6-119">Esempio 2: imposta le proprietà in una macchina virtuale dall'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="9bbe6-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="9bbe6-120">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9bbe6-121">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9bbe6-122">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9bbe6-123">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="9bbe6-124">Il comando finale imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="9bbe6-125">Esempio 3: imposta le proprietà in una macchina virtuale da un'immagine utente specifica</span><span class="sxs-lookup"><span data-stu-id="9bbe6-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="9bbe6-126">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9bbe6-127">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9bbe6-128">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9bbe6-129">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="9bbe6-130">Il comando finale imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="9bbe6-131">Esempio 4: Impostare le impostazioni di crittografia del disco in un disco del sistema operativo di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9bbe6-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="9bbe6-132">Questo esempio imposta le impostazioni di crittografia del disco in un disco del sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="9bbe6-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bbe6-133">PARAMETERS</span></span>

### <span data-ttu-id="9bbe6-134">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="9bbe6-134">-Caching</span></span>
<span data-ttu-id="9bbe6-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="9bbe6-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9bbe6-136">Valid values are:</span></span> 
- <span data-ttu-id="9bbe6-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9bbe6-137">ReadOnly</span></span>
- <span data-ttu-id="9bbe6-138">ReadWrite Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="9bbe6-139">Se si modifica il valore della cache, la macchina virtuale viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="9bbe6-140">Questa impostazione influisce sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="9bbe6-141">-CreateOption</span></span>
<span data-ttu-id="9bbe6-142">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o un'immagine utente oppure collega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="9bbe6-143">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9bbe6-143">Valid values are:</span></span> 
- <span data-ttu-id="9bbe6-144">Allega.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-144">Attach.</span></span>
<span data-ttu-id="9bbe6-145">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="9bbe6-146">Quando si specifica questa opzione, non specificare il *parametro SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="9bbe6-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="9bbe6-147">Usare invece il cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="9bbe6-148">È anche necessario usare i parametri *di Windows* o *Linux* per indicare alla piattaforma azure il tipo del sistema operativo nel disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="9bbe6-149">Il *parametro VhdUri* è sufficiente per indicare alla piattaforma azure la posizione del disco da collegare.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="9bbe6-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-150">FromImage.</span></span>
<span data-ttu-id="9bbe6-151">Specificare questa opzione per creare una macchina virtuale da un'immagine della piattaforma o da un'immagine utente generalizzata.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="9bbe6-152">Nel caso di un'immagine utente generalizzata, è necessario specificare anche il parametro *SourceImageUri* e i parametri *di Windows* o *Linux* per indicare alla piattaforma Azure la posizione e il tipo del disco del sistema operativo VHD invece di usare il cmdlet **Set-AzVMSourceImage.**</span><span class="sxs-lookup"><span data-stu-id="9bbe6-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="9bbe6-153">Nel caso di un'immagine della piattaforma, il *parametro VhdUri* è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="9bbe6-154">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbe6-155">-DefaultProfile</span></span>
<span data-ttu-id="9bbe6-156">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bbe6-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="9bbe6-157">-DiffDiskSetting</span></span>
<span data-ttu-id="9bbe6-158">Specifica le impostazioni disco diverse per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="9bbe6-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="9bbe6-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="9bbe6-160">Specifica il percorso della chiave di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9bbe6-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="9bbe6-162">Specifica l'ID della risorsa del Vault della chiave contenente la chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9bbe6-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9bbe6-164">Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="9bbe6-165">Può essere specificato solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="9bbe6-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9bbe6-166">-DiskSizeInGB</span></span>
<span data-ttu-id="9bbe6-167">Specifica le dimensioni, in GB, del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="9bbe6-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="9bbe6-169">Specifica la posizione della chiave di crittografia della chiave.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9bbe6-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="9bbe6-171">Specifica l'ID della risorsa del Vault della chiave contenente la chiave di crittografia della chiave.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="9bbe6-172">-Linux</span></span>
<span data-ttu-id="9bbe6-173">Indica che il sistema operativo nell'immagine utente è Linux.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="9bbe6-174">Specificare questo parametro per la distribuzione di macchine virtuali basate su immagini utente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9bbe6-175">-ManagedDiskId</span></span>
<span data-ttu-id="9bbe6-176">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="9bbe6-177">-Name</span><span class="sxs-lookup"><span data-stu-id="9bbe6-177">-Name</span></span>
<span data-ttu-id="9bbe6-178">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="9bbe6-179">-SourceImageUri</span></span>
<span data-ttu-id="9bbe6-180">Specifica l'URI del disco rigido virtuale per gli scenari con immagini utente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9bbe6-181">-StorageAccountType</span></span>
<span data-ttu-id="9bbe6-182">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="9bbe6-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="9bbe6-183">-VhdUri</span></span>
<span data-ttu-id="9bbe6-184">Specifica l'URI (Uniform Resource Identifier) di un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="9bbe6-185">Per una macchina virtuale basata su immagini, questo parametro specifica il file VHD da creare quando si specifica un'immagine della piattaforma o dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="9bbe6-186">Posizione da cui viene copiato il BLOB (Binary Large Object) dell'immagine per avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="9bbe6-187">Per uno scenario di avvio basato su disco della macchina virtuale, questo parametro specifica il file VHD che la macchina virtuale usa direttamente per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-188">-VM</span><span class="sxs-lookup"><span data-stu-id="9bbe6-188">-VM</span></span>
<span data-ttu-id="9bbe6-189">Specifica l'oggetto della macchina virtuale locale su cui impostare le proprietà del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="9bbe6-190">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="9bbe6-191">-Windows</span></span>
<span data-ttu-id="9bbe6-192">Indica che il sistema operativo nell'immagine utente è Windows.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbe6-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9bbe6-193">-WriteAccelerator</span></span>
<span data-ttu-id="9bbe6-194">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="9bbe6-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbe6-195">CommonParameters</span></span>
<span data-ttu-id="9bbe6-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbe6-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bbe6-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbe6-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="9bbe6-198">INPUTS</span></span>

### <span data-ttu-id="9bbe6-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9bbe6-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9bbe6-200">System.String</span><span class="sxs-lookup"><span data-stu-id="9bbe6-200">System.String</span></span>

## <span data-ttu-id="9bbe6-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bbe6-201">OUTPUTS</span></span>

### <span data-ttu-id="9bbe6-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9bbe6-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9bbe6-203">NOTE</span><span class="sxs-lookup"><span data-stu-id="9bbe6-203">NOTES</span></span>

## <span data-ttu-id="9bbe6-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bbe6-204">RELATED LINKS</span></span>

[<span data-ttu-id="9bbe6-205">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="9bbe6-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9bbe6-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9bbe6-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="9bbe6-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9bbe6-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


