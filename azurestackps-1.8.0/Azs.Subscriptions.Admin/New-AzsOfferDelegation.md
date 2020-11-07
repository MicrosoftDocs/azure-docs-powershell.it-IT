---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859221"
---
# <span data-ttu-id="a734f-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a734f-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="a734f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a734f-102">SYNOPSIS</span></span>
<span data-ttu-id="a734f-103">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a734f-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="a734f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a734f-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a734f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a734f-105">DESCRIPTION</span></span>
<span data-ttu-id="a734f-106">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a734f-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="a734f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a734f-107">EXAMPLES</span></span>

### <span data-ttu-id="a734f-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a734f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a734f-109">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a734f-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="a734f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a734f-110">PARAMETERS</span></span>

### <span data-ttu-id="a734f-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a734f-111">-Location</span></span>
<span data-ttu-id="a734f-112">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a734f-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a734f-113">-Name</span></span>
<span data-ttu-id="a734f-114">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a734f-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a734f-115">-Offername</span><span class="sxs-lookup"><span data-stu-id="a734f-115">-OfferName</span></span>
<span data-ttu-id="a734f-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a734f-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a734f-117">-ResourceGroupName</span></span>
<span data-ttu-id="a734f-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a734f-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a734f-119">-SubscriptionId</span></span>
<span data-ttu-id="a734f-120">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="a734f-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a734f-121">-Confirm</span></span>
<span data-ttu-id="a734f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a734f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a734f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a734f-123">-WhatIf</span></span>
<span data-ttu-id="a734f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a734f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a734f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a734f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a734f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a734f-126">CommonParameters</span></span>
<span data-ttu-id="a734f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a734f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a734f-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a734f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a734f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a734f-129">INPUTS</span></span>

## <span data-ttu-id="a734f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a734f-130">OUTPUTS</span></span>

### <span data-ttu-id="a734f-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a734f-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="a734f-132">Note</span><span class="sxs-lookup"><span data-stu-id="a734f-132">NOTES</span></span>

## <span data-ttu-id="a734f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a734f-133">RELATED LINKS</span></span>

