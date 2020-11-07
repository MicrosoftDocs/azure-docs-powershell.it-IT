---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685495"
---
# <span data-ttu-id="3571c-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="3571c-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="3571c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3571c-102">SYNOPSIS</span></span>
<span data-ttu-id="3571c-103">Rimuove un disco di dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="3571c-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3571c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3571c-104">SYNTAX</span></span>

### <span data-ttu-id="3571c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3571c-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3571c-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="3571c-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3571c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3571c-107">DESCRIPTION</span></span>
<span data-ttu-id="3571c-108">Il cmdlet **Remove-AzureRmVmssDataDisk** rimuove un disco di dati dall'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="3571c-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3571c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3571c-109">EXAMPLES</span></span>

### <span data-ttu-id="3571c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3571c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="3571c-111">Questo comando rimuove il disco di dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3571c-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="3571c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3571c-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="3571c-113">Questo comando rimuove il disco di dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3571c-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="3571c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3571c-114">PARAMETERS</span></span>

### <span data-ttu-id="3571c-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="3571c-115">-Lun</span></span>
<span data-ttu-id="3571c-116">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="3571c-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3571c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3571c-117">-Name</span></span>
<span data-ttu-id="3571c-118">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="3571c-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3571c-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3571c-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3571c-120">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3571c-120">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="3571c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3571c-121">-Confirm</span></span>
<span data-ttu-id="3571c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3571c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3571c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3571c-123">-WhatIf</span></span>
<span data-ttu-id="3571c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3571c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3571c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3571c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3571c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3571c-126">CommonParameters</span></span>
<span data-ttu-id="3571c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3571c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3571c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3571c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3571c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3571c-129">INPUTS</span></span>

### <span data-ttu-id="3571c-130">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3571c-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="3571c-131">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3571c-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3571c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3571c-132">OUTPUTS</span></span>

### <span data-ttu-id="3571c-133">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3571c-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="3571c-134">Note</span><span class="sxs-lookup"><span data-stu-id="3571c-134">NOTES</span></span>

## <span data-ttu-id="3571c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3571c-135">RELATED LINKS</span></span>

