---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866155"
---
# <span data-ttu-id="46ee0-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="46ee0-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="46ee0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="46ee0-103">Aggiunge un disco di dati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="46ee0-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46ee0-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ee0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="46ee0-106">Il cmdlet **Add-AzureRmVmssDataDisk** aggiunge un disco di dati all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="46ee0-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="46ee0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="46ee0-108">Esempio 1: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="46ee0-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="46ee0-109">Questo comando aggiunge un disco di dati vuoto all'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="46ee0-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="46ee0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="46ee0-111">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="46ee0-111">-Caching</span></span>
<span data-ttu-id="46ee0-112">Specifica il tipo di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="46ee0-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="46ee0-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="46ee0-113">-CreateOption</span></span>
<span data-ttu-id="46ee0-114">Specifica l'opzione Crea del disco.</span><span class="sxs-lookup"><span data-stu-id="46ee0-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="46ee0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ee0-115">-DefaultProfile</span></span>
<span data-ttu-id="46ee0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46ee0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ee0-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="46ee0-117">-DiskSizeGB</span></span>
<span data-ttu-id="46ee0-118">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="46ee0-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="46ee0-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="46ee0-119">-Lun</span></span>
<span data-ttu-id="46ee0-120">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="46ee0-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="46ee0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="46ee0-121">-Name</span></span>
<span data-ttu-id="46ee0-122">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="46ee0-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="46ee0-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="46ee0-123">-StorageAccountType</span></span>
<span data-ttu-id="46ee0-124">Specifica il tipo di account di archiviazione del disco.</span><span class="sxs-lookup"><span data-stu-id="46ee0-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="46ee0-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46ee0-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="46ee0-126">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="46ee0-126">Specify the VMSS object.</span></span>
<span data-ttu-id="46ee0-127">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46ee0-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46ee0-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="46ee0-128">-WriteAccelerator</span></span>
<span data-ttu-id="46ee0-129">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="46ee0-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="46ee0-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46ee0-130">-Confirm</span></span>
<span data-ttu-id="46ee0-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46ee0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ee0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ee0-132">-WhatIf</span></span>
<span data-ttu-id="46ee0-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ee0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ee0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ee0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ee0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ee0-135">CommonParameters</span></span>
<span data-ttu-id="46ee0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ee0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ee0-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ee0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ee0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46ee0-138">INPUTS</span></span>

### <span data-ttu-id="46ee0-139">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46ee0-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="46ee0-140">System. String System. Int32 System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="46ee0-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="46ee0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46ee0-141">OUTPUTS</span></span>

### <span data-ttu-id="46ee0-142">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46ee0-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="46ee0-143">Note</span><span class="sxs-lookup"><span data-stu-id="46ee0-143">NOTES</span></span>

## <span data-ttu-id="46ee0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46ee0-144">RELATED LINKS</span></span>

