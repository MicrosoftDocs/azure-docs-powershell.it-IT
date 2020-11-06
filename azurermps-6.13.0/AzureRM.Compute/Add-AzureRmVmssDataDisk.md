---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 0ef680f60f48451e5d5dd9bff730cbfe4ebc9aae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517503"
---
# <span data-ttu-id="b6870-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b6870-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="b6870-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6870-102">SYNOPSIS</span></span>
<span data-ttu-id="b6870-103">Aggiunge un disco di dati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6870-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6870-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6870-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6870-105">DESCRIPTION</span></span>
<span data-ttu-id="b6870-106">Il cmdlet **Add-AzureRmVmssDataDisk** aggiunge un disco di dati all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b6870-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b6870-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6870-107">EXAMPLES</span></span>

### <span data-ttu-id="b6870-108">Esempio 1: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="b6870-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="b6870-109">Questo comando aggiunge un disco di dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6870-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="b6870-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6870-110">PARAMETERS</span></span>

### <span data-ttu-id="b6870-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="b6870-111">-Caching</span></span>
<span data-ttu-id="b6870-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="b6870-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="b6870-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b6870-113">-CreateOption</span></span>
<span data-ttu-id="b6870-114">Specifica l'opzione Crea del disco.</span><span class="sxs-lookup"><span data-stu-id="b6870-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="b6870-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6870-115">-DefaultProfile</span></span>
<span data-ttu-id="b6870-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6870-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6870-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b6870-117">-DiskSizeGB</span></span>
<span data-ttu-id="b6870-118">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="b6870-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b6870-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="b6870-119">-Lun</span></span>
<span data-ttu-id="b6870-120">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="b6870-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="b6870-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6870-121">-Name</span></span>
<span data-ttu-id="b6870-122">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="b6870-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="b6870-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b6870-123">-StorageAccountType</span></span>
<span data-ttu-id="b6870-124">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="b6870-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="b6870-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b6870-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b6870-126">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6870-126">Specify the VMSS object.</span></span>
<span data-ttu-id="b6870-127">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6870-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b6870-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b6870-128">-WriteAccelerator</span></span>
<span data-ttu-id="b6870-129">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="b6870-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="b6870-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6870-130">-Confirm</span></span>
<span data-ttu-id="b6870-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6870-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6870-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6870-132">-WhatIf</span></span>
<span data-ttu-id="b6870-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6870-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6870-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6870-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6870-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6870-135">CommonParameters</span></span>
<span data-ttu-id="b6870-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6870-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6870-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6870-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6870-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6870-138">INPUTS</span></span>

### <span data-ttu-id="b6870-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b6870-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b6870-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b6870-140">System.String</span></span>

### <span data-ttu-id="b6870-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b6870-141">System.Int32</span></span>

### <span data-ttu-id="b6870-142">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6870-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b6870-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6870-143">OUTPUTS</span></span>

### <span data-ttu-id="b6870-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b6870-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b6870-145">Note</span><span class="sxs-lookup"><span data-stu-id="b6870-145">NOTES</span></span>

## <span data-ttu-id="b6870-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6870-146">RELATED LINKS</span></span>
