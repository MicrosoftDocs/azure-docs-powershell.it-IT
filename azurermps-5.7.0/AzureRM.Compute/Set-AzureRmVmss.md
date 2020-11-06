---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516855"
---
# <span data-ttu-id="295e5-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="295e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="295e5-102">SYNOPSIS</span></span>
<span data-ttu-id="295e5-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="295e5-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="295e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="295e5-104">SYNTAX</span></span>

### <span data-ttu-id="295e5-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="295e5-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="295e5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="295e5-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="295e5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="295e5-107">DESCRIPTION</span></span>
<span data-ttu-id="295e5-108">Il cmdlet **set-AzureRmVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="295e5-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="295e5-109">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="295e5-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="295e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="295e5-110">EXAMPLES</span></span>

### <span data-ttu-id="295e5-111">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="295e5-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="295e5-112">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="295e5-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="295e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="295e5-113">PARAMETERS</span></span>

### <span data-ttu-id="295e5-114">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="295e5-114">-Reimage</span></span>
<span data-ttu-id="295e5-115">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="295e5-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e5-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="295e5-116">-ReimageAll</span></span>
<span data-ttu-id="295e5-117">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="295e5-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295e5-118">-ResourceGroupName</span></span>
<span data-ttu-id="295e5-119">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="295e5-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="295e5-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="295e5-120">-VMScaleSetName</span></span>
<span data-ttu-id="295e5-121">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="295e5-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="295e5-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="295e5-122">-Confirm</span></span>
<span data-ttu-id="295e5-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295e5-124">-WhatIf</span></span>
<span data-ttu-id="295e5-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="295e5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="295e5-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="295e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295e5-127">CommonParameters</span></span>
<span data-ttu-id="295e5-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295e5-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="295e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295e5-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="295e5-130">INPUTS</span></span>

### <span data-ttu-id="295e5-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="295e5-131">None</span></span>
<span data-ttu-id="295e5-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="295e5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="295e5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="295e5-133">OUTPUTS</span></span>

### <span data-ttu-id="295e5-134">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="295e5-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="295e5-135">Note</span><span class="sxs-lookup"><span data-stu-id="295e5-135">NOTES</span></span>

## <span data-ttu-id="295e5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="295e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="295e5-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="295e5-138">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="295e5-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="295e5-140">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="295e5-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="295e5-142">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="295e5-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="295e5-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


