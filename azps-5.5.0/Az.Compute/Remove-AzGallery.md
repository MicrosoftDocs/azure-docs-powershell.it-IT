---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210011"
---
# <span data-ttu-id="e34cc-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="e34cc-101">Remove-AzGallery</span></span>

## <span data-ttu-id="e34cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e34cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e34cc-103">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="e34cc-103">Delete a gallery.</span></span>

## <span data-ttu-id="e34cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e34cc-104">SYNTAX</span></span>

### <span data-ttu-id="e34cc-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="e34cc-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e34cc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e34cc-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e34cc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e34cc-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e34cc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e34cc-108">DESCRIPTION</span></span>
<span data-ttu-id="e34cc-109">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="e34cc-109">Delete a gallery.</span></span>

## <span data-ttu-id="e34cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e34cc-110">EXAMPLES</span></span>

### <span data-ttu-id="e34cc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e34cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="e34cc-112">Eliminare la raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="e34cc-112">Delete the given gallery.</span></span>

## <span data-ttu-id="e34cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e34cc-113">PARAMETERS</span></span>

### <span data-ttu-id="e34cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e34cc-114">-AsJob</span></span>
<span data-ttu-id="e34cc-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e34cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e34cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e34cc-116">-DefaultProfile</span></span>
<span data-ttu-id="e34cc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e34cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e34cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e34cc-118">-Force</span></span>
<span data-ttu-id="e34cc-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="e34cc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e34cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e34cc-120">-InputObject</span></span>
<span data-ttu-id="e34cc-121">Oggetto raccolta PS</span><span class="sxs-lookup"><span data-stu-id="e34cc-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e34cc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e34cc-122">-Name</span></span>
<span data-ttu-id="e34cc-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e34cc-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e34cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="e34cc-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e34cc-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e34cc-126">-ResourceId</span></span>
<span data-ttu-id="e34cc-127">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="e34cc-127">The resource Id for the gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34cc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e34cc-128">-Confirm</span></span>
<span data-ttu-id="e34cc-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e34cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e34cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e34cc-130">-WhatIf</span></span>
<span data-ttu-id="e34cc-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e34cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e34cc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e34cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e34cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34cc-133">CommonParameters</span></span>
<span data-ttu-id="e34cc-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e34cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34cc-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e34cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34cc-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e34cc-136">INPUTS</span></span>

### <span data-ttu-id="e34cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e34cc-137">System.String</span></span>

### <span data-ttu-id="e34cc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="e34cc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="e34cc-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e34cc-139">OUTPUTS</span></span>

### <span data-ttu-id="e34cc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e34cc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e34cc-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e34cc-141">NOTES</span></span>

## <span data-ttu-id="e34cc-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e34cc-142">RELATED LINKS</span></span>
