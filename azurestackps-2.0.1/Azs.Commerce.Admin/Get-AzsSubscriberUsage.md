---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023302"
---
# <span data-ttu-id="92eb8-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="92eb8-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="92eb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="92eb8-103">Ottiene una raccolta di SubscriberUsageAggregates, che sono UsageAggregates dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="92eb8-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="92eb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92eb8-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="92eb8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="92eb8-106">Ottiene una raccolta di SubscriberUsageAggregates, che sono UsageAggregates dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="92eb8-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="92eb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="92eb8-108">Esempio 1: ottenere i dati di utilizzo aggregati per giorno</span><span class="sxs-lookup"><span data-stu-id="92eb8-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="92eb8-109">Ottenere i dati sull'utilizzo per l'intera giornata del 30 dicembre 2019 (in UTC) per tutti i tenant in provider aggregati per il giorno.</span><span class="sxs-lookup"><span data-stu-id="92eb8-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="92eb8-110">ReportedStartTime e ReportedEndTime devono essere arrotondati a giorni.</span><span class="sxs-lookup"><span data-stu-id="92eb8-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="92eb8-111">Se viene chiamato come amministratore del servizio, questo Mostra in modo efficace tutti i dati sull'utilizzo per ogni tenant.</span><span class="sxs-lookup"><span data-stu-id="92eb8-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="92eb8-112">Esempio 2: ottenere i dati di utilizzo aggregati in base all'ora</span><span class="sxs-lookup"><span data-stu-id="92eb8-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="92eb8-113">Ottenere i dati di utilizzo tra 12am-2 il 30 dicembre 2019 (in formato UTC) aggregati in base all'ora.</span><span class="sxs-lookup"><span data-stu-id="92eb8-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="92eb8-114">ReportedStartTime e ReportedEndTime devono essere arrotondati in ore.</span><span class="sxs-lookup"><span data-stu-id="92eb8-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="92eb8-115">Allo stesso modo, se chiamato come amministratore del servizio, questo Mostra in modo efficace tutti i dati sull'utilizzo per ogni tenant.</span><span class="sxs-lookup"><span data-stu-id="92eb8-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="92eb8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92eb8-116">PARAMETERS</span></span>

### <span data-ttu-id="92eb8-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="92eb8-117">-AggregationGranularity</span></span>
<span data-ttu-id="92eb8-118">Granularità dell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="92eb8-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="92eb8-119">-ContinuationToken</span></span>
<span data-ttu-id="92eb8-120">Token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="92eb8-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92eb8-121">-DefaultProfile</span></span>
<span data-ttu-id="92eb8-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92eb8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="92eb8-123">-ReportedEndTime</span></span>
<span data-ttu-id="92eb8-124">Ora di fine riportata (esclusiva).</span><span class="sxs-lookup"><span data-stu-id="92eb8-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="92eb8-125">-ReportedStartTime</span></span>
<span data-ttu-id="92eb8-126">Ora di inizio riportata (inclusi).</span><span class="sxs-lookup"><span data-stu-id="92eb8-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="92eb8-127">-SubscriberId</span></span>
<span data-ttu-id="92eb8-128">Identificatore della sottoscrizione del tenant.</span><span class="sxs-lookup"><span data-stu-id="92eb8-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92eb8-129">-SubscriptionId</span></span>
<span data-ttu-id="92eb8-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92eb8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92eb8-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="92eb8-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92eb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92eb8-132">CommonParameters</span></span>
<span data-ttu-id="92eb8-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92eb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92eb8-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92eb8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92eb8-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92eb8-135">INPUTS</span></span>

## <span data-ttu-id="92eb8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92eb8-136">OUTPUTS</span></span>

### <span data-ttu-id="92eb8-137">Microsoft. Azure. PowerShell. Cmdlets. Commerce. Models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="92eb8-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="92eb8-138">Note</span><span class="sxs-lookup"><span data-stu-id="92eb8-138">NOTES</span></span>

## <span data-ttu-id="92eb8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92eb8-139">RELATED LINKS</span></span>

