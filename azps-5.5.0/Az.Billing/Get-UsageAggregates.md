---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200942"
---
# <span data-ttu-id="4f0cc-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="4f0cc-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="4f0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0cc-103">Recupera i dettagli di utilizzo della sottoscrizione di Azure riportati.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="4f0cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f0cc-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f0cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="4f0cc-106">Il cmdlet **Get-UsageAggregates** ottiene i dati di utilizzo aggregati della sottoscrizione di Azure in base alle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f0cc-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="4f0cc-107">Ora di inizio e di fine della registrazione dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="4f0cc-108">Precisione dell'aggregazione, giornaliera o oraria.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="4f0cc-109">Dettagli del livello di istanza per più istanze della stessa risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="4f0cc-110">Per ottenere risultati coerenti, i dati restituiti si basano sulla data in cui la risorsa Azure ha riportato i dettagli sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="4f0cc-111">Per altre informazioni, vedere il riferimento all'API REST per la fatturazione di Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( nella libreria Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="4f0cc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f0cc-112">EXAMPLES</span></span>

### <span data-ttu-id="4f0cc-113">Esempio 1: Recuperare i dati dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="4f0cc-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="4f0cc-114">Questo comando recupera i dati di utilizzo segnalati per l'abbonamento tra il 2/5/2015 e il 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="4f0cc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f0cc-115">PARAMETERS</span></span>

### <span data-ttu-id="4f0cc-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="4f0cc-116">-AggregationGranularity</span></span>
<span data-ttu-id="4f0cc-117">Specifica la precisione di aggregazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="4f0cc-118">I valori validi sono: Ogni giorno e Ogni ora.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="4f0cc-119">Il valore predefinito è Giornaliero.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cc-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="4f0cc-120">-ContinuationToken</span></span>
<span data-ttu-id="4f0cc-121">Specifica il token di continuazione recuperato dal corpo della risposta nella chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="4f0cc-122">Per un set di risultati di grandi dimensioni, le risposte vengono paginate usando token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="4f0cc-123">Il token di continuazione funge da segnalibro per lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="4f0cc-124">Se non si specifica questo parametro, i dati vengono recuperati dall'inizio del giorno o dell'ora specificata in *ReportedStartTime.*</span><span class="sxs-lookup"><span data-stu-id="4f0cc-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="4f0cc-125">È consigliabile seguire il collegamento successivo nella risposta alla pagina, anche se i dati sono.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="4f0cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0cc-126">-DefaultProfile</span></span>
<span data-ttu-id="4f0cc-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cc-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="4f0cc-128">-ReportedEndTime</span></span>
<span data-ttu-id="4f0cc-129">Specifica l'ora di fine segnalata per la registrazione dell'utilizzo delle risorse nel sistema di fatturazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="4f0cc-130">Azure è un sistema distribuito che si estende su più data center in tutto il mondo, quindi c'è un ritardo tra il momento in cui la risorsa è stata effettivamente consumata, ovvero il tempo di utilizzo delle risorse e il momento in cui l'evento di utilizzo ha raggiunto il sistema di fatturazione, ovvero il tempo di utilizzo delle risorse segnalato.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="4f0cc-131">Per ottenere tutti gli eventi di utilizzo per una sottoscrizione riportati per un periodo di tempo, eseguire una query in base al tempo segnalato.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="4f0cc-132">Anche se si esegue una query in base al tempo segnalato, il cmdlet aggrega i dati delle risposte in base al tempo di utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="4f0cc-133">I dati sull'utilizzo delle risorse sono il pivot utile per l'analisi dei dati.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="4f0cc-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="4f0cc-134">-ReportedStartTime</span></span>
<span data-ttu-id="4f0cc-135">Specifica l'ora di inizio segnalata per la registrazione dell'utilizzo delle risorse nel sistema di fatturazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="4f0cc-136">-Mostra dettagli</span><span class="sxs-lookup"><span data-stu-id="4f0cc-136">-ShowDetails</span></span>
<span data-ttu-id="4f0cc-137">Indica se questo cmdlet restituisce dettagli a livello di istanza con i dati di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="4f0cc-138">Il valore predefinito è $True.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-138">The default value is $True.</span></span>
<span data-ttu-id="4f0cc-139">Se $False, il servizio aggrega i risultati sul lato server, quindi restituisce meno gruppi di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="4f0cc-140">Ad esempio, se si eseguono tre siti Web, per impostazione predefinita vengono visualizzati tre elementi per l'utilizzo dei siti Web.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="4f0cc-141">Tuttavia, quando il valore è $False, tutti i dati per lo stesso **subscriptionId,** **meterId,** **usageStartTime** e **usageEndTime** vengono compressi in una singola voce.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0cc-142">CommonParameters</span></span>
<span data-ttu-id="4f0cc-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f0cc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0cc-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f0cc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0cc-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f0cc-145">INPUTS</span></span>

### <span data-ttu-id="4f0cc-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f0cc-146">None</span></span>

## <span data-ttu-id="4f0cc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f0cc-147">OUTPUTS</span></span>

### <span data-ttu-id="4f0cc-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="4f0cc-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="4f0cc-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f0cc-149">NOTES</span></span>

## <span data-ttu-id="4f0cc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f0cc-150">RELATED LINKS</span></span>
