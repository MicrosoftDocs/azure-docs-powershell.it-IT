---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491145"
---
# <span data-ttu-id="bda05-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="bda05-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="bda05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bda05-102">SYNOPSIS</span></span>
<span data-ttu-id="bda05-103">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bda05-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="bda05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bda05-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bda05-105">DESCRIPTION</span></span>
<span data-ttu-id="bda05-106">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bda05-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="bda05-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bda05-107">EXAMPLES</span></span>

### <span data-ttu-id="bda05-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bda05-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="bda05-109">Creare un nuovo elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bda05-109">Create a new gallery item.</span></span>

## <span data-ttu-id="bda05-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bda05-110">PARAMETERS</span></span>

### <span data-ttu-id="bda05-111">-Force</span><span class="sxs-lookup"><span data-stu-id="bda05-111">-Force</span></span>
<span data-ttu-id="bda05-112">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bda05-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bda05-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="bda05-113">-GalleryItemUri</span></span>
<span data-ttu-id="bda05-114">URI per il file JSON dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bda05-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="bda05-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bda05-115">-Confirm</span></span>
<span data-ttu-id="bda05-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bda05-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda05-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda05-117">-WhatIf</span></span>
<span data-ttu-id="bda05-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bda05-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda05-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bda05-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bda05-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda05-120">CommonParameters</span></span>
<span data-ttu-id="bda05-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda05-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda05-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda05-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda05-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bda05-123">INPUTS</span></span>

## <span data-ttu-id="bda05-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bda05-124">OUTPUTS</span></span>

### <span data-ttu-id="bda05-125">Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="bda05-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="bda05-126">Note</span><span class="sxs-lookup"><span data-stu-id="bda05-126">NOTES</span></span>

## <span data-ttu-id="bda05-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bda05-127">RELATED LINKS</span></span>

