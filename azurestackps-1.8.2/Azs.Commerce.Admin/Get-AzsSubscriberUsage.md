---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030263"
---
# <span data-ttu-id="a47f8-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="a47f8-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="a47f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a47f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a47f8-103">Recuperare i dati sull'utilizzo durante l'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="a47f8-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="a47f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a47f8-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a47f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a47f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a47f8-106">Recuperare i dati sull'utilizzo durante l'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="a47f8-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="a47f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a47f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a47f8-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="a47f8-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="a47f8-109">Ottenere i dati sull'utilizzo delle ultime 24 ore.</span><span class="sxs-lookup"><span data-stu-id="a47f8-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="a47f8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a47f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a47f8-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="a47f8-111">-SubscriberId</span></span>
<span data-ttu-id="a47f8-112">Identificatore della sottoscrizione del tenant.</span><span class="sxs-lookup"><span data-stu-id="a47f8-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="a47f8-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="a47f8-113">-ReportedStartTime</span></span>
<span data-ttu-id="a47f8-114">Ora di inizio riportata (inclusi).</span><span class="sxs-lookup"><span data-stu-id="a47f8-114">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="a47f8-115">-AggregationGranularity</span></span>
<span data-ttu-id="a47f8-116">Granularità dell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="a47f8-116">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="a47f8-117">-Skip</span></span>
<span data-ttu-id="a47f8-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a47f8-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="a47f8-119">-ReportedEndTime</span></span>
<span data-ttu-id="a47f8-120">Ora di fine riportata (esclusiva).</span><span class="sxs-lookup"><span data-stu-id="a47f8-120">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="a47f8-121">-ContinuationToken</span></span>
<span data-ttu-id="a47f8-122">Token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="a47f8-122">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="a47f8-123">-Top</span></span>
<span data-ttu-id="a47f8-124">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a47f8-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a47f8-125">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a47f8-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47f8-126">CommonParameters</span></span>
<span data-ttu-id="a47f8-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47f8-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47f8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47f8-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a47f8-129">INPUTS</span></span>

## <span data-ttu-id="a47f8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a47f8-130">OUTPUTS</span></span>

### <span data-ttu-id="a47f8-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="a47f8-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="a47f8-132">Note</span><span class="sxs-lookup"><span data-stu-id="a47f8-132">NOTES</span></span>

## <span data-ttu-id="a47f8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a47f8-133">RELATED LINKS</span></span>
