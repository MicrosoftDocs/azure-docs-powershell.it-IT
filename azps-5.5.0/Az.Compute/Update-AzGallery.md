---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181535"
---
# <span data-ttu-id="f2543-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="f2543-101">Update-AzGallery</span></span>

## <span data-ttu-id="f2543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2543-102">SYNOPSIS</span></span>
<span data-ttu-id="f2543-103">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="f2543-103">Update a gallery.</span></span>

## <span data-ttu-id="f2543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2543-104">SYNTAX</span></span>

### <span data-ttu-id="f2543-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="f2543-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2543-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f2543-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2543-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f2543-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2543-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2543-108">DESCRIPTION</span></span>
<span data-ttu-id="f2543-109">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="f2543-109">Update a gallery.</span></span>

## <span data-ttu-id="f2543-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2543-110">EXAMPLES</span></span>

### <span data-ttu-id="f2543-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2543-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="f2543-112">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="f2543-112">Update a gallery.</span></span>

## <span data-ttu-id="f2543-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2543-113">PARAMETERS</span></span>

### <span data-ttu-id="f2543-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2543-114">-AsJob</span></span>
<span data-ttu-id="f2543-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2543-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2543-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2543-116">-DefaultProfile</span></span>
<span data-ttu-id="f2543-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2543-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2543-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2543-118">-Description</span></span>
<span data-ttu-id="f2543-119">Descrizione della risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f2543-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2543-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2543-120">-InputObject</span></span>
<span data-ttu-id="f2543-121">Oggetto raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="f2543-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="f2543-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f2543-122">-Name</span></span>
<span data-ttu-id="f2543-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f2543-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f2543-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2543-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2543-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2543-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2543-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2543-126">-ResourceId</span></span>
<span data-ttu-id="f2543-127">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="f2543-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="f2543-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2543-128">-Tag</span></span>
<span data-ttu-id="f2543-129">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="f2543-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2543-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2543-130">-Confirm</span></span>
<span data-ttu-id="f2543-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2543-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2543-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2543-132">-WhatIf</span></span>
<span data-ttu-id="f2543-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2543-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2543-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2543-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2543-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2543-135">CommonParameters</span></span>
<span data-ttu-id="f2543-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2543-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2543-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2543-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2543-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2543-138">INPUTS</span></span>

### <span data-ttu-id="f2543-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f2543-139">System.String</span></span>

### <span data-ttu-id="f2543-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="f2543-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="f2543-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2543-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2543-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2543-142">OUTPUTS</span></span>

### <span data-ttu-id="f2543-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="f2543-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="f2543-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2543-144">NOTES</span></span>

## <span data-ttu-id="f2543-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2543-145">RELATED LINKS</span></span>
