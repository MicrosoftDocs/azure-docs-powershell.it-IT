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
ms.locfileid: "93858698"
---
# <span data-ttu-id="a0602-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a0602-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="a0602-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0602-102">SYNOPSIS</span></span>
<span data-ttu-id="a0602-103">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="a0602-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="a0602-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0602-104">SYNTAX</span></span>

### <span data-ttu-id="a0602-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0602-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0602-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a0602-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="a0602-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0602-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a0602-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0602-108">DESCRIPTION</span></span>
<span data-ttu-id="a0602-109">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="a0602-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="a0602-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0602-110">EXAMPLES</span></span>

### <span data-ttu-id="a0602-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a0602-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="a0602-112">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="a0602-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="a0602-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0602-113">PARAMETERS</span></span>

### <span data-ttu-id="a0602-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0602-114">-Name</span></span>
<span data-ttu-id="a0602-115">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a0602-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a0602-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="a0602-116">-OfferName</span></span>
<span data-ttu-id="a0602-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a0602-117">Name of an offer.</span></span>

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

### <span data-ttu-id="a0602-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0602-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0602-119">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0602-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a0602-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0602-120">-ResourceId</span></span>
<span data-ttu-id="a0602-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0602-121">The resource id.</span></span>

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

### <span data-ttu-id="a0602-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="a0602-122">-Skip</span></span>
<span data-ttu-id="a0602-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a0602-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a0602-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="a0602-124">-Top</span></span>
<span data-ttu-id="a0602-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a0602-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a0602-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a0602-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a0602-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0602-127">CommonParameters</span></span>
<span data-ttu-id="a0602-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0602-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0602-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0602-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0602-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0602-130">INPUTS</span></span>

## <span data-ttu-id="a0602-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0602-131">OUTPUTS</span></span>

### <span data-ttu-id="a0602-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a0602-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="a0602-133">Note</span><span class="sxs-lookup"><span data-stu-id="a0602-133">NOTES</span></span>

## <span data-ttu-id="a0602-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0602-134">RELATED LINKS</span></span>

