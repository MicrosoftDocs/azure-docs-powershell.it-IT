---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858310"
---
# <span data-ttu-id="6f51c-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="6f51c-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="6f51c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f51c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f51c-103">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="6f51c-103">Get the plan metrics.</span></span>

## <span data-ttu-id="6f51c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f51c-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="6f51c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f51c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f51c-106">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="6f51c-106">Get the plan metrics.</span></span>

## <span data-ttu-id="6f51c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f51c-107">EXAMPLES</span></span>

### <span data-ttu-id="6f51c-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f51c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="6f51c-109">Ottenere le metriche di un piano.</span><span class="sxs-lookup"><span data-stu-id="6f51c-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="6f51c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f51c-110">PARAMETERS</span></span>

### <span data-ttu-id="6f51c-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6f51c-111">-PlanName</span></span>
<span data-ttu-id="6f51c-112">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="6f51c-112">Name of the plan.</span></span>

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

### <span data-ttu-id="6f51c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f51c-113">-ResourceGroupName</span></span>
<span data-ttu-id="6f51c-114">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f51c-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6f51c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f51c-115">CommonParameters</span></span>
<span data-ttu-id="6f51c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f51c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f51c-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f51c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f51c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f51c-118">INPUTS</span></span>

## <span data-ttu-id="6f51c-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f51c-119">OUTPUTS</span></span>

### <span data-ttu-id="6f51c-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="6f51c-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="6f51c-121">Note</span><span class="sxs-lookup"><span data-stu-id="6f51c-121">NOTES</span></span>

## <span data-ttu-id="6f51c-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f51c-122">RELATED LINKS</span></span>

