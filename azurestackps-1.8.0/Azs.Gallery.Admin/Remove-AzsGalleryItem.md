---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859130"
---
# <span data-ttu-id="02842-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="02842-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="02842-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02842-102">SYNOPSIS</span></span>
<span data-ttu-id="02842-103">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="02842-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="02842-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02842-104">SYNTAX</span></span>

### <span data-ttu-id="02842-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02842-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02842-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="02842-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02842-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02842-107">DESCRIPTION</span></span>
<span data-ttu-id="02842-108">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="02842-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="02842-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02842-109">EXAMPLES</span></span>

### <span data-ttu-id="02842-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="02842-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="02842-111">Eliminare un elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="02842-111">Delete a gallery item.</span></span>

## <span data-ttu-id="02842-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02842-112">PARAMETERS</span></span>

### <span data-ttu-id="02842-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="02842-113">-Name</span></span>
<span data-ttu-id="02842-114">Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="02842-114">Identity of the gallery item.</span></span>
<span data-ttu-id="02842-115">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="02842-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02842-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02842-116">-ResourceId</span></span>
<span data-ttu-id="02842-117">ID risorsa di Azure completo.</span><span class="sxs-lookup"><span data-stu-id="02842-117">Fully qualified Azure resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02842-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02842-118">-Force</span></span>
<span data-ttu-id="02842-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="02842-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="02842-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02842-120">-WhatIf</span></span>
<span data-ttu-id="02842-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02842-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02842-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02842-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02842-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02842-123">-Confirm</span></span>
<span data-ttu-id="02842-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02842-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02842-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02842-125">CommonParameters</span></span>
<span data-ttu-id="02842-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02842-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02842-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02842-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02842-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02842-128">INPUTS</span></span>

## <span data-ttu-id="02842-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02842-129">OUTPUTS</span></span>

## <span data-ttu-id="02842-130">Note</span><span class="sxs-lookup"><span data-stu-id="02842-130">NOTES</span></span>

## <span data-ttu-id="02842-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02842-131">RELATED LINKS</span></span>
