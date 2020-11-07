---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859258"
---
# <span data-ttu-id="d235f-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d235f-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="d235f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d235f-102">SYNOPSIS</span></span>
<span data-ttu-id="d235f-103">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="d235f-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="d235f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d235f-104">SYNTAX</span></span>

### <span data-ttu-id="d235f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d235f-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d235f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d235f-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="d235f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d235f-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d235f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d235f-108">DESCRIPTION</span></span>
<span data-ttu-id="d235f-109">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="d235f-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="d235f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d235f-110">EXAMPLES</span></span>

### <span data-ttu-id="d235f-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d235f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="d235f-112">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="d235f-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="d235f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d235f-113">PARAMETERS</span></span>

### <span data-ttu-id="d235f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d235f-114">-Name</span></span>
<span data-ttu-id="d235f-115">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="d235f-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="d235f-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="d235f-116">-OfferName</span></span>
<span data-ttu-id="d235f-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="d235f-117">Name of an offer.</span></span>

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

### <span data-ttu-id="d235f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d235f-118">-ResourceGroupName</span></span>
<span data-ttu-id="d235f-119">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d235f-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d235f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d235f-120">-ResourceId</span></span>
<span data-ttu-id="d235f-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d235f-121">The resource id.</span></span>

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

### <span data-ttu-id="d235f-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="d235f-122">-Skip</span></span>
<span data-ttu-id="d235f-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d235f-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d235f-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d235f-124">-Top</span></span>
<span data-ttu-id="d235f-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d235f-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d235f-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d235f-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d235f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d235f-127">CommonParameters</span></span>
<span data-ttu-id="d235f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d235f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d235f-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d235f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d235f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d235f-130">INPUTS</span></span>

## <span data-ttu-id="d235f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d235f-131">OUTPUTS</span></span>

### <span data-ttu-id="d235f-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d235f-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="d235f-133">Note</span><span class="sxs-lookup"><span data-stu-id="d235f-133">NOTES</span></span>

## <span data-ttu-id="d235f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d235f-134">RELATED LINKS</span></span>

