---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: a0aa7f095dea635574ce3fade9446864adf50d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955997"
---
# <span data-ttu-id="9d240-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9d240-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="9d240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d240-102">SYNOPSIS</span></span>
<span data-ttu-id="9d240-103">Crea un oggetto disco dati locale per una macchina virtuale o una macchina virtuale Vmss.</span><span class="sxs-lookup"><span data-stu-id="9d240-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="9d240-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d240-104">SYNTAX</span></span>

### <span data-ttu-id="9d240-105">NormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d240-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d240-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d240-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d240-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d240-107">DESCRIPTION</span></span>
<span data-ttu-id="9d240-108">Il cmdlet **New-AzVMDataDisk** crea un oggetto disco dati locale per una macchina virtuale o una VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="9d240-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="9d240-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d240-109">EXAMPLES</span></span>

### <span data-ttu-id="9d240-110">Esempio 1: Aggiungere un disco dati gestito a vmss.</span><span class="sxs-lookup"><span data-stu-id="9d240-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="9d240-111">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="9d240-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="9d240-112">Il comando successivo crea un oggetto disco di dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9d240-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="9d240-113">Il comando successivo ottiene una VM Vmss esistente specificata dal nome del gruppo di risorse, dal nome della macchina virtuale e dall'ID dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9d240-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="9d240-114">Il comando finale aggiorna Vmss VM aggiungendo un nuovo disco dati.</span><span class="sxs-lookup"><span data-stu-id="9d240-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="9d240-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9d240-115">Example 2</span></span>

<span data-ttu-id="9d240-116">Crea un oggetto disco dati locale per una macchina virtuale o una macchina virtuale Vmss.</span><span class="sxs-lookup"><span data-stu-id="9d240-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="9d240-117">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="9d240-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="9d240-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d240-118">PARAMETERS</span></span>

### <span data-ttu-id="9d240-119">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="9d240-119">-Caching</span></span>
<span data-ttu-id="9d240-120">Memorizzazione nella cache del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="9d240-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="9d240-121">-CreateOption</span></span>
<span data-ttu-id="9d240-122">Opzione di creazione del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="9d240-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d240-123">-DefaultProfile</span></span>
<span data-ttu-id="9d240-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d240-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d240-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9d240-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9d240-126">ID del set di crittografia del disco gestito dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="9d240-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9d240-127">-DiskSizeInGB</span></span>
<span data-ttu-id="9d240-128">Dimensioni del disco dati della macchina virtuale in GB.</span><span class="sxs-lookup"><span data-stu-id="9d240-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="9d240-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="9d240-129">-Lun</span></span>
<span data-ttu-id="9d240-130">Lun del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="9d240-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9d240-131">-ManagedDiskId</span></span>
<span data-ttu-id="9d240-132">ID del disco gestito dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="9d240-133">-Name</span><span class="sxs-lookup"><span data-stu-id="9d240-133">-Name</span></span>
<span data-ttu-id="9d240-134">Nome del disco dei dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="9d240-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="9d240-135">-SourceImageUri</span></span>
<span data-ttu-id="9d240-136">URI immagine di origine del disco del sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="9d240-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9d240-137">-StorageAccountType</span></span>
<span data-ttu-id="9d240-138">Tipo di account del disco gestito dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="9d240-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="9d240-139">-VhdUri</span></span>
<span data-ttu-id="9d240-140">Uri Vhd del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d240-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="9d240-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9d240-141">-WriteAccelerator</span></span>
<span data-ttu-id="9d240-142">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="9d240-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="9d240-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d240-143">CommonParameters</span></span>
<span data-ttu-id="9d240-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d240-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d240-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d240-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d240-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d240-146">INPUTS</span></span>

### <span data-ttu-id="9d240-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9d240-147">System.Int32</span></span>

### <span data-ttu-id="9d240-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9d240-148">System.String</span></span>

### <span data-ttu-id="9d240-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="9d240-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="9d240-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9d240-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9d240-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d240-151">OUTPUTS</span></span>

### <span data-ttu-id="9d240-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="9d240-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="9d240-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d240-153">NOTES</span></span>

## <span data-ttu-id="9d240-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d240-154">RELATED LINKS</span></span>
