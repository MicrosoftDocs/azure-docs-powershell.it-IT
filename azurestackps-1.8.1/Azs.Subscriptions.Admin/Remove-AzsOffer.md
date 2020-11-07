---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859478"
---
# <span data-ttu-id="208bb-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="208bb-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="208bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="208bb-102">SYNOPSIS</span></span>
<span data-ttu-id="208bb-103">Eliminare l'offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="208bb-103">Delete the specified offer.</span></span>

## <span data-ttu-id="208bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="208bb-104">SYNTAX</span></span>

### <span data-ttu-id="208bb-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="208bb-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208bb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="208bb-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="208bb-107">DESCRIPTION</span></span>
<span data-ttu-id="208bb-108">Eliminare l'offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="208bb-108">Delete the specified offer.</span></span>

## <span data-ttu-id="208bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="208bb-109">EXAMPLES</span></span>

### <span data-ttu-id="208bb-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="208bb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="208bb-111">Eliminare l'offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="208bb-111">Delete the specified offer.</span></span>

## <span data-ttu-id="208bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="208bb-112">PARAMETERS</span></span>

### <span data-ttu-id="208bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="208bb-113">-Force</span></span>
<span data-ttu-id="208bb-114">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="208bb-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="208bb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="208bb-115">-Name</span></span>
<span data-ttu-id="208bb-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="208bb-116">Name of an offer.</span></span>

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

### <span data-ttu-id="208bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="208bb-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="208bb-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="208bb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="208bb-119">-ResourceId</span></span>
<span data-ttu-id="208bb-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="208bb-120">The resource id.</span></span>

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

### <span data-ttu-id="208bb-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="208bb-121">-Confirm</span></span>
<span data-ttu-id="208bb-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208bb-123">-WhatIf</span></span>
<span data-ttu-id="208bb-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="208bb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208bb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="208bb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208bb-126">CommonParameters</span></span>
<span data-ttu-id="208bb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208bb-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208bb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208bb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="208bb-129">INPUTS</span></span>

## <span data-ttu-id="208bb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="208bb-130">OUTPUTS</span></span>

## <span data-ttu-id="208bb-131">Note</span><span class="sxs-lookup"><span data-stu-id="208bb-131">NOTES</span></span>

## <span data-ttu-id="208bb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="208bb-132">RELATED LINKS</span></span>

