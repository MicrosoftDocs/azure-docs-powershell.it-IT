---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: abc9fd93545f229c39dd696a856781ceed748a77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988356"
---
# <span data-ttu-id="a5cd9-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="a5cd9-101">Remove-AzGallery</span></span>

## <span data-ttu-id="a5cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cd9-103">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-103">Delete a gallery.</span></span>

## <span data-ttu-id="a5cd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5cd9-104">SYNTAX</span></span>

### <span data-ttu-id="a5cd9-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="a5cd9-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cd9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a5cd9-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cd9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a5cd9-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5cd9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5cd9-108">DESCRIPTION</span></span>
<span data-ttu-id="a5cd9-109">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-109">Delete a gallery.</span></span>

## <span data-ttu-id="a5cd9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5cd9-110">EXAMPLES</span></span>

### <span data-ttu-id="a5cd9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5cd9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="a5cd9-112">Eliminare la raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-112">Delete the given gallery.</span></span>

## <span data-ttu-id="a5cd9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5cd9-113">PARAMETERS</span></span>

### <span data-ttu-id="a5cd9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5cd9-114">-AsJob</span></span>
<span data-ttu-id="a5cd9-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a5cd9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5cd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cd9-116">-DefaultProfile</span></span>
<span data-ttu-id="a5cd9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5cd9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a5cd9-118">-Force</span></span>
<span data-ttu-id="a5cd9-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5cd9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5cd9-120">-InputObject</span></span>
<span data-ttu-id="a5cd9-121">Oggetto raccolta PS</span><span class="sxs-lookup"><span data-stu-id="a5cd9-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="a5cd9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a5cd9-122">-Name</span></span>
<span data-ttu-id="a5cd9-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="a5cd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5cd9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5cd9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5cd9-126">-ResourceId</span></span>
<span data-ttu-id="a5cd9-127">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="a5cd9-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="a5cd9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5cd9-128">-Confirm</span></span>
<span data-ttu-id="a5cd9-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cd9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cd9-130">-WhatIf</span></span>
<span data-ttu-id="a5cd9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5cd9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cd9-133">CommonParameters</span></span>
<span data-ttu-id="a5cd9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cd9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5cd9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cd9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5cd9-136">INPUTS</span></span>

### <span data-ttu-id="a5cd9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a5cd9-137">System.String</span></span>

### <span data-ttu-id="a5cd9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="a5cd9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="a5cd9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5cd9-139">OUTPUTS</span></span>

### <span data-ttu-id="a5cd9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a5cd9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a5cd9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5cd9-141">NOTES</span></span>

## <span data-ttu-id="a5cd9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5cd9-142">RELATED LINKS</span></span>
