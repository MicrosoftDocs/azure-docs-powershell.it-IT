---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: 89a45e785252d1351e41e895cc610a75cbf6c5fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515455"
---
# <span data-ttu-id="eebdc-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="eebdc-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="eebdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eebdc-102">SYNOPSIS</span></span>
<span data-ttu-id="eebdc-103">Imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eebdc-104">SYNTAX</span></span>

### <span data-ttu-id="eebdc-105">DefaultParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eebdc-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eebdc-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="eebdc-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eebdc-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebdc-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eebdc-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="eebdc-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eebdc-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebdc-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eebdc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eebdc-110">DESCRIPTION</span></span>
<span data-ttu-id="eebdc-111">Il cmdlet **set-AzureRmVMOSDisk** imposta le proprietà del disco del sistema operativo in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="eebdc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eebdc-112">EXAMPLES</span></span>

### <span data-ttu-id="eebdc-113">Esempio 1: impostare le proprietà in una macchina virtuale dall'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="eebdc-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="eebdc-114">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="eebdc-115">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eebdc-116">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eebdc-117">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="eebdc-118">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="eebdc-119">Esempio 2: imposta le proprietà in una macchina virtuale dall'immagine utente generalizzata</span><span class="sxs-lookup"><span data-stu-id="eebdc-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="eebdc-120">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="eebdc-121">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eebdc-122">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eebdc-123">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="eebdc-124">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="eebdc-125">Esempio 3: imposta le proprietà in una macchina virtuale dall'immagine utente specializzata</span><span class="sxs-lookup"><span data-stu-id="eebdc-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="eebdc-126">Il primo comando ottiene il set di disponibilità denominato AvailablitySet13 nel gruppo di risorse denominato ResourceGroup11 e archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="eebdc-127">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eebdc-128">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eebdc-129">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="eebdc-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="eebdc-130">Il comando Final imposta le proprietà della macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="eebdc-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="eebdc-131">Esempio 4: impostare le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="eebdc-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="eebdc-132">Questo esempio imposta le impostazioni di crittografia del disco in un disco di sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="eebdc-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eebdc-133">PARAMETERS</span></span>

### <span data-ttu-id="eebdc-134">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="eebdc-134">-Caching</span></span>
<span data-ttu-id="eebdc-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="eebdc-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="eebdc-136">Valid values are:</span></span> 
- <span data-ttu-id="eebdc-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="eebdc-137">ReadOnly</span></span>
- <span data-ttu-id="eebdc-138">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="eebdc-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="eebdc-139">La modifica del valore di memorizzazione nella cache fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="eebdc-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="eebdc-140">Questa impostazione influisce sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="eebdc-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="eebdc-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="eebdc-141">-CreateOption</span></span>
<span data-ttu-id="eebdc-142">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente oppure allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="eebdc-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="eebdc-143">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="eebdc-143">Valid values are:</span></span> 
- <span data-ttu-id="eebdc-144">Allegare.</span><span class="sxs-lookup"><span data-stu-id="eebdc-144">Attach.</span></span>
<span data-ttu-id="eebdc-145">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="eebdc-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="eebdc-146">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="eebdc-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="eebdc-147">USA invece il cmdlet Set-AzureRmVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="eebdc-147">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="eebdc-148">Devi anche usare i parametri *Windows* o *Linux* per indicare alla piattaforma Azure il tipo di sistema operativo nel VHD.</span><span class="sxs-lookup"><span data-stu-id="eebdc-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="eebdc-149">Il parametro *VhdUri* è sufficiente per indicare alla piattaforma Azure la posizione del disco da allegare.</span><span class="sxs-lookup"><span data-stu-id="eebdc-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="eebdc-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="eebdc-150">FromImage.</span></span>
<span data-ttu-id="eebdc-151">Specifica questa opzione per creare una macchina virtuale da un'immagine della piattaforma o da un'immagine utente generalizzata.</span><span class="sxs-lookup"><span data-stu-id="eebdc-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="eebdc-152">Nel caso di un'immagine utente generalizzata, devi anche specificare il parametro *SourceImageUri* e i parametri *Windows* o *Linux* per indicare alla piattaforma Azure la posizione e il tipo del disco rigido virtuale dei dischi del sistema operativo invece di usare il cmdlet **set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="eebdc-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="eebdc-153">Nel caso di un'immagine della piattaforma, il parametro *VhdUri* è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="eebdc-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="eebdc-154">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="eebdc-154">Empty.</span></span>

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

