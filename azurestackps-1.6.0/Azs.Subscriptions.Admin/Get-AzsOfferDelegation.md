---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491526"
---
# <span data-ttu-id="eb938-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eb938-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="eb938-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb938-102">SYNOPSIS</span></span>
<span data-ttu-id="eb938-103">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="eb938-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="eb938-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb938-104">SYNTAX</span></span>

### <span data-ttu-id="eb938-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb938-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb938-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="eb938-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="eb938-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb938-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eb938-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb938-108">DESCRIPTION</span></span>
<span data-ttu-id="eb938-109">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="eb938-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="eb938-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb938-110">EXAMPLES</span></span>

### <span data-ttu-id="eb938-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb938-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="eb938-112">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="eb938-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="eb938-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb938-113">PARAMETERS</span></span>

### <span data-ttu-id="eb938-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb938-114">-Name</span></span>
<span data-ttu-id="eb938-115">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="eb938-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="eb938-116">-OfferName</span></span>
<span data-ttu-id="eb938-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="eb938-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb938-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb938-119">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb938-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb938-120">-ResourceId</span></span>
<span data-ttu-id="eb938-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb938-121">The resource id.</span></span>

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

### <span data-ttu-id="eb938-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="eb938-122">-Skip</span></span>
<span data-ttu-id="eb938-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eb938-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="eb938-124">-Top</span></span>
<span data-ttu-id="eb938-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eb938-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eb938-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="eb938-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb938-127">CommonParameters</span></span>
<span data-ttu-id="eb938-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb938-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb938-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb938-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb938-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb938-130">INPUTS</span></span>

## <span data-ttu-id="eb938-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb938-131">OUTPUTS</span></span>

### <span data-ttu-id="eb938-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eb938-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="eb938-133">Note</span><span class="sxs-lookup"><span data-stu-id="eb938-133">NOTES</span></span>

## <span data-ttu-id="eb938-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb938-134">RELATED LINKS</span></span>

