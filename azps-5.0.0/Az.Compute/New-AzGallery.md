---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199705"
---
# <span data-ttu-id="212ba-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="212ba-101">New-AzGallery</span></span>

## <span data-ttu-id="212ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="212ba-102">SYNOPSIS</span></span>
<span data-ttu-id="212ba-103">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="212ba-103">Create a gallery.</span></span>

## <span data-ttu-id="212ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="212ba-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="212ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="212ba-105">DESCRIPTION</span></span>
<span data-ttu-id="212ba-106">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="212ba-106">Create a gallery.</span></span>

## <span data-ttu-id="212ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="212ba-107">EXAMPLES</span></span>

### <span data-ttu-id="212ba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="212ba-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="212ba-109">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="212ba-109">Create a gallery.</span></span>

## <span data-ttu-id="212ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="212ba-110">PARAMETERS</span></span>

### <span data-ttu-id="212ba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="212ba-111">-AsJob</span></span>
<span data-ttu-id="212ba-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="212ba-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="212ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212ba-113">-DefaultProfile</span></span>
<span data-ttu-id="212ba-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="212ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="212ba-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="212ba-115">-Description</span></span>
<span data-ttu-id="212ba-116">Descrizione della risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="212ba-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="212ba-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="212ba-117">-Location</span></span>
<span data-ttu-id="212ba-118">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="212ba-118">Resource location</span></span>

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

### <span data-ttu-id="212ba-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="212ba-119">-Name</span></span>
<span data-ttu-id="212ba-120">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="212ba-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="212ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="212ba-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="212ba-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="212ba-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="212ba-123">-Tag</span></span>
<span data-ttu-id="212ba-124">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="212ba-124">Resource tags</span></span>

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

### <span data-ttu-id="212ba-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="212ba-125">-Confirm</span></span>
<span data-ttu-id="212ba-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="212ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212ba-127">-WhatIf</span></span>
<span data-ttu-id="212ba-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="212ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212ba-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="212ba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212ba-130">CommonParameters</span></span>
<span data-ttu-id="212ba-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212ba-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="212ba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212ba-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="212ba-133">INPUTS</span></span>

### <span data-ttu-id="212ba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="212ba-134">System.String</span></span>

### <span data-ttu-id="212ba-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="212ba-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="212ba-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="212ba-136">OUTPUTS</span></span>

### <span data-ttu-id="212ba-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="212ba-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="212ba-138">Note</span><span class="sxs-lookup"><span data-stu-id="212ba-138">NOTES</span></span>

## <span data-ttu-id="212ba-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="212ba-139">RELATED LINKS</span></span>
