---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 1df2e8fc82ba071692f8c7b5bf677d275c429323
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855485"
---
# <span data-ttu-id="60587-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="60587-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="60587-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60587-102">SYNOPSIS</span></span>
<span data-ttu-id="60587-103">Restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="60587-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="60587-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60587-104">SYNTAX</span></span>

### <span data-ttu-id="60587-105">ByWorkspaceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60587-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60587-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60587-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60587-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60587-107">DESCRIPTION</span></span>
<span data-ttu-id="60587-108">Il cmdlet **Invoke-AzOperationalInsightsQuery** restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="60587-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="60587-109">Puoi accedere allo stato della ricerca nella proprietà Metadata dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="60587-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="60587-110">Se lo stato è in sospeso, la ricerca non è stata completata e i risultati verranno dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="60587-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="60587-111">Puoi recuperare i risultati della ricerca dalla proprietà Value dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="60587-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="60587-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60587-112">EXAMPLES</span></span>

### <span data-ttu-id="60587-113">Esempio 1: ottenere i risultati della ricerca tramite una query</span><span class="sxs-lookup"><span data-stu-id="60587-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="60587-114">Una volta richiamato, $queryResults. Results conterrà tutte le righe risultanti della query.</span><span class="sxs-lookup"><span data-stu-id="60587-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="60587-115">Esempio 2: convertire $results. IEnumerable risultato in una matrice</span><span class="sxs-lookup"><span data-stu-id="60587-115">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="60587-116">Alcune query possono determinare la restituzione di set di dati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="60587-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="60587-117">Per questo motivo, il comportamento predefinito del cmdlet consiste nel restituire un oggetto IEnumerable per ridurre i costi di memoria.</span><span class="sxs-lookup"><span data-stu-id="60587-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="60587-118">Se preferisci avere una matrice di risultati, puoi usare il metodo di estensione Enumerable. ToArray () LINQ per convertire l'oggetto IEnumerable in una matrice.</span><span class="sxs-lookup"><span data-stu-id="60587-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="60587-119">Esempio 3: ottenere i risultati della ricerca usando una query su un intervallo di tempo specifico</span><span class="sxs-lookup"><span data-stu-id="60587-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="60587-120">I risultati della query verranno limitati alle ultime 24 ore.</span><span class="sxs-lookup"><span data-stu-id="60587-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="60587-121">Esempio 4: includere il rendering & le statistiche nel risultato della query</span><span class="sxs-lookup"><span data-stu-id="60587-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="60587-122">Vedere [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) per informazioni dettagliate sulle informazioni di rendering e statistiche.</span><span class="sxs-lookup"><span data-stu-id="60587-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="60587-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60587-123">PARAMETERS</span></span>

### <span data-ttu-id="60587-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60587-124">-AsJob</span></span>
<span data-ttu-id="60587-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60587-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60587-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60587-126">-DefaultProfile</span></span>
<span data-ttu-id="60587-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60587-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60587-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="60587-128">-IncludeRender</span></span>
<span data-ttu-id="60587-129">Se specificato, il rendering delle informazioni per le query metriche verrà incluso nella risposta.</span><span class="sxs-lookup"><span data-stu-id="60587-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="60587-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="60587-130">-IncludeStatistics</span></span>
<span data-ttu-id="60587-131">Se specificato, le statistiche di query verranno incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="60587-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="60587-132">-Query</span><span class="sxs-lookup"><span data-stu-id="60587-132">-Query</span></span>
<span data-ttu-id="60587-133">Query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="60587-133">The query to execute.</span></span>

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

### <span data-ttu-id="60587-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="60587-134">-Timespan</span></span>
<span data-ttu-id="60587-135">TimeSpan a cui associare la query.</span><span class="sxs-lookup"><span data-stu-id="60587-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="60587-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="60587-136">-Wait</span></span>
<span data-ttu-id="60587-137">Inserisce un limite superiore per la quantità di tempo che il server spenderà per l'elaborazione della query.</span><span class="sxs-lookup"><span data-stu-id="60587-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="60587-138">Vedere https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="60587-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="60587-139">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="60587-139">-Workspace</span></span>
<span data-ttu-id="60587-140">Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="60587-140">The workspace</span></span>

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

### <span data-ttu-id="60587-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="60587-141">-WorkspaceId</span></span>
<span data-ttu-id="60587-142">ID area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="60587-142">The workspace ID.</span></span>

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

### <span data-ttu-id="60587-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60587-143">CommonParameters</span></span>
<span data-ttu-id="60587-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60587-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60587-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60587-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60587-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60587-146">INPUTS</span></span>

### <span data-ttu-id="60587-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="60587-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="60587-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60587-148">OUTPUTS</span></span>

### <span data-ttu-id="60587-149">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="60587-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="60587-150">Note</span><span class="sxs-lookup"><span data-stu-id="60587-150">NOTES</span></span>

## <span data-ttu-id="60587-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60587-151">RELATED LINKS</span></span>
