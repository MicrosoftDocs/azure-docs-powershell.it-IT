---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 43ff179aa11c3cf9bf4b22f8b5c938a473a9d8c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684780"
---
# <span data-ttu-id="ad4bc-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="ad4bc-101">New-AzGallery</span></span>

## <span data-ttu-id="ad4bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4bc-103">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-103">Create a gallery.</span></span>

## <span data-ttu-id="ad4bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad4bc-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad4bc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4bc-106">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-106">Create a gallery.</span></span>

## <span data-ttu-id="ad4bc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad4bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4bc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad4bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="ad4bc-109">Creare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-109">Create a gallery.</span></span>

## <span data-ttu-id="ad4bc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad4bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ad4bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad4bc-111">-AsJob</span></span>
<span data-ttu-id="ad4bc-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad4bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad4bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ad4bc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad4bc-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad4bc-115">-Description</span></span>
<span data-ttu-id="ad4bc-116">Descrizione della risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="ad4bc-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad4bc-117">-Location</span></span>
<span data-ttu-id="ad4bc-118">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad4bc-118">Resource location</span></span>

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

### <span data-ttu-id="ad4bc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad4bc-119">-Name</span></span>
<span data-ttu-id="ad4bc-120">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="ad4bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad4bc-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad4bc-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad4bc-123">-Tag</span></span>
<span data-ttu-id="ad4bc-124">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad4bc-124">Resource tags</span></span>

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

### <span data-ttu-id="ad4bc-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad4bc-125">-Confirm</span></span>
<span data-ttu-id="ad4bc-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4bc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4bc-127">-WhatIf</span></span>
<span data-ttu-id="ad4bc-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4bc-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4bc-130">CommonParameters</span></span>
<span data-ttu-id="ad4bc-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4bc-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4bc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4bc-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad4bc-133">INPUTS</span></span>

### <span data-ttu-id="ad4bc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ad4bc-134">System.String</span></span>

### <span data-ttu-id="ad4bc-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad4bc-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad4bc-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad4bc-136">OUTPUTS</span></span>

### <span data-ttu-id="ad4bc-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ad4bc-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ad4bc-138">Note</span><span class="sxs-lookup"><span data-stu-id="ad4bc-138">NOTES</span></span>

## <span data-ttu-id="ad4bc-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad4bc-139">RELATED LINKS</span></span>
