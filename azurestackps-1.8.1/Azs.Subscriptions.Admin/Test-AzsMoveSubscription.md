---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859486"
---
# <span data-ttu-id="cbd13-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="cbd13-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="cbd13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbd13-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd13-103">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="cbd13-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="cbd13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbd13-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="cbd13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd13-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd13-106">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="cbd13-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="cbd13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbd13-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd13-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cbd13-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="cbd13-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-BB8F-2c8bebc7c777/offers/RO1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="cbd13-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="cbd13-110">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cbd13-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="cbd13-111">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1'" | Select-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="cbd13-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="cbd13-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbd13-112">PARAMETERS</span></span>

### <span data-ttu-id="cbd13-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbd13-113">-AsJob</span></span>
<span data-ttu-id="cbd13-114">Specifica se l'operazione di movimento deve essere eseguita come processo.</span><span class="sxs-lookup"><span data-stu-id="cbd13-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="cbd13-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="cbd13-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="cbd13-116">Specifica l'offerta completa di provider delegati in cui questo cmdlet sposta gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="cbd13-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="cbd13-117">NULL se gli abbonamenti devono essere spostati di nuovo nel provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="cbd13-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="cbd13-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd13-118">-ResourceId</span></span>
<span data-ttu-id="cbd13-119">Specifica una matrice di identificatori di risorse di sottoscrizione completi che questo cmdlet si sposta.</span><span class="sxs-lookup"><span data-stu-id="cbd13-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="cbd13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd13-120">CommonParameters</span></span>
<span data-ttu-id="cbd13-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd13-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd13-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd13-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbd13-123">INPUTS</span></span>

## <span data-ttu-id="cbd13-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbd13-124">OUTPUTS</span></span>

## <span data-ttu-id="cbd13-125">Note</span><span class="sxs-lookup"><span data-stu-id="cbd13-125">NOTES</span></span>

## <span data-ttu-id="cbd13-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbd13-126">RELATED LINKS</span></span>

