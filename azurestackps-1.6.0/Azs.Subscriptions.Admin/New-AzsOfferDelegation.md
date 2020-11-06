---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490981"
---
# <span data-ttu-id="8ee55-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="8ee55-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="8ee55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ee55-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee55-103">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee55-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="8ee55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ee55-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ee55-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee55-106">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee55-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="8ee55-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ee55-107">EXAMPLES</span></span>

### <span data-ttu-id="8ee55-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ee55-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="8ee55-109">Creare una nuova delega per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee55-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="8ee55-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ee55-110">PARAMETERS</span></span>

### <span data-ttu-id="8ee55-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8ee55-111">-Location</span></span>
<span data-ttu-id="8ee55-112">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ee55-112">Location of the resource.</span></span>

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

### <span data-ttu-id="8ee55-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ee55-113">-Name</span></span>
<span data-ttu-id="8ee55-114">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee55-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="8ee55-115">-Offername</span><span class="sxs-lookup"><span data-stu-id="8ee55-115">-OfferName</span></span>
<span data-ttu-id="8ee55-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee55-116">Name of an offer.</span></span>

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

### <span data-ttu-id="8ee55-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee55-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ee55-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ee55-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8ee55-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ee55-119">-SubscriptionId</span></span>
<span data-ttu-id="8ee55-120">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="8ee55-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="8ee55-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ee55-121">-Confirm</span></span>
<span data-ttu-id="8ee55-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ee55-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee55-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee55-123">-WhatIf</span></span>
<span data-ttu-id="8ee55-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ee55-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee55-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ee55-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee55-126">CommonParameters</span></span>
<span data-ttu-id="8ee55-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee55-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee55-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee55-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ee55-129">INPUTS</span></span>

## <span data-ttu-id="8ee55-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ee55-130">OUTPUTS</span></span>

### <span data-ttu-id="8ee55-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="8ee55-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="8ee55-132">Note</span><span class="sxs-lookup"><span data-stu-id="8ee55-132">NOTES</span></span>

## <span data-ttu-id="8ee55-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ee55-133">RELATED LINKS</span></span>

