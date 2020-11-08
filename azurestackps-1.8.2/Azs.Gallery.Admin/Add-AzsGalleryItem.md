---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030339"
---
# <span data-ttu-id="ae7bb-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="ae7bb-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="ae7bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7bb-103">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="ae7bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae7bb-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae7bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7bb-106">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="ae7bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7bb-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="ae7bb-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="ae7bb-109">Creare un nuovo elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-109">Create a new gallery item.</span></span>

## <span data-ttu-id="ae7bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae7bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ae7bb-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="ae7bb-111">-GalleryItemUri</span></span>
<span data-ttu-id="ae7bb-112">URI per il file JSON dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="ae7bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae7bb-113">-Force</span></span>
<span data-ttu-id="ae7bb-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ae7bb-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7bb-115">-WhatIf</span></span>
<span data-ttu-id="ae7bb-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae7bb-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7bb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae7bb-118">-Confirm</span></span>
<span data-ttu-id="ae7bb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7bb-120">CommonParameters</span></span>
<span data-ttu-id="ae7bb-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7bb-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7bb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7bb-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae7bb-123">INPUTS</span></span>

## <span data-ttu-id="ae7bb-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae7bb-124">OUTPUTS</span></span>

### <span data-ttu-id="ae7bb-125">Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="ae7bb-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="ae7bb-126">Note</span><span class="sxs-lookup"><span data-stu-id="ae7bb-126">NOTES</span></span>

## <span data-ttu-id="ae7bb-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae7bb-127">RELATED LINKS</span></span>
