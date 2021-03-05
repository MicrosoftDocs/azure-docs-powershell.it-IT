---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 47ba904378ed8f58da29876d5835ca43bb8a7a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959693"
---
# <span data-ttu-id="44c6b-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="44c6b-101">New-AzGallery</span></span>

## <span data-ttu-id="44c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="44c6b-103">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="44c6b-103">Create a gallery.</span></span>

## <span data-ttu-id="44c6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44c6b-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44c6b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="44c6b-106">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="44c6b-106">Create a gallery.</span></span>

## <span data-ttu-id="44c6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="44c6b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44c6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="44c6b-109">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="44c6b-109">Create a gallery.</span></span>

## <span data-ttu-id="44c6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44c6b-110">PARAMETERS</span></span>

### <span data-ttu-id="44c6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44c6b-111">-AsJob</span></span>
<span data-ttu-id="44c6b-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44c6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44c6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c6b-113">-DefaultProfile</span></span>
<span data-ttu-id="44c6b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44c6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c6b-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="44c6b-115">-Description</span></span>
<span data-ttu-id="44c6b-116">Descrizione della risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="44c6b-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="44c6b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="44c6b-117">-Location</span></span>
<span data-ttu-id="44c6b-118">Luogo della risorsa</span><span class="sxs-lookup"><span data-stu-id="44c6b-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c6b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44c6b-119">-Name</span></span>
<span data-ttu-id="44c6b-120">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="44c6b-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c6b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c6b-121">-ResourceGroupName</span></span>
<span data-ttu-id="44c6b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44c6b-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c6b-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="44c6b-123">-Tag</span></span>
<span data-ttu-id="44c6b-124">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="44c6b-124">Resource tags</span></span>

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

### <span data-ttu-id="44c6b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44c6b-125">-Confirm</span></span>
<span data-ttu-id="44c6b-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c6b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c6b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c6b-127">-WhatIf</span></span>
<span data-ttu-id="44c6b-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44c6b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c6b-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44c6b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c6b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c6b-130">CommonParameters</span></span>
<span data-ttu-id="44c6b-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c6b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c6b-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44c6b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c6b-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="44c6b-133">INPUTS</span></span>

### <span data-ttu-id="44c6b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="44c6b-134">System.String</span></span>

### <span data-ttu-id="44c6b-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="44c6b-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="44c6b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44c6b-136">OUTPUTS</span></span>

### <span data-ttu-id="44c6b-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="44c6b-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="44c6b-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="44c6b-138">NOTES</span></span>

## <span data-ttu-id="44c6b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44c6b-139">RELATED LINKS</span></span>
