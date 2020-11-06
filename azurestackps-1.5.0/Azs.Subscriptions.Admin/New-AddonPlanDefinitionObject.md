---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506987"
---
# <span data-ttu-id="11ec0-101">New-AddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="11ec0-101">New-AddonPlanDefinitionObject</span></span>

## <span data-ttu-id="11ec0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="11ec0-103">Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="11ec0-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="11ec0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11ec0-104">SYNTAX</span></span>

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="11ec0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="11ec0-106">Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="11ec0-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="11ec0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="11ec0-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11ec0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="11ec0-109">Creare un nuovo oggetto definizione piano per il piano specificato con il limite di acquisizione di 500.</span><span class="sxs-lookup"><span data-stu-id="11ec0-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="11ec0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11ec0-110">PARAMETERS</span></span>

### <span data-ttu-id="11ec0-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="11ec0-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="11ec0-112">Numero massimo di istanze che possono essere acquisite da un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="11ec0-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="11ec0-113">Se non specificato, il valore assunto è 1.</span><span class="sxs-lookup"><span data-stu-id="11ec0-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ec0-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="11ec0-114">-PlanId</span></span>
<span data-ttu-id="11ec0-115">Identificatore piano.</span><span class="sxs-lookup"><span data-stu-id="11ec0-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ec0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ec0-116">CommonParameters</span></span>
<span data-ttu-id="11ec0-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ec0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ec0-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ec0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ec0-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11ec0-119">INPUTS</span></span>

## <span data-ttu-id="11ec0-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11ec0-120">OUTPUTS</span></span>

## <span data-ttu-id="11ec0-121">Note</span><span class="sxs-lookup"><span data-stu-id="11ec0-121">NOTES</span></span>

## <span data-ttu-id="11ec0-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11ec0-122">RELATED LINKS</span></span>

