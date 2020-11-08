---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030558"
---
# <span data-ttu-id="0056b-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="0056b-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="0056b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0056b-102">SYNOPSIS</span></span>
<span data-ttu-id="0056b-103">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="0056b-103">Get the plan metrics.</span></span>

## <span data-ttu-id="0056b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0056b-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="0056b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0056b-105">DESCRIPTION</span></span>
<span data-ttu-id="0056b-106">Ottenere le metriche per il piano.</span><span class="sxs-lookup"><span data-stu-id="0056b-106">Get the plan metrics.</span></span>

## <span data-ttu-id="0056b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0056b-107">EXAMPLES</span></span>

### <span data-ttu-id="0056b-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0056b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="0056b-109">Ottenere le metriche di un piano.</span><span class="sxs-lookup"><span data-stu-id="0056b-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="0056b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0056b-110">PARAMETERS</span></span>

### <span data-ttu-id="0056b-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0056b-111">-PlanName</span></span>
<span data-ttu-id="0056b-112">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="0056b-112">Name of the plan.</span></span>

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

### <span data-ttu-id="0056b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0056b-113">-ResourceGroupName</span></span>
<span data-ttu-id="0056b-114">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0056b-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0056b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0056b-115">CommonParameters</span></span>
<span data-ttu-id="0056b-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0056b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0056b-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0056b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0056b-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0056b-118">INPUTS</span></span>

## <span data-ttu-id="0056b-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0056b-119">OUTPUTS</span></span>

### <span data-ttu-id="0056b-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="0056b-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="0056b-121">Note</span><span class="sxs-lookup"><span data-stu-id="0056b-121">NOTES</span></span>

## <span data-ttu-id="0056b-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0056b-122">RELATED LINKS</span></span>