### <span data-ttu-id="eebdc-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebdc-155">-DefaultProfile</span></span>
<span data-ttu-id="eebdc-156">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eebdc-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eebdc-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="eebdc-157">-DiffDiskSetting</span></span>
<span data-ttu-id="eebdc-158">Specifica le impostazioni del disco differenze per il disco di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="eebdc-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="eebdc-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="eebdc-160">Specifica la posizione della chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="eebdc-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="eebdc-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="eebdc-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="eebdc-162">Specifica l'ID risorsa dell'archivio di chiavi contenente la chiave di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="eebdc-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="eebdc-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="eebdc-163">-DiskSizeInGB</span></span>
<span data-ttu-id="eebdc-164">Specifica le dimensioni, in GB, del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-164">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="eebdc-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="eebdc-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="eebdc-166">Specifica la posizione della chiave di crittografia chiave.</span><span class="sxs-lookup"><span data-stu-id="eebdc-166">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="eebdc-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="eebdc-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="eebdc-168">Specifica l'ID risorsa della chiave di volta contenente la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="eebdc-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="eebdc-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="eebdc-169">-Linux</span></span>
<span data-ttu-id="eebdc-170">Indica che il sistema operativo nell'immagine utente è Linux.</span><span class="sxs-lookup"><span data-stu-id="eebdc-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="eebdc-171">Specifica questo parametro per la distribuzione di macchine virtuali basate su immagini utente.</span><span class="sxs-lookup"><span data-stu-id="eebdc-171">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="eebdc-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="eebdc-172">-ManagedDiskId</span></span>
<span data-ttu-id="eebdc-173">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="eebdc-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="eebdc-174">-Nome</span><span class="sxs-lookup"><span data-stu-id="eebdc-174">-Name</span></span>
<span data-ttu-id="eebdc-175">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-175">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="eebdc-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="eebdc-176">-SourceImageUri</span></span>
<span data-ttu-id="eebdc-177">Specifica l'URI del VHD per gli scenari di immagini utente.</span><span class="sxs-lookup"><span data-stu-id="eebdc-177">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="eebdc-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="eebdc-178">-StorageAccountType</span></span>
<span data-ttu-id="eebdc-179">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="eebdc-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="eebdc-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="eebdc-180">-VhdUri</span></span>
<span data-ttu-id="eebdc-181">Specifica l'URI (Uniform Resource Identifier) di un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="eebdc-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="eebdc-182">Per una macchina virtuale basata su immagini, questo parametro specifica il file VHD da creare quando viene specificata un'immagine della piattaforma o un'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="eebdc-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="eebdc-183">Questa è la posizione da cui viene copiato l'oggetto binario di grandi dimensioni (BLOB) dell'immagine per avviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eebdc-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="eebdc-184">Per uno scenario di avvio di una macchina virtuale basata su disco, questo parametro specifica il file VHD usato direttamente dalla macchina virtuale per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="eebdc-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="eebdc-185">-VM</span><span class="sxs-lookup"><span data-stu-id="eebdc-185">-VM</span></span>
<span data-ttu-id="eebdc-186">Specifica l'oggetto macchina virtuale locale in cui impostare le proprietà del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="eebdc-187">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="eebdc-187">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="eebdc-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="eebdc-188">-Windows</span></span>
<span data-ttu-id="eebdc-189">Indica che il sistema operativo nell'immagine utente è Windows.</span><span class="sxs-lookup"><span data-stu-id="eebdc-189">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="eebdc-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="eebdc-190">-WriteAccelerator</span></span>
<span data-ttu-id="eebdc-191">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eebdc-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="eebdc-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebdc-192">CommonParameters</span></span>
<span data-ttu-id="eebdc-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebdc-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebdc-194">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebdc-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebdc-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eebdc-195">INPUTS</span></span>

### <span data-ttu-id="eebdc-196">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eebdc-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>
<span data-ttu-id="eebdc-197">Parametri: VM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eebdc-197">Parameters: VM (ByValue)</span></span>

## <span data-ttu-id="eebdc-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eebdc-198">OUTPUTS</span></span>

### <span data-ttu-id="eebdc-199">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eebdc-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="eebdc-200">Note</span><span class="sxs-lookup"><span data-stu-id="eebdc-200">NOTES</span></span>

## <span data-ttu-id="eebdc-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eebdc-201">RELATED LINKS</span></span>

[<span data-ttu-id="eebdc-202">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eebdc-202">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="eebdc-203">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eebdc-203">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="eebdc-204">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="eebdc-204">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


