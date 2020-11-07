---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686333"
---
# <span data-ttu-id="875c9-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="875c9-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="875c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="875c9-102">SYNOPSIS</span></span>
<span data-ttu-id="875c9-103">Aggiunge un disco di dati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="875c9-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="875c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="875c9-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="875c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="875c9-105">DESCRIPTION</span></span>
<span data-ttu-id="875c9-106">Il cmdlet **Add-AzureRmVmssDataDisk** aggiunge un disco di dati all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="875c9-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="875c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="875c9-107">EXAMPLES</span></span>

### <span data-ttu-id="875c9-108">Esempio 1: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="875c9-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="875c9-109">Questo comando aggiunge un disco di dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="875c9-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="875c9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="875c9-110">PARAMETERS</span></span>

### <span data-ttu-id="875c9-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="875c9-111">-Caching</span></span>
<span data-ttu-id="875c9-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="875c9-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="875c9-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="875c9-113">-CreateOption</span></span>
<span data-ttu-id="875c9-114">Specifica l'opzione Crea del disco.</span><span class="sxs-lookup"><span data-stu-id="875c9-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="875c9-115">-DiskSizeGB</span></span>
<span data-ttu-id="875c9-116">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="875c9-116">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="875c9-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="875c9-117">-Lun</span></span>
<span data-ttu-id="875c9-118">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="875c9-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="875c9-119">-Name</span></span>
<span data-ttu-id="875c9-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="875c9-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="875c9-121">-StorageAccountType</span></span>
<span data-ttu-id="875c9-122">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="875c9-122">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="875c9-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="875c9-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="875c9-124">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="875c9-124">Specify the VMSS object.</span></span>
<span data-ttu-id="875c9-125">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="875c9-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="875c9-126">-Confirm</span></span>
<span data-ttu-id="875c9-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="875c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875c9-128">-WhatIf</span></span>
<span data-ttu-id="875c9-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="875c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875c9-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="875c9-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875c9-131">CommonParameters</span></span>
<span data-ttu-id="875c9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875c9-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875c9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875c9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="875c9-134">INPUTS</span></span>

### <span data-ttu-id="875c9-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="875c9-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="875c9-136">System. String System. Int32 System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="875c9-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="875c9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="875c9-137">OUTPUTS</span></span>

### <span data-ttu-id="875c9-138">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="875c9-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="875c9-139">Note</span><span class="sxs-lookup"><span data-stu-id="875c9-139">NOTES</span></span>

## <span data-ttu-id="875c9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="875c9-140">RELATED LINKS</span></span>
