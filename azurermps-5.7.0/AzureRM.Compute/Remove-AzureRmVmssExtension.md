---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514448"
---
# <span data-ttu-id="a0928-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a0928-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="a0928-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0928-102">SYNOPSIS</span></span>
<span data-ttu-id="a0928-103">Rimuove un'estensione da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0928-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0928-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0928-104">SYNTAX</span></span>

### <span data-ttu-id="a0928-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0928-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0928-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0928-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0928-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0928-107">DESCRIPTION</span></span>
<span data-ttu-id="a0928-108">Il cmdlet **Remove-AzureRmVmssExtension** consente di rimuovere un'estensione dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a0928-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a0928-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0928-109">EXAMPLES</span></span>

## <span data-ttu-id="a0928-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0928-110">PARAMETERS</span></span>

### <span data-ttu-id="a0928-111">-ID</span><span class="sxs-lookup"><span data-stu-id="a0928-111">-Id</span></span>
<span data-ttu-id="a0928-112">Specifica l'ID dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0928-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0928-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0928-113">-Name</span></span>
<span data-ttu-id="a0928-114">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0928-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a0928-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0928-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a0928-116">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a0928-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a0928-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0928-117">-Confirm</span></span>
<span data-ttu-id="a0928-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0928-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0928-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0928-119">-WhatIf</span></span>
<span data-ttu-id="a0928-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0928-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0928-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0928-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0928-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0928-122">CommonParameters</span></span>
<span data-ttu-id="a0928-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0928-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0928-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0928-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0928-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0928-125">INPUTS</span></span>

### <span data-ttu-id="a0928-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a0928-126">None</span></span>
<span data-ttu-id="a0928-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a0928-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0928-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0928-128">OUTPUTS</span></span>

### <span data-ttu-id="a0928-129">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a0928-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a0928-130">Note</span><span class="sxs-lookup"><span data-stu-id="a0928-130">NOTES</span></span>

## <span data-ttu-id="a0928-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0928-131">RELATED LINKS</span></span>

[<span data-ttu-id="a0928-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a0928-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
