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
ms.locfileid: "93491525"
---
# <span data-ttu-id="f4882-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="f4882-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="f4882-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4882-102">SYNOPSIS</span></span>
<span data-ttu-id="f4882-103">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="f4882-103">Get the plan metrics.</span></span>

## <span data-ttu-id="f4882-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4882-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="f4882-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4882-105">DESCRIPTION</span></span>
<span data-ttu-id="f4882-106">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="f4882-106">Get the plan metrics.</span></span>

## <span data-ttu-id="f4882-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4882-107">EXAMPLES</span></span>

### <span data-ttu-id="f4882-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4882-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="f4882-109">Ottenere le metriche di un piano.</span><span class="sxs-lookup"><span data-stu-id="f4882-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="f4882-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4882-110">PARAMETERS</span></span>

### <span data-ttu-id="f4882-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f4882-111">-PlanName</span></span>
<span data-ttu-id="f4882-112">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="f4882-112">Name of the plan.</span></span>

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

### <span data-ttu-id="f4882-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4882-113">-ResourceGroupName</span></span>
<span data-ttu-id="f4882-114">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4882-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f4882-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4882-115">CommonParameters</span></span>
<span data-ttu-id="f4882-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4882-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4882-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4882-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4882-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4882-118">INPUTS</span></span>

## <span data-ttu-id="f4882-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4882-119">OUTPUTS</span></span>

### <span data-ttu-id="f4882-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="f4882-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="f4882-121">Note</span><span class="sxs-lookup"><span data-stu-id="f4882-121">NOTES</span></span>

## <span data-ttu-id="f4882-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4882-122">RELATED LINKS</span></span>

