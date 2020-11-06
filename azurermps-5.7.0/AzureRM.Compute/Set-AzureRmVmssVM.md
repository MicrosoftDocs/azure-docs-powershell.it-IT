---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516839"
---
# <span data-ttu-id="8e8e3-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="8e8e3-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="8e8e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8e3-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e8e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e8e3-104">SYNTAX</span></span>

### <span data-ttu-id="8e8e3-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e8e3-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8e3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8e8e3-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e8e3-107">DESCRIPTION</span></span>
<span data-ttu-id="8e8e3-108">Il cmdlet **set-AzureRmVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="8e8e3-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8e8e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e8e3-109">EXAMPLES</span></span>

## <span data-ttu-id="8e8e3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e8e3-110">PARAMETERS</span></span>

### <span data-ttu-id="8e8e3-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8e8e3-111">-InstanceId</span></span>
<span data-ttu-id="8e8e3-112">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e3-113">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="8e8e3-113">-Reimage</span></span>
<span data-ttu-id="8e8e3-114">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e3-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="8e8e3-115">-ReimageAll</span></span>
<span data-ttu-id="8e8e3-116">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e8e3-118">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e3-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8e8e3-119">-VMScaleSetName</span></span>
<span data-ttu-id="8e8e3-120">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e3-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e8e3-121">-Confirm</span></span>
<span data-ttu-id="8e8e3-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8e3-123">-WhatIf</span></span>
<span data-ttu-id="8e8e3-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e8e3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8e3-126">CommonParameters</span></span>
<span data-ttu-id="8e8e3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8e3-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e8e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8e3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e8e3-129">INPUTS</span></span>

### <span data-ttu-id="8e8e3-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8e8e3-130">None</span></span>
<span data-ttu-id="8e8e3-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8e8e3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e8e3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e8e3-132">OUTPUTS</span></span>

## <span data-ttu-id="8e8e3-133">Note</span><span class="sxs-lookup"><span data-stu-id="8e8e3-133">NOTES</span></span>

## <span data-ttu-id="8e8e3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e8e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e8e3-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="8e8e3-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
