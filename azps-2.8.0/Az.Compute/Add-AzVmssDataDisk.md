---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 032c38c3fcc3b09286b795fd3e0efba85e076807
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675471"
---
# <span data-ttu-id="fa9ba-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="fa9ba-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="fa9ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9ba-103">Aggiunge un disco di dati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="fa9ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa9ba-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa9ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9ba-106">Il cmdlet **Add-AzVmssDataDisk** aggiunge un disco di dati all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fa9ba-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="fa9ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa9ba-107">EXAMPLES</span></span>

### <span data-ttu-id="fa9ba-108">Esempio 1: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="fa9ba-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="fa9ba-109">Questo comando aggiunge un disco di dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="fa9ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa9ba-110">PARAMETERS</span></span>

### <span data-ttu-id="fa9ba-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="fa9ba-111">-Caching</span></span>
<span data-ttu-id="fa9ba-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="fa9ba-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="fa9ba-113">-CreateOption</span></span>
<span data-ttu-id="fa9ba-114">Specifica l'opzione Crea del disco.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="fa9ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9ba-115">-DefaultProfile</span></span>
<span data-ttu-id="fa9ba-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa9ba-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="fa9ba-117">-DiskSizeGB</span></span>
<span data-ttu-id="fa9ba-118">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="fa9ba-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="fa9ba-119">-Lun</span></span>
<span data-ttu-id="fa9ba-120">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="fa9ba-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa9ba-121">-Name</span></span>
<span data-ttu-id="fa9ba-122">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="fa9ba-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fa9ba-123">-StorageAccountType</span></span>
<span data-ttu-id="fa9ba-124">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="fa9ba-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fa9ba-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fa9ba-126">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-126">Specify the VMSS object.</span></span>
<span data-ttu-id="fa9ba-127">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="fa9ba-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="fa9ba-128">-WriteAccelerator</span></span>
<span data-ttu-id="fa9ba-129">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="fa9ba-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa9ba-130">-Confirm</span></span>
<span data-ttu-id="fa9ba-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9ba-132">-WhatIf</span></span>
<span data-ttu-id="fa9ba-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9ba-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9ba-135">CommonParameters</span></span>
<span data-ttu-id="fa9ba-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9ba-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa9ba-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9ba-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa9ba-138">INPUTS</span></span>

### <span data-ttu-id="fa9ba-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fa9ba-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fa9ba-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fa9ba-140">System.String</span></span>

### <span data-ttu-id="fa9ba-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fa9ba-141">System.Int32</span></span>

### <span data-ttu-id="fa9ba-142">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fa9ba-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="fa9ba-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa9ba-143">OUTPUTS</span></span>

### <span data-ttu-id="fa9ba-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fa9ba-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fa9ba-145">Note</span><span class="sxs-lookup"><span data-stu-id="fa9ba-145">NOTES</span></span>

## <span data-ttu-id="fa9ba-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa9ba-146">RELATED LINKS</span></span>