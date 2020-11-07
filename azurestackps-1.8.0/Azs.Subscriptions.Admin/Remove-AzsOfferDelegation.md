---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859209"
---
# <span data-ttu-id="3e419-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="3e419-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="3e419-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e419-102">SYNOPSIS</span></span>
<span data-ttu-id="3e419-103">Rimuove la delega dell'offerta</span><span class="sxs-lookup"><span data-stu-id="3e419-103">Removes the offer delegation</span></span>

## <span data-ttu-id="3e419-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e419-104">SYNTAX</span></span>

### <span data-ttu-id="3e419-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e419-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e419-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e419-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e419-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e419-107">DESCRIPTION</span></span>
<span data-ttu-id="3e419-108">Rimuove la delega dell'offerta</span><span class="sxs-lookup"><span data-stu-id="3e419-108">Removes the offer delegation</span></span>

## <span data-ttu-id="3e419-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e419-109">EXAMPLES</span></span>

### <span data-ttu-id="3e419-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e419-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="3e419-111">Rimuove la delega dell'offerta</span><span class="sxs-lookup"><span data-stu-id="3e419-111">Removes the offer delegation</span></span>

## <span data-ttu-id="3e419-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e419-112">PARAMETERS</span></span>

### <span data-ttu-id="3e419-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e419-113">-Force</span></span>
<span data-ttu-id="3e419-114">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="3e419-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="3e419-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e419-115">-Name</span></span>
<span data-ttu-id="3e419-116">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e419-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="3e419-117">-Offername</span><span class="sxs-lookup"><span data-stu-id="3e419-117">-OfferName</span></span>
<span data-ttu-id="3e419-118">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e419-118">Name of an offer.</span></span>

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

### <span data-ttu-id="3e419-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e419-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e419-120">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e419-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3e419-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e419-121">-ResourceId</span></span>
<span data-ttu-id="3e419-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e419-122">The resource id.</span></span>

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

### <span data-ttu-id="3e419-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e419-123">-Confirm</span></span>
<span data-ttu-id="3e419-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e419-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e419-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e419-125">-WhatIf</span></span>
<span data-ttu-id="3e419-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e419-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e419-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e419-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e419-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e419-128">CommonParameters</span></span>
<span data-ttu-id="3e419-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e419-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e419-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e419-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e419-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e419-131">INPUTS</span></span>

## <span data-ttu-id="3e419-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e419-132">OUTPUTS</span></span>

## <span data-ttu-id="3e419-133">Note</span><span class="sxs-lookup"><span data-stu-id="3e419-133">NOTES</span></span>

## <span data-ttu-id="3e419-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e419-134">RELATED LINKS</span></span>

