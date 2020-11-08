---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030465"
---
# <span data-ttu-id="9c5d4-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="9c5d4-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="9c5d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5d4-103">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="9c5d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c5d4-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c5d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5d4-106">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="9c5d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5d4-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9c5d4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="9c5d4-109">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="9c5d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c5d4-110">PARAMETERS</span></span>

### <span data-ttu-id="9c5d4-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9c5d4-111">-Location</span></span>
<span data-ttu-id="9c5d4-112">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-112">Location of the resource.</span></span>

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

### <span data-ttu-id="9c5d4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c5d4-113">-Name</span></span>
<span data-ttu-id="9c5d4-114">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="9c5d4-115">-Offername</span><span class="sxs-lookup"><span data-stu-id="9c5d4-115">-OfferName</span></span>
<span data-ttu-id="9c5d4-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-116">Name of an offer.</span></span>

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

### <span data-ttu-id="9c5d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c5d4-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9c5d4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c5d4-119">-SubscriptionId</span></span>
<span data-ttu-id="9c5d4-120">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="9c5d4-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c5d4-121">-Confirm</span></span>
<span data-ttu-id="9c5d4-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5d4-123">-WhatIf</span></span>
<span data-ttu-id="9c5d4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5d4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5d4-126">CommonParameters</span></span>
<span data-ttu-id="9c5d4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5d4-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5d4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5d4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c5d4-129">INPUTS</span></span>

## <span data-ttu-id="9c5d4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c5d4-130">OUTPUTS</span></span>

### <span data-ttu-id="9c5d4-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="9c5d4-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="9c5d4-132">Note</span><span class="sxs-lookup"><span data-stu-id="9c5d4-132">NOTES</span></span>

## <span data-ttu-id="9c5d4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c5d4-133">RELATED LINKS</span></span>

