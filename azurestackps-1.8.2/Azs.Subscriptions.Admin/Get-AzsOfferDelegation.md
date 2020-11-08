---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030434"
---
# <span data-ttu-id="6cf82-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="6cf82-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="6cf82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cf82-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf82-103">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="6cf82-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="6cf82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cf82-104">SYNTAX</span></span>

### <span data-ttu-id="6cf82-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cf82-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cf82-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6cf82-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="6cf82-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf82-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6cf82-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cf82-108">DESCRIPTION</span></span>
<span data-ttu-id="6cf82-109">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="6cf82-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="6cf82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cf82-110">EXAMPLES</span></span>

### <span data-ttu-id="6cf82-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cf82-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="6cf82-112">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="6cf82-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="6cf82-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cf82-113">PARAMETERS</span></span>

### <span data-ttu-id="6cf82-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cf82-114">-Name</span></span>
<span data-ttu-id="6cf82-115">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="6cf82-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="6cf82-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="6cf82-116">-OfferName</span></span>
<span data-ttu-id="6cf82-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="6cf82-117">Name of an offer.</span></span>

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

### <span data-ttu-id="6cf82-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf82-118">-ResourceGroupName</span></span>
<span data-ttu-id="6cf82-119">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6cf82-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6cf82-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf82-120">-ResourceId</span></span>
<span data-ttu-id="6cf82-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6cf82-121">The resource id.</span></span>

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

### <span data-ttu-id="6cf82-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="6cf82-122">-Skip</span></span>
<span data-ttu-id="6cf82-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6cf82-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6cf82-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="6cf82-124">-Top</span></span>
<span data-ttu-id="6cf82-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6cf82-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6cf82-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6cf82-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6cf82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf82-127">CommonParameters</span></span>
<span data-ttu-id="6cf82-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf82-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf82-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf82-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cf82-130">INPUTS</span></span>

## <span data-ttu-id="6cf82-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cf82-131">OUTPUTS</span></span>

### <span data-ttu-id="6cf82-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="6cf82-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="6cf82-133">Note</span><span class="sxs-lookup"><span data-stu-id="6cf82-133">NOTES</span></span>

## <span data-ttu-id="6cf82-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cf82-134">RELATED LINKS</span></span>

