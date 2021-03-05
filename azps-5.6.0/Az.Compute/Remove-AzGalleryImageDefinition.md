---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: d632f3f9717c706adf2881aa177d9cb7ff2425dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988342"
---
# <span data-ttu-id="10924-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="10924-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="10924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10924-102">SYNOPSIS</span></span>
<span data-ttu-id="10924-103">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10924-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="10924-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10924-104">SYNTAX</span></span>

### <span data-ttu-id="10924-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="10924-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10924-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="10924-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10924-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="10924-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10924-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10924-108">DESCRIPTION</span></span>
<span data-ttu-id="10924-109">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10924-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="10924-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10924-110">EXAMPLES</span></span>

### <span data-ttu-id="10924-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10924-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="10924-112">Rimuovere la definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10924-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="10924-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10924-113">PARAMETERS</span></span>

### <span data-ttu-id="10924-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10924-114">-AsJob</span></span>
<span data-ttu-id="10924-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="10924-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10924-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10924-116">-DefaultProfile</span></span>
<span data-ttu-id="10924-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10924-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10924-118">-Force</span><span class="sxs-lookup"><span data-stu-id="10924-118">-Force</span></span>
<span data-ttu-id="10924-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="10924-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10924-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="10924-120">-GalleryName</span></span>
<span data-ttu-id="10924-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10924-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="10924-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10924-122">-InputObject</span></span>
<span data-ttu-id="10924-123">Oggetto definizione immagine raccolta PS</span><span class="sxs-lookup"><span data-stu-id="10924-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="10924-124">-Name</span><span class="sxs-lookup"><span data-stu-id="10924-124">-Name</span></span>
<span data-ttu-id="10924-125">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="10924-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="10924-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10924-126">-ResourceGroupName</span></span>
<span data-ttu-id="10924-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10924-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="10924-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10924-128">-ResourceId</span></span>
<span data-ttu-id="10924-129">ID risorsa per la definizione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="10924-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="10924-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10924-130">-Confirm</span></span>
<span data-ttu-id="10924-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10924-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10924-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10924-132">-WhatIf</span></span>
<span data-ttu-id="10924-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10924-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10924-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10924-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10924-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10924-135">CommonParameters</span></span>
<span data-ttu-id="10924-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10924-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10924-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10924-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10924-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="10924-138">INPUTS</span></span>

### <span data-ttu-id="10924-139">System.String</span><span class="sxs-lookup"><span data-stu-id="10924-139">System.String</span></span>

### <span data-ttu-id="10924-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="10924-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="10924-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10924-141">OUTPUTS</span></span>

### <span data-ttu-id="10924-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="10924-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="10924-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="10924-143">NOTES</span></span>

## <span data-ttu-id="10924-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10924-144">RELATED LINKS</span></span>
