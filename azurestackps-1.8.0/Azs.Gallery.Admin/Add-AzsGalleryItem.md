---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859137"
---
# <span data-ttu-id="63b6b-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="63b6b-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="63b6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="63b6b-103">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63b6b-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="63b6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63b6b-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63b6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="63b6b-106">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63b6b-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="63b6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="63b6b-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="63b6b-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="63b6b-109">Creare un nuovo elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="63b6b-109">Create a new gallery item.</span></span>

## <span data-ttu-id="63b6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="63b6b-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="63b6b-111">-GalleryItemUri</span></span>
<span data-ttu-id="63b6b-112">URI per il file JSON dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="63b6b-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="63b6b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="63b6b-113">-Force</span></span>
<span data-ttu-id="63b6b-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="63b6b-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="63b6b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63b6b-115">-WhatIf</span></span>
<span data-ttu-id="63b6b-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63b6b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63b6b-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63b6b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63b6b-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63b6b-118">-Confirm</span></span>
<span data-ttu-id="63b6b-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63b6b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63b6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b6b-120">CommonParameters</span></span>
<span data-ttu-id="63b6b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63b6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b6b-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63b6b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b6b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63b6b-123">INPUTS</span></span>

## <span data-ttu-id="63b6b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63b6b-124">OUTPUTS</span></span>

### <span data-ttu-id="63b6b-125">Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="63b6b-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="63b6b-126">Note</span><span class="sxs-lookup"><span data-stu-id="63b6b-126">NOTES</span></span>

## <span data-ttu-id="63b6b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63b6b-127">RELATED LINKS</span></span>
