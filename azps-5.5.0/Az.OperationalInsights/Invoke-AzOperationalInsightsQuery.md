---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202339"
---
# <span data-ttu-id="d2abf-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="d2abf-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="d2abf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2abf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2abf-103">Restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="d2abf-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="d2abf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2abf-104">SYNTAX</span></span>

### <span data-ttu-id="d2abf-105">ByWorkspaceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2abf-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2abf-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2abf-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2abf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d2abf-107">DESCRIPTION</span></span>
<span data-ttu-id="d2abf-108">Il cmdlet **Invoke-AzOperationalInsightsQuery** restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="d2abf-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="d2abf-109">È possibile accedere allo stato della ricerca nella proprietà Metadati dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="d2abf-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="d2abf-110">Se lo stato è In sospeso, la ricerca non è stata completata e i risultati saranno provenienti dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="d2abf-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="d2abf-111">È possibile recuperare i risultati della ricerca dalla proprietà Value dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="d2abf-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="d2abf-112">Vedere i dettagli dei limiti di query generali qui: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language .</span><span class="sxs-lookup"><span data-stu-id="d2abf-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="d2abf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2abf-113">EXAMPLES</span></span>

### <span data-ttu-id="d2abf-114">Esempio 1: Ottenere i risultati della ricerca con una query</span><span class="sxs-lookup"><span data-stu-id="d2abf-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="d2abf-115">Una volta richiamato, $queryResults.Results conterrà tutte le righe risultanti dalla query.</span><span class="sxs-lookup"><span data-stu-id="d2abf-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="d2abf-116">Esempio 2: Convertire $results. Risultato I Possono essere restituito da una matrice</span><span class="sxs-lookup"><span data-stu-id="d2abf-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="d2abf-117">Alcune query possono comportare la visualizzazione di set di dati molto grandi.</span><span class="sxs-lookup"><span data-stu-id="d2abf-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="d2abf-118">Per questo, il comportamento predefinito del cmdlet è la restituzione di un valore I Dello stesso tipo per ridurre i costi di memoria.</span><span class="sxs-lookup"><span data-stu-id="d2abf-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="d2abf-119">Se si preferisce avere una matrice di risultati, è possibile usare il metodo di estensione TIR.CIE.ToArray() per convertire IArray in una matrice.</span><span class="sxs-lookup"><span data-stu-id="d2abf-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="d2abf-120">Esempio 3: Ottenere i risultati della ricerca usando una query su un intervallo di tempo specifico</span><span class="sxs-lookup"><span data-stu-id="d2abf-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="d2abf-121">I risultati di questa query saranno limitati alle ultime 24 ore.</span><span class="sxs-lookup"><span data-stu-id="d2abf-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="d2abf-122">Esempio 4: Includere le statistiche & rendering nel risultato della query</span><span class="sxs-lookup"><span data-stu-id="d2abf-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="d2abf-123">Vedi [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) per informazioni dettagliate sul rendering e le statistiche.</span><span class="sxs-lookup"><span data-stu-id="d2abf-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="d2abf-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2abf-124">PARAMETERS</span></span>

### <span data-ttu-id="d2abf-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2abf-125">-AsJob</span></span>
<span data-ttu-id="d2abf-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d2abf-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2abf-127">-DefaultProfile</span></span>
<span data-ttu-id="d2abf-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2abf-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2abf-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="d2abf-129">-IncludeRender</span></span>
<span data-ttu-id="d2abf-130">Se si specifica, le informazioni di rendering per le query metriche verranno incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="d2abf-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="d2abf-131">-IncludeStatistics</span></span>
<span data-ttu-id="d2abf-132">Se specificato, le statistiche della query verranno incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="d2abf-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-133">-Query</span><span class="sxs-lookup"><span data-stu-id="d2abf-133">-Query</span></span>
<span data-ttu-id="d2abf-134">Query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d2abf-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="d2abf-135">-Timespan</span></span>
<span data-ttu-id="d2abf-136">L'intervallo di tempo a cui deve essere associata la query.</span><span class="sxs-lookup"><span data-stu-id="d2abf-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="d2abf-137">-Wait</span></span>
<span data-ttu-id="d2abf-138">Imposta un limite superiore per la quantità di tempo di elaborazione della query da parte del server.</span><span class="sxs-lookup"><span data-stu-id="d2abf-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="d2abf-139">Vedere: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="d2abf-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-140">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d2abf-140">-Workspace</span></span>
<span data-ttu-id="d2abf-141">Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d2abf-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d2abf-142">-WorkspaceId</span></span>
<span data-ttu-id="d2abf-143">ID dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d2abf-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2abf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2abf-144">CommonParameters</span></span>
<span data-ttu-id="d2abf-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2abf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2abf-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2abf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2abf-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="d2abf-147">INPUTS</span></span>

### <span data-ttu-id="d2abf-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2abf-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="d2abf-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2abf-149">OUTPUTS</span></span>

### <span data-ttu-id="d2abf-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="d2abf-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="d2abf-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="d2abf-151">NOTES</span></span>

## <span data-ttu-id="d2abf-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2abf-152">RELATED LINKS</span></span>
