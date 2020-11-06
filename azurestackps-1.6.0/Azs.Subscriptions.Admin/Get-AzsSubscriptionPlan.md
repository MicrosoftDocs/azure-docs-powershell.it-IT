---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490689"
---
# <span data-ttu-id="fb0e6-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="fb0e6-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="fb0e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0e6-103">Ottenere una raccolta di tutti i piani acquisiti a cui l'abbonamento ha accesso.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="fb0e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb0e6-104">SYNTAX</span></span>

### <span data-ttu-id="fb0e6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb0e6-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fb0e6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="fb0e6-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="fb0e6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0e6-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fb0e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb0e6-108">DESCRIPTION</span></span>
<span data-ttu-id="fb0e6-109">Ottenere una raccolta di tutti i piani acquisiti a cui l'abbonamento ha accesso.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="fb0e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb0e6-110">EXAMPLES</span></span>

### <span data-ttu-id="fb0e6-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb0e6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="fb0e6-112">Ottenere una raccolta di tutti i piani acquisiti a cui l'abbonamento ha accesso.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="fb0e6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb0e6-113">PARAMETERS</span></span>

### <span data-ttu-id="fb0e6-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="fb0e6-114">-AcquisitionId</span></span>
<span data-ttu-id="fb0e6-115">Identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="fb0e6-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0e6-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0e6-116">-ResourceId</span></span>
<span data-ttu-id="fb0e6-117">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-117">The resource id.</span></span>

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

### <span data-ttu-id="fb0e6-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="fb0e6-118">-Skip</span></span>
<span data-ttu-id="fb0e6-119">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fb0e6-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb0e6-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="fb0e6-121">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0e6-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="fb0e6-122">-Top</span></span>
<span data-ttu-id="fb0e6-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fb0e6-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fb0e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0e6-125">CommonParameters</span></span>
<span data-ttu-id="fb0e6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0e6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0e6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0e6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb0e6-128">INPUTS</span></span>

## <span data-ttu-id="fb0e6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb0e6-129">OUTPUTS</span></span>

### <span data-ttu-id="fb0e6-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="fb0e6-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="fb0e6-131">Note</span><span class="sxs-lookup"><span data-stu-id="fb0e6-131">NOTES</span></span>

## <span data-ttu-id="fb0e6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb0e6-132">RELATED LINKS</span></span>

