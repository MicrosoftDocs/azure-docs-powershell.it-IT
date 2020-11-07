---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860034"
---
# <span data-ttu-id="deb02-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="deb02-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="deb02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="deb02-102">SYNOPSIS</span></span>
<span data-ttu-id="deb02-103">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="deb02-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="deb02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="deb02-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="deb02-105">DESCRIPTION</span></span>
<span data-ttu-id="deb02-106">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="deb02-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="deb02-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="deb02-107">EXAMPLES</span></span>

### <span data-ttu-id="deb02-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="deb02-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="deb02-109">Creare un nuovo elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="deb02-109">Create a new gallery item.</span></span>

## <span data-ttu-id="deb02-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="deb02-110">PARAMETERS</span></span>

### <span data-ttu-id="deb02-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="deb02-111">-GalleryItemUri</span></span>
<span data-ttu-id="deb02-112">URI per il file JSON dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="deb02-112">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb02-113">-Force</span><span class="sxs-lookup"><span data-stu-id="deb02-113">-Force</span></span>
<span data-ttu-id="deb02-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="deb02-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb02-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb02-115">-WhatIf</span></span>
<span data-ttu-id="deb02-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deb02-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb02-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deb02-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb02-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="deb02-118">-Confirm</span></span>
<span data-ttu-id="deb02-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb02-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb02-120">CommonParameters</span></span>
<span data-ttu-id="deb02-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb02-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb02-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb02-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="deb02-123">INPUTS</span></span>

## <span data-ttu-id="deb02-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="deb02-124">OUTPUTS</span></span>

### <span data-ttu-id="deb02-125">Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="deb02-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="deb02-126">Note</span><span class="sxs-lookup"><span data-stu-id="deb02-126">NOTES</span></span>

## <span data-ttu-id="deb02-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="deb02-127">RELATED LINKS</span></span>
