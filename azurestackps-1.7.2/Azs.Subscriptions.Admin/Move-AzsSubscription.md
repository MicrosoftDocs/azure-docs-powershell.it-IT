---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f415da1d6f9bb086d796c0c1bf191282c2880a09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854085"
---
# <span data-ttu-id="5eb85-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="5eb85-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="5eb85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eb85-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb85-103">Trasferimento di abbonamenti tra offerte di provider Delegate.</span><span class="sxs-lookup"><span data-stu-id="5eb85-103">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="5eb85-104">Questo processo eseguirà solo un rebranding, l'offerta sottostante, i piani e le quote per gli abbonamenti non verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="5eb85-104">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="5eb85-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eb85-105">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="5eb85-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb85-106">DESCRIPTION</span></span>
<span data-ttu-id="5eb85-107">Trasferimento di abbonamenti tra offerte di provider Delegate.</span><span class="sxs-lookup"><span data-stu-id="5eb85-107">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="5eb85-108">Questo processo eseguirà solo un rebranding, l'offerta sottostante, i piani e le quote per gli abbonamenti non verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="5eb85-108">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="5eb85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eb85-109">EXAMPLES</span></span>

### <span data-ttu-id="5eb85-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5eb85-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="5eb85-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-BB8F-2c8bebc7c777/offers/RO1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="5eb85-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="5eb85-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5eb85-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="5eb85-113">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1'" | dove {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-BB8F-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="5eb85-113">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="5eb85-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eb85-114">PARAMETERS</span></span>

### <span data-ttu-id="5eb85-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eb85-115">-AsJob</span></span>
<span data-ttu-id="5eb85-116">Specifica se l'operazione di movimento deve essere eseguita come processo.</span><span class="sxs-lookup"><span data-stu-id="5eb85-116">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb85-117">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="5eb85-117">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="5eb85-118">Specifica l'offerta completa di provider delegati in cui questo cmdlet sposta gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="5eb85-118">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="5eb85-119">NULL se gli abbonamenti devono essere spostati di nuovo nel provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="5eb85-119">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="5eb85-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5eb85-120">-ResourceId</span></span>
<span data-ttu-id="5eb85-121">Specifica una matrice di identificatori di risorse di sottoscrizione completi che questo cmdlet si sposta.</span><span class="sxs-lookup"><span data-stu-id="5eb85-121">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb85-122">CommonParameters</span></span>
<span data-ttu-id="5eb85-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb85-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb85-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb85-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eb85-125">INPUTS</span></span>

## <span data-ttu-id="5eb85-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eb85-126">OUTPUTS</span></span>

## <span data-ttu-id="5eb85-127">Note</span><span class="sxs-lookup"><span data-stu-id="5eb85-127">NOTES</span></span>

## <span data-ttu-id="5eb85-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eb85-128">RELATED LINKS</span></span>

