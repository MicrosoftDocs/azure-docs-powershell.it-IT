---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030245"
---
# <span data-ttu-id="85065-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="85065-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="85065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85065-102">SYNOPSIS</span></span>
<span data-ttu-id="85065-103">Eliminare un'immagine della macchina virtuale dal repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="85065-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="85065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85065-104">SYNTAX</span></span>

### <span data-ttu-id="85065-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85065-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85065-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85065-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85065-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85065-107">DESCRIPTION</span></span>
<span data-ttu-id="85065-108">Eliminare un'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="85065-108">Delete a platform image</span></span>

## <span data-ttu-id="85065-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85065-109">EXAMPLES</span></span>

### <span data-ttu-id="85065-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85065-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="85065-111">Eliminare un'immagine della piattaforma esistente.</span><span class="sxs-lookup"><span data-stu-id="85065-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="85065-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85065-112">PARAMETERS</span></span>

### <span data-ttu-id="85065-113">-Force</span><span class="sxs-lookup"><span data-stu-id="85065-113">-Force</span></span>
<span data-ttu-id="85065-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="85065-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="85065-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="85065-115">-Location</span></span>
<span data-ttu-id="85065-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="85065-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85065-117">-Offerta</span><span class="sxs-lookup"><span data-stu-id="85065-117">-Offer</span></span>
<span data-ttu-id="85065-118">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="85065-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85065-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="85065-119">-Publisher</span></span>
<span data-ttu-id="85065-120">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="85065-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85065-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85065-121">-ResourceId</span></span>
<span data-ttu-id="85065-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="85065-122">The resource id.</span></span>

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

### <span data-ttu-id="85065-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="85065-123">-Sku</span></span>
<span data-ttu-id="85065-124">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="85065-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85065-125">-Versione</span><span class="sxs-lookup"><span data-stu-id="85065-125">-Version</span></span>
<span data-ttu-id="85065-126">Versione dell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85065-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85065-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85065-127">-Confirm</span></span>
<span data-ttu-id="85065-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85065-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85065-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85065-129">-WhatIf</span></span>
<span data-ttu-id="85065-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85065-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85065-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85065-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85065-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85065-132">CommonParameters</span></span>
<span data-ttu-id="85065-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85065-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85065-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85065-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85065-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85065-135">INPUTS</span></span>

## <span data-ttu-id="85065-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85065-136">OUTPUTS</span></span>

## <span data-ttu-id="85065-137">Note</span><span class="sxs-lookup"><span data-stu-id="85065-137">NOTES</span></span>

## <span data-ttu-id="85065-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85065-138">RELATED LINKS</span></span>

