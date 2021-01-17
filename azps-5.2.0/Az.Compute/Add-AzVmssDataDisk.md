---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353251"
---
# <span data-ttu-id="d040c-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d040c-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="d040c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d040c-102">SYNOPSIS</span></span>
<span data-ttu-id="d040c-103">Aggiunge un disco di dati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="d040c-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="d040c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d040c-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d040c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d040c-105">DESCRIPTION</span></span>
<span data-ttu-id="d040c-106">Il cmdlet **Add-AzVmssDataDisk** aggiunge un disco di dati all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d040c-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d040c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d040c-107">EXAMPLES</span></span>

### <span data-ttu-id="d040c-108">Esempio 1: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="d040c-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="d040c-109">Questo comando aggiunge un disco di dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d040c-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="d040c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d040c-110">PARAMETERS</span></span>

### <span data-ttu-id="d040c-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="d040c-111">-Caching</span></span>
<span data-ttu-id="d040c-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="d040c-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="d040c-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d040c-113">-CreateOption</span></span>
<span data-ttu-id="d040c-114">Specifica l'opzione Crea del disco.</span><span class="sxs-lookup"><span data-stu-id="d040c-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="d040c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d040c-115">-DefaultProfile</span></span>
<span data-ttu-id="d040c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d040c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d040c-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d040c-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d040c-118">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="d040c-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d040c-119">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="d040c-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d040c-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="d040c-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="d040c-121">Specifica l'Read-Write IOPS per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="d040c-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="d040c-122">Deve essere usato solo quando StorageAccountType è UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="d040c-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="d040c-123">Se non specificato, verrà assegnato un valore predefinito basato su diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="d040c-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="d040c-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="d040c-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="d040c-125">Specifica la larghezza di banda in MB al secondo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="d040c-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="d040c-126">Deve essere usato solo quando StorageAccountType è UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="d040c-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="d040c-127">Se non specificato, verrà assegnato un valore predefinito basato su diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="d040c-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="d040c-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d040c-128">-DiskSizeGB</span></span>
<span data-ttu-id="d040c-129">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="d040c-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="d040c-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="d040c-130">-Lun</span></span>
<span data-ttu-id="d040c-131">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="d040c-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="d040c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="d040c-132">-Name</span></span>
<span data-ttu-id="d040c-133">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="d040c-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="d040c-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d040c-134">-StorageAccountType</span></span>
<span data-ttu-id="d040c-135">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="d040c-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="d040c-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d040c-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d040c-137">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d040c-137">Specify the VMSS object.</span></span>
<span data-ttu-id="d040c-138">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d040c-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d040c-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d040c-139">-WriteAccelerator</span></span>
<span data-ttu-id="d040c-140">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="d040c-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="d040c-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d040c-141">-Confirm</span></span>
<span data-ttu-id="d040c-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d040c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d040c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d040c-143">-WhatIf</span></span>
<span data-ttu-id="d040c-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d040c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d040c-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d040c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d040c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d040c-146">CommonParameters</span></span>
<span data-ttu-id="d040c-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d040c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d040c-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d040c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d040c-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d040c-149">INPUTS</span></span>

### <span data-ttu-id="d040c-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d040c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d040c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d040c-151">System.String</span></span>

### <span data-ttu-id="d040c-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d040c-152">System.Int32</span></span>

### <span data-ttu-id="d040c-153">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d040c-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d040c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d040c-154">OUTPUTS</span></span>

### <span data-ttu-id="d040c-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d040c-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d040c-156">Note</span><span class="sxs-lookup"><span data-stu-id="d040c-156">NOTES</span></span>

## <span data-ttu-id="d040c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d040c-157">RELATED LINKS</span></span>
