---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334243"
---
# <span data-ttu-id="de015-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="de015-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="de015-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de015-102">SYNOPSIS</span></span>
<span data-ttu-id="de015-103">Imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="de015-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de015-104">SYNTAX</span></span>

### <span data-ttu-id="de015-105">DefaultParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de015-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de015-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="de015-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de015-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="de015-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de015-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="de015-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de015-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="de015-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de015-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de015-110">DESCRIPTION</span></span>
<span data-ttu-id="de015-111">Il cmdlet **set-AzVMOSDisk** imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="de015-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de015-112">EXAMPLES</span></span>

### <span data-ttu-id="de015-113">Esempio 1: impostare le proprietà in una macchina virtuale dall'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="de015-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="de015-114">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="de015-115">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="de015-116">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="de015-117">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="de015-118">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="de015-119">Esempio 2: imposta le proprietà in una macchina virtuale dall'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="de015-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="de015-120">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="de015-121">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="de015-122">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="de015-123">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="de015-124">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="de015-125">Esempio 3: imposta le proprietà in una macchina virtuale dall'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="de015-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="de015-126">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="de015-127">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="de015-128">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="de015-129">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="de015-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="de015-130">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="de015-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="de015-131">Esempio 4: impostare le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="de015-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="de015-132">Questo esempio imposta le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="de015-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de015-133">PARAMETERS</span></span>

### <span data-ttu-id="de015-134">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="de015-134">-Caching</span></span>
<span data-ttu-id="de015-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="de015-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="de015-136">Valid values are:</span></span> 
- <span data-ttu-id="de015-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="de015-137">ReadOnly</span></span>
- <span data-ttu-id="de015-138">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="de015-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="de015-139">La modifica del valore di memorizzazione nella cache fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="de015-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="de015-140">Questa impostazione influisce sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="de015-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="de015-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="de015-141">-CreateOption</span></span>
<span data-ttu-id="de015-142">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente oppure allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="de015-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="de015-143">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="de015-143">Valid values are:</span></span> 
- <span data-ttu-id="de015-144">Allegare.</span><span class="sxs-lookup"><span data-stu-id="de015-144">Attach.</span></span>
<span data-ttu-id="de015-145">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="de015-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="de015-146">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="de015-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="de015-147">USA invece il cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="de015-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="de015-148">Devi anche usare i parametri *Windows* o *Linux* per indicare alla piattaforma Azure il tipo di sistema operativo nel VHD.</span><span class="sxs-lookup"><span data-stu-id="de015-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="de015-149">Il parametro *VhdUri* è sufficiente per indicare alla piattaforma Azure la posizione del disco da allegare.</span><span class="sxs-lookup"><span data-stu-id="de015-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="de015-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="de015-150">FromImage.</span></span>
<span data-ttu-id="de015-151">Specifica questa opzione per creare una macchina virtuale da un'immagine della piattaforma o da un'immagine utente generalizzata.</span><span class="sxs-lookup"><span data-stu-id="de015-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="de015-152">Nel caso di un'immagine utente generalizzata, devi anche specificare il parametro *SourceImageUri* e i parametri *Windows* o *Linux* per indicare alla piattaforma Azure la posizione e il tipo del disco rigido virtuale dei dischi del sistema operativo invece di usare il cmdlet **set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="de015-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="de015-153">Nel caso di un'immagine della piattaforma, il parametro *VhdUri* è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="de015-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="de015-154">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="de015-154">Empty.</span></span>

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

### <span data-ttu-id="de015-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de015-155">-DefaultProfile</span></span>
<span data-ttu-id="de015-156">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de015-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de015-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="de015-157">-DiffDiskSetting</span></span>
<span data-ttu-id="de015-158">Specifica le impostazioni del disco differenze per il disco di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="de015-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="de015-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="de015-160">Specifica la posizione della chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="de015-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="de015-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="de015-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="de015-162">Specifica l'ID risorsa dell'archivio di chiavi contenente la chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="de015-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="de015-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="de015-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="de015-164">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="de015-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="de015-165">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="de015-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="de015-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="de015-166">-DiskSizeInGB</span></span>
<span data-ttu-id="de015-167">Specifica le dimensioni, in GB, del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="de015-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="de015-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="de015-169">Specifica la posizione della chiave di crittografia chiave.</span><span class="sxs-lookup"><span data-stu-id="de015-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="de015-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="de015-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="de015-171">Specifica l'ID risorsa della chiave di volta contenente la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="de015-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="de015-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="de015-172">-Linux</span></span>
<span data-ttu-id="de015-173">Indica che il sistema operativo nell'immagine utente è Linux.</span><span class="sxs-lookup"><span data-stu-id="de015-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="de015-174">Specifica questo parametro per la distribuzione di macchine virtuali basate su immagini utente.</span><span class="sxs-lookup"><span data-stu-id="de015-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="de015-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="de015-175">-ManagedDiskId</span></span>
<span data-ttu-id="de015-176">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="de015-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="de015-177">-Nome</span><span class="sxs-lookup"><span data-stu-id="de015-177">-Name</span></span>
<span data-ttu-id="de015-178">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="de015-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="de015-179">-SourceImageUri</span></span>
<span data-ttu-id="de015-180">Specifica l'URI del VHD per gli scenari di immagini utente.</span><span class="sxs-lookup"><span data-stu-id="de015-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="de015-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="de015-181">-StorageAccountType</span></span>
<span data-ttu-id="de015-182">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="de015-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="de015-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="de015-183">-VhdUri</span></span>
<span data-ttu-id="de015-184">Specifica l'URI (Uniform Resource Identifier) di un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="de015-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="de015-185">Per una macchina virtuale basata su immagini, questo parametro specifica il file VHD da creare quando viene specificata un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="de015-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="de015-186">Questa è la posizione da cui viene copiato l'oggetto binario di grandi dimensioni (BLOB) dell'immagine per avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de015-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="de015-187">Per uno scenario di avvio di una macchina virtuale basata su disco, questo parametro specifica il file VHD usato direttamente dalla macchina virtuale per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="de015-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="de015-188">-VM</span><span class="sxs-lookup"><span data-stu-id="de015-188">-VM</span></span>
<span data-ttu-id="de015-189">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="de015-190">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="de015-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="de015-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="de015-191">-Windows</span></span>
<span data-ttu-id="de015-192">Indica che il sistema operativo nell'immagine utente è Windows.</span><span class="sxs-lookup"><span data-stu-id="de015-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="de015-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="de015-193">-WriteAccelerator</span></span>
<span data-ttu-id="de015-194">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="de015-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="de015-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de015-195">CommonParameters</span></span>
<span data-ttu-id="de015-196">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de015-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de015-197">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de015-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de015-198">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de015-198">INPUTS</span></span>

### <span data-ttu-id="de015-199">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="de015-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="de015-200">System. String</span><span class="sxs-lookup"><span data-stu-id="de015-200">System.String</span></span>

## <span data-ttu-id="de015-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de015-201">OUTPUTS</span></span>

### <span data-ttu-id="de015-202">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="de015-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="de015-203">Note</span><span class="sxs-lookup"><span data-stu-id="de015-203">NOTES</span></span>

## <span data-ttu-id="de015-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de015-204">RELATED LINKS</span></span>

[<span data-ttu-id="de015-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="de015-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="de015-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de015-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="de015-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="de015-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


