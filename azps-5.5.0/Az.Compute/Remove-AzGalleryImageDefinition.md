---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195014"
---
# <span data-ttu-id="683b1-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="683b1-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="683b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="683b1-102">SYNOPSIS</span></span>
<span data-ttu-id="683b1-103">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="683b1-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="683b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="683b1-104">SYNTAX</span></span>

### <span data-ttu-id="683b1-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="683b1-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683b1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="683b1-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683b1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="683b1-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="683b1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="683b1-108">DESCRIPTION</span></span>
<span data-ttu-id="683b1-109">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="683b1-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="683b1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="683b1-110">EXAMPLES</span></span>

### <span data-ttu-id="683b1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="683b1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="683b1-112">Rimuovere la definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="683b1-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="683b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="683b1-113">PARAMETERS</span></span>

### <span data-ttu-id="683b1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="683b1-114">-AsJob</span></span>
<span data-ttu-id="683b1-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="683b1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="683b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683b1-116">-DefaultProfile</span></span>
<span data-ttu-id="683b1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="683b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683b1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="683b1-118">-Force</span></span>
<span data-ttu-id="683b1-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="683b1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="683b1-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="683b1-120">-GalleryName</span></span>
<span data-ttu-id="683b1-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="683b1-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="683b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="683b1-122">-InputObject</span></span>
<span data-ttu-id="683b1-123">Oggetto definizione immagine raccolta PS</span><span class="sxs-lookup"><span data-stu-id="683b1-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="683b1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="683b1-124">-Name</span></span>
<span data-ttu-id="683b1-125">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="683b1-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="683b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="683b1-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="683b1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="683b1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="683b1-128">-ResourceId</span></span>
<span data-ttu-id="683b1-129">ID risorsa per la definizione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="683b1-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="683b1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="683b1-130">-Confirm</span></span>
<span data-ttu-id="683b1-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683b1-132">-WhatIf</span></span>
<span data-ttu-id="683b1-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="683b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683b1-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="683b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683b1-135">CommonParameters</span></span>
<span data-ttu-id="683b1-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683b1-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="683b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683b1-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="683b1-138">INPUTS</span></span>

### <span data-ttu-id="683b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="683b1-139">System.String</span></span>

### <span data-ttu-id="683b1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="683b1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="683b1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="683b1-141">OUTPUTS</span></span>

### <span data-ttu-id="683b1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="683b1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="683b1-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="683b1-143">NOTES</span></span>

## <span data-ttu-id="683b1-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="683b1-144">RELATED LINKS</span></span>
