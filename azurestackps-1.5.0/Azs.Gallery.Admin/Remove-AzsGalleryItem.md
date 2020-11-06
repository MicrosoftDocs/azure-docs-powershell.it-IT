---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491134"
---
# <span data-ttu-id="2e11a-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2e11a-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="2e11a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e11a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e11a-103">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="2e11a-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="2e11a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e11a-104">SYNTAX</span></span>

### <span data-ttu-id="2e11a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e11a-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e11a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e11a-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e11a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e11a-107">DESCRIPTION</span></span>
<span data-ttu-id="2e11a-108">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="2e11a-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="2e11a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e11a-109">EXAMPLES</span></span>

### <span data-ttu-id="2e11a-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e11a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="2e11a-111">Eliminare un elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2e11a-111">Delete a gallery item.</span></span>

## <span data-ttu-id="2e11a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e11a-112">PARAMETERS</span></span>

### <span data-ttu-id="2e11a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e11a-113">-Force</span></span>
<span data-ttu-id="2e11a-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2e11a-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2e11a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e11a-115">-Name</span></span>
<span data-ttu-id="2e11a-116">Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2e11a-116">Identity of the gallery item.</span></span>
<span data-ttu-id="2e11a-117">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="2e11a-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="2e11a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e11a-118">-ResourceId</span></span>
<span data-ttu-id="2e11a-119">ID risorsa di Azure completo.</span><span class="sxs-lookup"><span data-stu-id="2e11a-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="2e11a-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e11a-120">-Confirm</span></span>
<span data-ttu-id="2e11a-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e11a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e11a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e11a-122">-WhatIf</span></span>
<span data-ttu-id="2e11a-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e11a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e11a-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e11a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e11a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e11a-125">CommonParameters</span></span>
<span data-ttu-id="2e11a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e11a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e11a-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e11a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e11a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e11a-128">INPUTS</span></span>

## <span data-ttu-id="2e11a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e11a-129">OUTPUTS</span></span>

## <span data-ttu-id="2e11a-130">Note</span><span class="sxs-lookup"><span data-stu-id="2e11a-130">NOTES</span></span>

## <span data-ttu-id="2e11a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e11a-131">RELATED LINKS</span></span>
