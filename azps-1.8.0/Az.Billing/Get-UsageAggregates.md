---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 35324b558d673f71d9007a63c578d77d69a5f338
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852290"
---
# <span data-ttu-id="14db9-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="14db9-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="14db9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14db9-102">SYNOPSIS</span></span>
<span data-ttu-id="14db9-103">Ottiene i dettagli di utilizzo dell'abbonamento Azure segnalati.</span><span class="sxs-lookup"><span data-stu-id="14db9-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="14db9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14db9-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14db9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14db9-105">DESCRIPTION</span></span>
<span data-ttu-id="14db9-106">Il cmdlet **Get-UsageAggregates** ottiene i dati di utilizzo degli abbonamenti di Azure aggregati in base alle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="14db9-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="14db9-107">Orari di inizio e fine di quando è stato segnalato l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="14db9-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="14db9-108">Precisione di aggregazione, giornaliera o oraria.</span><span class="sxs-lookup"><span data-stu-id="14db9-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="14db9-109">Dettagli del livello di istanza per più istanze della stessa risorsa.</span><span class="sxs-lookup"><span data-stu-id="14db9-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="14db9-110">Per risultati coerenti, i dati restituiti si basano su quando i dettagli sull'utilizzo sono stati segnalati dalla risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="14db9-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="14db9-111">Per altre informazioni, vedi riferimenti alle API REST di Azure Billing https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="14db9-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="14db9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14db9-112">EXAMPLES</span></span>

### <span data-ttu-id="14db9-113">Esempio 1: recuperare i dati dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="14db9-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="14db9-114">Questo comando recupera i dati di utilizzo segnalati per l'abbonamento tra 5/2/2015 e 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="14db9-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="14db9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14db9-115">PARAMETERS</span></span>

### <span data-ttu-id="14db9-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="14db9-116">-AggregationGranularity</span></span>
<span data-ttu-id="14db9-117">Specifica la precisione di aggregazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="14db9-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="14db9-118">I valori validi sono: ogni giorno e ogni ora.</span><span class="sxs-lookup"><span data-stu-id="14db9-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="14db9-119">Il valore predefinito è Daily.</span><span class="sxs-lookup"><span data-stu-id="14db9-119">The default value is Daily.</span></span>

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

### <span data-ttu-id="14db9-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="14db9-120">-ContinuationToken</span></span>
<span data-ttu-id="14db9-121">Specifica il token di continuazione recuperato dal corpo della risposta nella chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="14db9-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="14db9-122">Per un set di risultati di grandi dimensioni, le risposte vengono inpaginate usando i token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="14db9-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="14db9-123">Il token di continuazione funge da segnalibro per lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="14db9-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="14db9-124">Se non specifichi questo parametro, i dati vengono recuperati dall'inizio del giorno o dell'ora specificati in *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="14db9-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="14db9-125">È consigliabile seguire il collegamento successivo nella pagina Response to anche se i dati.</span><span class="sxs-lookup"><span data-stu-id="14db9-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="14db9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14db9-126">-DefaultProfile</span></span>
<span data-ttu-id="14db9-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14db9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14db9-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="14db9-128">-ReportedEndTime</span></span>
<span data-ttu-id="14db9-129">Specifica l'ora di fine segnalata per quando l'utilizzo delle risorse è stato registrato nel sistema di fatturazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="14db9-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="14db9-130">Azure è un sistema distribuito che include più datacenter in tutto il mondo, quindi c'è un ritardo tra il momento in cui la risorsa è stata effettivamente consumata, ovvero il tempo di utilizzo delle risorse, e quando l'evento di utilizzo ha raggiunto il sistema di fatturazione, ovvero l'utilizzo delle risorse indicato nel tempo.</span><span class="sxs-lookup"><span data-stu-id="14db9-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="14db9-131">Per ottenere tutti gli eventi di utilizzo per un abbonamento segnalato per un periodo di tempo, è possibile eseguire una query in base al tempo segnalato.</span><span class="sxs-lookup"><span data-stu-id="14db9-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="14db9-132">Anche se si esegue una query in base al tempo segnalato, il cmdlet aggrega i dati di risposta in base al tempo di utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="14db9-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="14db9-133">I dati sull'utilizzo delle risorse sono il perno utile per analizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="14db9-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="14db9-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="14db9-134">-ReportedStartTime</span></span>
<span data-ttu-id="14db9-135">Specifica l'ora di inizio riportata per quando l'utilizzo delle risorse è stato registrato nel sistema di fatturazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="14db9-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="14db9-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="14db9-136">-ShowDetails</span></span>
<span data-ttu-id="14db9-137">Indica se questo cmdlet restituisce i dettagli a livello di istanza con i dati sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="14db9-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="14db9-138">Il valore predefinito è $True.</span><span class="sxs-lookup"><span data-stu-id="14db9-138">The default value is $True.</span></span>
<span data-ttu-id="14db9-139">Se $False, il servizio aggrega i risultati sul lato server e quindi restituisce meno gruppi aggregati.</span><span class="sxs-lookup"><span data-stu-id="14db9-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="14db9-140">Ad esempio, se stai usando tre siti Web, per impostazione predefinita otterrai tre voci per il consumo del sito Web.</span><span class="sxs-lookup"><span data-stu-id="14db9-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="14db9-141">Tuttavia, quando il valore è $False, tutti i dati per lo stesso **SubscriptionId** , **meterId** , **usageStartTime** e **usageEndTime** vengono compressi in una singola voce.</span><span class="sxs-lookup"><span data-stu-id="14db9-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

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

### <span data-ttu-id="14db9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14db9-142">CommonParameters</span></span>
<span data-ttu-id="14db9-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14db9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14db9-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14db9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14db9-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14db9-145">INPUTS</span></span>

### <span data-ttu-id="14db9-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14db9-146">None</span></span>

## <span data-ttu-id="14db9-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14db9-147">OUTPUTS</span></span>

### <span data-ttu-id="14db9-148">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="14db9-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="14db9-149">Note</span><span class="sxs-lookup"><span data-stu-id="14db9-149">NOTES</span></span>

## <span data-ttu-id="14db9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14db9-150">RELATED LINKS</span></span>
