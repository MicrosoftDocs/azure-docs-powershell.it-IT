---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: d7ce0b96c4ab286e21c253d701ec6d21c385ac56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675313"
---
# <span data-ttu-id="12340-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="12340-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="12340-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12340-102">SYNOPSIS</span></span>
<span data-ttu-id="12340-103">Crea un oggetto disco dati locale per una macchina virtuale o una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="12340-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="12340-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12340-104">SYNTAX</span></span>

### <span data-ttu-id="12340-105">NormalDiskParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12340-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12340-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="12340-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12340-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12340-107">DESCRIPTION</span></span>
<span data-ttu-id="12340-108">Il cmdlet **New-AzVMDataDisk** crea un oggetto disco di dati locale per una macchina virtuale o una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="12340-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="12340-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12340-109">EXAMPLES</span></span>

### <span data-ttu-id="12340-110">Esempio 1: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="12340-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="12340-111">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="12340-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="12340-112">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="12340-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="12340-113">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="12340-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="12340-114">Il comando finale aggiorna la VM vmss aggiungendo un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="12340-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="12340-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12340-115">PARAMETERS</span></span>

### <span data-ttu-id="12340-116">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="12340-116">-Caching</span></span>
<span data-ttu-id="12340-117">Memorizzazione nella cache del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="12340-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="12340-118">-CreateOption</span></span>
<span data-ttu-id="12340-119">Opzione Crea del disco dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="12340-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12340-120">-DefaultProfile</span></span>
<span data-ttu-id="12340-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12340-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12340-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="12340-122">-DiskSizeInGB</span></span>
<span data-ttu-id="12340-123">Dimensioni del disco di dati della macchina virtuale in GB.</span><span class="sxs-lookup"><span data-stu-id="12340-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="12340-124">-Lun</span><span class="sxs-lookup"><span data-stu-id="12340-124">-Lun</span></span>
<span data-ttu-id="12340-125">Lun del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-125">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="12340-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="12340-126">-ManagedDiskId</span></span>
<span data-ttu-id="12340-127">ID del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-127">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="12340-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="12340-128">-Name</span></span>
<span data-ttu-id="12340-129">Nome del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="12340-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="12340-130">-SourceImageUri</span></span>
<span data-ttu-id="12340-131">URI dell'immagine di origine del disco operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-131">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="12340-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="12340-132">-StorageAccountType</span></span>
<span data-ttu-id="12340-133">Tipo di account del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="12340-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="12340-134">-VhdUri</span></span>
<span data-ttu-id="12340-135">URI VHD del disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="12340-135">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="12340-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="12340-136">-WriteAccelerator</span></span>
<span data-ttu-id="12340-137">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="12340-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="12340-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12340-138">CommonParameters</span></span>
<span data-ttu-id="12340-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12340-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12340-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12340-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12340-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12340-141">INPUTS</span></span>

### <span data-ttu-id="12340-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="12340-142">System.Int32</span></span>

### <span data-ttu-id="12340-143">System. String</span><span class="sxs-lookup"><span data-stu-id="12340-143">System.String</span></span>

### <span data-ttu-id="12340-144">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="12340-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="12340-145">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12340-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="12340-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12340-146">OUTPUTS</span></span>

### <span data-ttu-id="12340-147">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="12340-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="12340-148">Note</span><span class="sxs-lookup"><span data-stu-id="12340-148">NOTES</span></span>

## <span data-ttu-id="12340-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12340-149">RELATED LINKS</span></span>
