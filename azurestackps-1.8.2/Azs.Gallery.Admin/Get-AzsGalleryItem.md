---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030283"
---
# <span data-ttu-id="4818f-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="4818f-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="4818f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4818f-102">SYNOPSIS</span></span>
<span data-ttu-id="4818f-103">Elenca gli elementi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4818f-103">Lists gallery items.</span></span>

## <span data-ttu-id="4818f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4818f-104">SYNTAX</span></span>

### <span data-ttu-id="4818f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4818f-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="4818f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4818f-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="4818f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4818f-107">DESCRIPTION</span></span>
<span data-ttu-id="4818f-108">Ottenere un elenco di elementi della raccolta disponibili in Azure stack Marketplace</span><span class="sxs-lookup"><span data-stu-id="4818f-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="4818f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4818f-109">EXAMPLES</span></span>

### <span data-ttu-id="4818f-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="4818f-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="4818f-111">Elementi della raccolta elenchi.</span><span class="sxs-lookup"><span data-stu-id="4818f-111">List gallery items.</span></span>

### <span data-ttu-id="4818f-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="4818f-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="4818f-113">Ottenere un elemento della raccolta in base al nome.</span><span class="sxs-lookup"><span data-stu-id="4818f-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="4818f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4818f-114">PARAMETERS</span></span>

### <span data-ttu-id="4818f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4818f-115">-Name</span></span>
<span data-ttu-id="4818f-116">Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4818f-116">Identity of the gallery item.</span></span>
<span data-ttu-id="4818f-117">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="4818f-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4818f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4818f-118">CommonParameters</span></span>
<span data-ttu-id="4818f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4818f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4818f-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4818f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4818f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4818f-121">INPUTS</span></span>

## <span data-ttu-id="4818f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4818f-122">OUTPUTS</span></span>

### <span data-ttu-id="4818f-123">Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="4818f-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="4818f-124">Note</span><span class="sxs-lookup"><span data-stu-id="4818f-124">NOTES</span></span>

## <span data-ttu-id="4818f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4818f-125">RELATED LINKS</span></span>
