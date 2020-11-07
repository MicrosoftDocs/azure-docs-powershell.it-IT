---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 378d0d33d6cc1ceb2eca4773d93f76afbf75cf4b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863361"
---
# <span data-ttu-id="f9fb8-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f9fb8-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="f9fb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fb8-103">Imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="f9fb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9fb8-104">SYNTAX</span></span>

### <span data-ttu-id="f9fb8-105">DefaultParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9fb8-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9fb8-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9fb8-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9fb8-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9fb8-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9fb8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9fb8-110">DESCRIPTION</span></span>
<span data-ttu-id="f9fb8-111">Il cmdlet **set-AzVMOSDisk** imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="f9fb8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9fb8-112">EXAMPLES</span></span>

### <span data-ttu-id="f9fb8-113">Esempio 1: impostare le proprietà in una macchina virtuale dall'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="f9fb8-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f9fb8-114">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f9fb8-115">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f9fb8-116">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f9fb8-117">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f9fb8-118">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f9fb8-119">Esempio 2: imposta le proprietà in una macchina virtuale dall'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="f9fb8-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f9fb8-120">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f9fb8-121">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f9fb8-122">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f9fb8-123">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f9fb8-124">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f9fb8-125">Esempio 3: imposta le proprietà in una macchina virtuale dall'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="f9fb8-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f9fb8-126">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f9fb8-127">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f9fb8-128">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f9fb8-129">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f9fb8-130">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f9fb8-131">Esempio 4: impostare le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f9fb8-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="f9fb8-132">Questo esempio imposta le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="f9fb8-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9fb8-133">PARAMETERS</span></span>

### <span data-ttu-id="f9fb8-134">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="f9fb8-134">-Caching</span></span>
<span data-ttu-id="f9fb8-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="f9fb8-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f9fb8-136">Valid values are:</span></span> 

- <span data-ttu-id="f9fb8-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f9fb8-137">ReadOnly</span></span>
- <span data-ttu-id="f9fb8-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9fb8-138">ReadWrite</span></span>

<span data-ttu-id="f9fb8-139">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="f9fb8-140">La modifica del valore di memorizzazione nella cache fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="f9fb8-141">Questa impostazione influisce sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f9fb8-142">-CreateOption</span></span>
<span data-ttu-id="f9fb8-143">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente oppure allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="f9fb8-144">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f9fb8-144">Valid values are:</span></span> 

- <span data-ttu-id="f9fb8-145">Allegare.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-145">Attach.</span></span>
<span data-ttu-id="f9fb8-146">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="f9fb8-147">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="f9fb8-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="f9fb8-148">USA invece il cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-148">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="f9fb8-149">Devi anche usare i parametri *Windows* o *Linux* per indicare alla piattaforma azure2 il tipo di sistema operativo nel VHD.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="f9fb8-150">Il parametro *VhdUri* è sufficiente per indicare alla piattaforma azure2 la posizione del disco da allegare.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="f9fb8-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-151">FromImage.</span></span>
<span data-ttu-id="f9fb8-152">Specifica questa opzione per creare una macchina virtuale da un'immagine della piattaforma o da un'immagine utente generalizzata.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="f9fb8-153">Nel caso di un'immagine utente generalizzata, devi anche specificare il parametro *SourceImageUri* e i parametri *Windows* o *Linux* per indicare alla piattaforma Azure la posizione e il tipo del disco rigido virtuale dei dischi del sistema operativo invece di usare il cmdlet **set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="f9fb8-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="f9fb8-154">Nel caso di un'immagine della piattaforma, il parametro *VhdUri* è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="f9fb8-155">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fb8-156">-DefaultProfile</span></span>
<span data-ttu-id="f9fb8-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9fb8-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f9fb8-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="f9fb8-159">Specifica la posizione della chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f9fb8-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="f9fb8-161">Specifica l'ID risorsa dell'archivio di chiavi contenente la chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f9fb8-162">-DiskSizeInGB</span></span>
<span data-ttu-id="f9fb8-163">Specifica le dimensioni, in GB, del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f9fb8-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f9fb8-165">Specifica la posizione della chiave di crittografia chiave.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f9fb8-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="f9fb8-167">Specifica l'ID risorsa della chiave di volta contenente la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="f9fb8-168">-Linux</span></span>
<span data-ttu-id="f9fb8-169">Indica che il sistema operativo nell'immagine utente è Linux.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="f9fb8-170">Specifica questo parametro per la distribuzione di macchine virtuali basate su immagini utente.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f9fb8-171">-ManagedDiskId</span></span>
<span data-ttu-id="f9fb8-172">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-172">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-173">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9fb8-173">-Name</span></span>
<span data-ttu-id="f9fb8-174">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="f9fb8-175">-SourceImageUri</span></span>
<span data-ttu-id="f9fb8-176">Specifica l'URI del VHD per gli scenari di immagini utente.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f9fb8-177">-StorageAccountType</span></span>
<span data-ttu-id="f9fb8-178">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f9fb8-179">-VhdUri</span></span>
<span data-ttu-id="f9fb8-180">Specifica l'URI (Uniform Resource Identifier) di un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="f9fb8-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="f9fb8-181">Per una macchina virtuale basata su immagini, questo parametro specifica il file VHD da creare quando viene specificata un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="f9fb8-182">Questa è la posizione da cui viene copiato l'oggetto binario di grandi dimensioni (BLOB) dell'immagine per avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="f9fb8-183">Per uno scenario di avvio di una macchina virtuale basata su disco, questo parametro specifica il file VHD usato direttamente dalla macchina virtuale per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-184">-VM</span><span class="sxs-lookup"><span data-stu-id="f9fb8-184">-VM</span></span>
<span data-ttu-id="f9fb8-185">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="f9fb8-186">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-186">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="f9fb8-187">-Windows</span></span>
<span data-ttu-id="f9fb8-188">Indica che il sistema operativo nell'immagine utente è Windows.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb8-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f9fb8-189">-WriteAccelerator</span></span>
<span data-ttu-id="f9fb8-190">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="f9fb8-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fb8-191">CommonParameters</span></span>
<span data-ttu-id="f9fb8-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fb8-193">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fb8-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fb8-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9fb8-194">INPUTS</span></span>

### <span data-ttu-id="f9fb8-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9fb8-195">PSVirtualMachine</span></span>
<span data-ttu-id="f9fb8-196">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f9fb8-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="f9fb8-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9fb8-197">OUTPUTS</span></span>

### <span data-ttu-id="f9fb8-198">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9fb8-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f9fb8-199">Note</span><span class="sxs-lookup"><span data-stu-id="f9fb8-199">NOTES</span></span>

## <span data-ttu-id="f9fb8-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9fb8-200">RELATED LINKS</span></span>

[<span data-ttu-id="f9fb8-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9fb8-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f9fb8-202">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-202">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f9fb8-203">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f9fb8-203">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


