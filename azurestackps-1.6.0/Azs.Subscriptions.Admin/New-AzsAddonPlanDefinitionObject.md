---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490870"
---
# <span data-ttu-id="2fca9-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="2fca9-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="2fca9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fca9-102">SYNOPSIS</span></span>
<span data-ttu-id="2fca9-103">Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fca9-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="2fca9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fca9-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="2fca9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fca9-105">DESCRIPTION</span></span>
<span data-ttu-id="2fca9-106">Contiene il nome del piano desiderato da collegare o scollegare da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fca9-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="2fca9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fca9-107">EXAMPLES</span></span>

### <span data-ttu-id="2fca9-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2fca9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="2fca9-109">Creare un nuovo oggetto definizione piano per il piano specificato con il limite di acquisizione di 500.</span><span class="sxs-lookup"><span data-stu-id="2fca9-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="2fca9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fca9-110">PARAMETERS</span></span>

### <span data-ttu-id="2fca9-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="2fca9-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="2fca9-112">Numero massimo di istanze che possono essere acquisite da un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2fca9-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="2fca9-113">Se non specificato, il valore assunto è 1.</span><span class="sxs-lookup"><span data-stu-id="2fca9-113">If not specified, the assumed value is 1.</span></span>

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

### <span data-ttu-id="2fca9-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="2fca9-114">-PlanId</span></span>
<span data-ttu-id="2fca9-115">Identificatore piano.</span><span class="sxs-lookup"><span data-stu-id="2fca9-115">Plan identifier.</span></span>

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

### <span data-ttu-id="2fca9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fca9-116">CommonParameters</span></span>
<span data-ttu-id="2fca9-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fca9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fca9-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fca9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fca9-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fca9-119">INPUTS</span></span>

## <span data-ttu-id="2fca9-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fca9-120">OUTPUTS</span></span>

## <span data-ttu-id="2fca9-121">Note</span><span class="sxs-lookup"><span data-stu-id="2fca9-121">NOTES</span></span>

## <span data-ttu-id="2fca9-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fca9-122">RELATED LINKS</span></span>

