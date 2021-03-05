---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: ec16e946907e7d2815997cbcfb9cbf1563805039
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975485"
---
# <span data-ttu-id="c411a-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c411a-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="c411a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c411a-102">SYNOPSIS</span></span>
<span data-ttu-id="c411a-103">Aggiunge un disco dati al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="c411a-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="c411a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c411a-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c411a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c411a-105">DESCRIPTION</span></span>
<span data-ttu-id="c411a-106">Il cmdlet **Add-AzVmssDataDisk** aggiunge un disco dati all'istanza VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="c411a-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c411a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c411a-107">EXAMPLES</span></span>

### <span data-ttu-id="c411a-108">Esempio 1: Aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="c411a-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="c411a-109">Questo comando aggiunge un disco dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c411a-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="c411a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c411a-110">PARAMETERS</span></span>

### <span data-ttu-id="c411a-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="c411a-111">-Caching</span></span>
<span data-ttu-id="c411a-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="c411a-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c411a-113">-CreateOption</span></span>
<span data-ttu-id="c411a-114">Specifica l'opzione di creazione del disco.</span><span class="sxs-lookup"><span data-stu-id="c411a-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="c411a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c411a-115">-DefaultProfile</span></span>
<span data-ttu-id="c411a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c411a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c411a-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c411a-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c411a-118">Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="c411a-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c411a-119">Può essere specificato solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c411a-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c411a-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="c411a-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="c411a-121">Specifica l'Read-Write operazioni di I/O al secondo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c411a-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="c411a-122">Deve essere usato solo quando StorageAccountType è UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c411a-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="c411a-123">Se non viene specificato, verrà assegnato un valore predefinito in base a diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="c411a-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="c411a-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="c411a-125">Specifica la larghezza di banda in MB al secondo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c411a-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="c411a-126">Deve essere usato solo quando StorageAccountType è UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c411a-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="c411a-127">Se non viene specificato, verrà assegnato un valore predefinito in base a diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="c411a-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c411a-128">-DiskSizeGB</span></span>
<span data-ttu-id="c411a-129">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="c411a-129">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="c411a-130">-Lun</span></span>
<span data-ttu-id="c411a-131">Specifica il numero di unità logiche del disco.</span><span class="sxs-lookup"><span data-stu-id="c411a-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c411a-132">-Name</span></span>
<span data-ttu-id="c411a-133">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="c411a-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="c411a-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c411a-134">-StorageAccountType</span></span>
<span data-ttu-id="c411a-135">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="c411a-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="c411a-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c411a-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c411a-137">Specificare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c411a-137">Specify the VMSS object.</span></span>
<span data-ttu-id="c411a-138">È possibile usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c411a-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c411a-139">-WriteAccelerator</span></span>
<span data-ttu-id="c411a-140">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="c411a-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="c411a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c411a-141">-Confirm</span></span>
<span data-ttu-id="c411a-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c411a-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c411a-143">-WhatIf</span></span>
<span data-ttu-id="c411a-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c411a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c411a-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c411a-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c411a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c411a-146">CommonParameters</span></span>
<span data-ttu-id="c411a-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c411a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c411a-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c411a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c411a-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="c411a-149">INPUTS</span></span>

### <span data-ttu-id="c411a-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c411a-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c411a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c411a-151">System.String</span></span>

### <span data-ttu-id="c411a-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c411a-152">System.Int32</span></span>

### <span data-ttu-id="c411a-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c411a-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c411a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c411a-154">OUTPUTS</span></span>

### <span data-ttu-id="c411a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c411a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c411a-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="c411a-156">NOTES</span></span>

## <span data-ttu-id="c411a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c411a-157">RELATED LINKS</span></span>
