---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030547"
---
# <span data-ttu-id="9e810-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="9e810-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="9e810-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e810-102">SYNOPSIS</span></span>
<span data-ttu-id="9e810-103">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="9e810-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="9e810-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e810-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="9e810-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e810-105">DESCRIPTION</span></span>
<span data-ttu-id="9e810-106">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="9e810-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="9e810-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e810-107">EXAMPLES</span></span>

### <span data-ttu-id="9e810-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e810-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="9e810-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-BB8F-2c8bebc7c777/offers/RO1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="9e810-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="9e810-110">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e810-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="9e810-111">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1'" | Select-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="9e810-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="9e810-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e810-112">PARAMETERS</span></span>

### <span data-ttu-id="9e810-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e810-113">-AsJob</span></span>
<span data-ttu-id="9e810-114">Specifica se l'operazione di movimento deve essere eseguita come processo.</span><span class="sxs-lookup"><span data-stu-id="9e810-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="9e810-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="9e810-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="9e810-116">Specifica l'offerta completa di provider delegati in cui questo cmdlet sposta gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="9e810-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="9e810-117">NULL se gli abbonamenti devono essere spostati di nuovo nel provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="9e810-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="9e810-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e810-118">-ResourceId</span></span>
<span data-ttu-id="9e810-119">Specifica una matrice di identificatori di risorse di sottoscrizione completi che questo cmdlet si sposta.</span><span class="sxs-lookup"><span data-stu-id="9e810-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="9e810-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e810-120">CommonParameters</span></span>
<span data-ttu-id="9e810-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e810-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e810-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e810-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e810-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e810-123">INPUTS</span></span>

## <span data-ttu-id="9e810-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e810-124">OUTPUTS</span></span>

## <span data-ttu-id="9e810-125">Note</span><span class="sxs-lookup"><span data-stu-id="9e810-125">NOTES</span></span>

## <span data-ttu-id="9e810-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e810-126">RELATED LINKS</span></span>

