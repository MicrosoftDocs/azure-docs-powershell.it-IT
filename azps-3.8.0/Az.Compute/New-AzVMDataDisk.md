---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019400"
---
# <span data-ttu-id="87627-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="87627-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="87627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87627-102">SYNOPSIS</span></span>
<span data-ttu-id="87627-103">Crea un oggetto disco dati locale per una macchina virtuale o una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="87627-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="87627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87627-104">SYNTAX</span></span>

### <span data-ttu-id="87627-105">NormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87627-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87627-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="87627-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87627-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87627-107">DESCRIPTION</span></span>
<span data-ttu-id="87627-108">Il cmdlet **New-AzVMDataDisk** crea un oggetto disco di dati locale per una macchina virtuale o una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="87627-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="87627-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87627-109">EXAMPLES</span></span>

### <span data-ttu-id="87627-110">Esempio 1: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="87627-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="87627-111">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="87627-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="87627-112">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="87627-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="87627-113">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="87627-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="87627-114">Il comando finale aggiorna la VM vmss aggiungendo un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="87627-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="87627-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87627-115">PARAMETERS</span></span>

### <span data-ttu-id="87627-116">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="87627-116">-Caching</span></span>
<span data-ttu-id="87627-117">Memorizzazione nella cache del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="87627-118">-CreateOption</span></span>
<span data-ttu-id="87627-119">Opzione Crea del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87627-120">-DefaultProfile</span></span>
<span data-ttu-id="87627-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87627-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87627-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="87627-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="87627-123">ID della macchina virtuale Managed Disk Encryption set.</span><span class="sxs-lookup"><span data-stu-id="87627-123">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="87627-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="87627-124">-DiskSizeInGB</span></span>
<span data-ttu-id="87627-125">Dimensioni del disco di dati della macchina virtuale in GB.</span><span class="sxs-lookup"><span data-stu-id="87627-125">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-126">-Lun</span><span class="sxs-lookup"><span data-stu-id="87627-126">-Lun</span></span>
<span data-ttu-id="87627-127">Lun del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-127">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="87627-128">-ManagedDiskId</span></span>
<span data-ttu-id="87627-129">ID del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-129">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="87627-130">-Name</span></span>
<span data-ttu-id="87627-131">Nome del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="87627-132">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="87627-132">-SourceImageUri</span></span>
<span data-ttu-id="87627-133">URI dell'immagine di origine del disco operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-133">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="87627-134">-StorageAccountType</span></span>
<span data-ttu-id="87627-135">Tipo di account del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-135">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="87627-136">-VhdUri</span></span>
<span data-ttu-id="87627-137">URI VHD del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87627-137">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87627-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="87627-138">-WriteAccelerator</span></span>
<span data-ttu-id="87627-139">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="87627-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87627-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87627-140">CommonParameters</span></span>
<span data-ttu-id="87627-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87627-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87627-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87627-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87627-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87627-143">INPUTS</span></span>

### <span data-ttu-id="87627-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="87627-144">System.Int32</span></span>

### <span data-ttu-id="87627-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87627-145">System.String</span></span>

### <span data-ttu-id="87627-146">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="87627-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="87627-147">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87627-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="87627-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87627-148">OUTPUTS</span></span>

### <span data-ttu-id="87627-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="87627-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="87627-150">Note</span><span class="sxs-lookup"><span data-stu-id="87627-150">NOTES</span></span>

## <span data-ttu-id="87627-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87627-151">RELATED LINKS</span></span>
