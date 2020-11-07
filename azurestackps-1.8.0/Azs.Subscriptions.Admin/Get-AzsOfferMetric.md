---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859254"
---
# <span data-ttu-id="3e3d1-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="3e3d1-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="3e3d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3d1-103">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-103">Get the offer metrics.</span></span>

## <span data-ttu-id="3e3d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e3d1-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="3e3d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e3d1-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3d1-106">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-106">Get the offer metrics.</span></span>

## <span data-ttu-id="3e3d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e3d1-107">EXAMPLES</span></span>

### <span data-ttu-id="3e3d1-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e3d1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="3e3d1-109">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-109">Get the offer metrics.</span></span>

## <span data-ttu-id="3e3d1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e3d1-110">PARAMETERS</span></span>

### <span data-ttu-id="3e3d1-111">-Offername</span><span class="sxs-lookup"><span data-stu-id="3e3d1-111">-OfferName</span></span>
<span data-ttu-id="3e3d1-112">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-112">Name of an offer.</span></span>

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

### <span data-ttu-id="3e3d1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e3d1-113">-ResourceGroupName</span></span>
<span data-ttu-id="3e3d1-114">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3e3d1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3d1-115">CommonParameters</span></span>
<span data-ttu-id="3e3d1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3d1-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3d1-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3d1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e3d1-118">INPUTS</span></span>

## <span data-ttu-id="3e3d1-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e3d1-119">OUTPUTS</span></span>

### <span data-ttu-id="3e3d1-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="3e3d1-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="3e3d1-121">Note</span><span class="sxs-lookup"><span data-stu-id="3e3d1-121">NOTES</span></span>

## <span data-ttu-id="3e3d1-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e3d1-122">RELATED LINKS</span></span>

