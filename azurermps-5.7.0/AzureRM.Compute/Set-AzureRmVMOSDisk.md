---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509955"
---
# <span data-ttu-id="4dfe2-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="4dfe2-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="4dfe2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfe2-103">Imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dfe2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dfe2-104">SYNTAX</span></span>

### <span data-ttu-id="4dfe2-105">DefaultParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4dfe2-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dfe2-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="4dfe2-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dfe2-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfe2-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="4dfe2-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="4dfe2-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dfe2-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfe2-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="4dfe2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dfe2-110">DESCRIPTION</span></span>
<span data-ttu-id="4dfe2-111">Il cmdlet **set-AzureRmVMOSDisk** imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="4dfe2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dfe2-112">EXAMPLES</span></span>

### <span data-ttu-id="4dfe2-113">Esempio 1: impostare le proprietà in una macchina virtuale dall'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="4dfe2-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4dfe2-114">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4dfe2-115">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4dfe2-116">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4dfe2-117">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4dfe2-118">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4dfe2-119">Esempio 2: imposta le proprietà in una macchina virtuale dall'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="4dfe2-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4dfe2-120">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4dfe2-121">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4dfe2-122">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4dfe2-123">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4dfe2-124">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4dfe2-125">Esempio 3: imposta le proprietà in una macchina virtuale dall'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="4dfe2-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4dfe2-126">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4dfe2-127">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4dfe2-128">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4dfe2-129">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4dfe2-130">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4dfe2-131">Esempio 4: impostare le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="4dfe2-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="4dfe2-132">Questo esempio imposta le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="4dfe2-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dfe2-133">PARAMETERS</span></span>

### <span data-ttu-id="4dfe2-134">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="4dfe2-134">-Caching</span></span>
<span data-ttu-id="4dfe2-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="4dfe2-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4dfe2-136">Valid values are:</span></span> 

- <span data-ttu-id="4dfe2-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dfe2-137">ReadOnly</span></span>
- <span data-ttu-id="4dfe2-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4dfe2-138">ReadWrite</span></span>

<span data-ttu-id="4dfe2-139">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="4dfe2-140">La modifica del valore di memorizzazione nella cache fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="4dfe2-141">Questa impostazione influisce sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-141">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="4dfe2-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4dfe2-142">-CreateOption</span></span>
<span data-ttu-id="4dfe2-143">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente oppure allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="4dfe2-144">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4dfe2-144">Valid values are:</span></span> 

- <span data-ttu-id="4dfe2-145">Allegare.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-145">Attach.</span></span>
<span data-ttu-id="4dfe2-146">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="4dfe2-147">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="4dfe2-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="4dfe2-148">USA invece il cmdlet Set-AzureRmVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="4dfe2-149">Devi anche usare i parametri *Windows* o *Linux* per indicare alla piattaforma azure2 il tipo di sistema operativo nel VHD.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="4dfe2-150">Il parametro *VhdUri* è sufficiente per indicare alla piattaforma azure2 la posizione del disco da allegare.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="4dfe2-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-151">FromImage.</span></span>
<span data-ttu-id="4dfe2-152">Specifica questa opzione per creare una macchina virtuale da un'immagine della piattaforma o da un'immagine utente generalizzata.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="4dfe2-153">Nel caso di un'immagine utente generalizzata, devi anche specificare il parametro *SourceImageUri* e i parametri *Windows* o *Linux* per indicare alla piattaforma Azure la posizione e il tipo del disco rigido virtuale dei dischi del sistema operativo invece di usare il cmdlet **set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="4dfe2-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="4dfe2-154">Nel caso di un'immagine della piattaforma, il parametro *VhdUri* è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="4dfe2-155">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="4dfe2-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="4dfe2-157">Specifica la posizione della chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4dfe2-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="4dfe2-159">Specifica l'ID risorsa dell'archivio di chiavi contenente la chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4dfe2-160">-DiskSizeInGB</span></span>
<span data-ttu-id="4dfe2-161">Specifica le dimensioni, in GB, del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="4dfe2-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="4dfe2-163">Specifica la posizione della chiave di crittografia chiave.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4dfe2-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="4dfe2-165">Specifica l'ID risorsa della chiave di volta contenente la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="4dfe2-166">-Linux</span></span>
<span data-ttu-id="4dfe2-167">Indica che il sistema operativo nell'immagine utente è Linux.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="4dfe2-168">Specifica questo parametro per la distribuzione di macchine virtuali basate su immagini utente.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4dfe2-169">-ManagedDiskId</span></span>
<span data-ttu-id="4dfe2-170">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-171">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dfe2-171">-Name</span></span>
<span data-ttu-id="4dfe2-172">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="4dfe2-173">-SourceImageUri</span></span>
<span data-ttu-id="4dfe2-174">Specifica l'URI del VHD per gli scenari di immagini utente.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4dfe2-175">-StorageAccountType</span></span>
<span data-ttu-id="4dfe2-176">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4dfe2-177">-VhdUri</span></span>
<span data-ttu-id="4dfe2-178">Specifica l'URI (Uniform Resource Identifier) di un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="4dfe2-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="4dfe2-179">Per una macchina virtuale basata su immagini, questo parametro specifica il file VHD da creare quando viene specificata un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="4dfe2-180">Questa è la posizione da cui viene copiato l'oggetto binario di grandi dimensioni (BLOB) dell'immagine per avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="4dfe2-181">Per uno scenario di avvio di una macchina virtuale basata su disco, questo parametro specifica il file VHD usato direttamente dalla macchina virtuale per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-182">-VM</span><span class="sxs-lookup"><span data-stu-id="4dfe2-182">-VM</span></span>
<span data-ttu-id="4dfe2-183">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="4dfe2-184">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="4dfe2-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="4dfe2-185">-Windows</span></span>
<span data-ttu-id="4dfe2-186">Indica che il sistema operativo nell'immagine utente è Windows.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe2-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfe2-187">CommonParameters</span></span>
<span data-ttu-id="4dfe2-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfe2-189">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dfe2-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfe2-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dfe2-190">INPUTS</span></span>

### <span data-ttu-id="4dfe2-191">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4dfe2-191">None</span></span>
<span data-ttu-id="4dfe2-192">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4dfe2-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4dfe2-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dfe2-193">OUTPUTS</span></span>

## <span data-ttu-id="4dfe2-194">Note</span><span class="sxs-lookup"><span data-stu-id="4dfe2-194">NOTES</span></span>

## <span data-ttu-id="4dfe2-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dfe2-195">RELATED LINKS</span></span>

[<span data-ttu-id="4dfe2-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dfe2-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4dfe2-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4dfe2-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4dfe2-198">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4dfe2-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


