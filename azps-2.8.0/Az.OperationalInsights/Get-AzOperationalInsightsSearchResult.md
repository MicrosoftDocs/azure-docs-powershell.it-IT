---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855501"
---
# <span data-ttu-id="27a59-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="27a59-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="27a59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27a59-102">SYNOPSIS</span></span>
<span data-ttu-id="27a59-103">Restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="27a59-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="27a59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27a59-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27a59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27a59-105">DESCRIPTION</span></span>
<span data-ttu-id="27a59-106">Il cmdlet **Get-AzOperationalInsightsSearchResult** restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="27a59-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="27a59-107">Puoi accedere allo stato della ricerca nella proprietà Metadata dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="27a59-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="27a59-108">Se lo stato è in sospeso, la ricerca non è stata completata e i risultati verranno dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="27a59-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="27a59-109">Puoi recuperare i risultati della ricerca dalla proprietà Value dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="27a59-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="27a59-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27a59-110">EXAMPLES</span></span>

### <span data-ttu-id="27a59-111">Esempio 1: ottenere i risultati della ricerca tramite una query</span><span class="sxs-lookup"><span data-stu-id="27a59-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="27a59-112">Questo comando ottiene tutti i risultati della ricerca usando una query.</span><span class="sxs-lookup"><span data-stu-id="27a59-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="27a59-113">Esempio 2: ottenere i risultati della ricerca usando un ID</span><span class="sxs-lookup"><span data-stu-id="27a59-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="27a59-114">Questo comando ottiene i risultati della ricerca usando un ID.</span><span class="sxs-lookup"><span data-stu-id="27a59-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="27a59-115">Esempio 3: attendere il completamento di una ricerca prima di visualizzare i risultati</span><span class="sxs-lookup"><span data-stu-id="27a59-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="27a59-116">Questo script avvia una ricerca e attende finché non viene completata prima di visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="27a59-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="27a59-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27a59-117">PARAMETERS</span></span>

### <span data-ttu-id="27a59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a59-118">-DefaultProfile</span></span>
<span data-ttu-id="27a59-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27a59-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27a59-120">-Fine</span><span class="sxs-lookup"><span data-stu-id="27a59-120">-End</span></span>
<span data-ttu-id="27a59-121">Fine dell'intervallo di tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="27a59-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-122">-ID</span><span class="sxs-lookup"><span data-stu-id="27a59-122">-Id</span></span>
<span data-ttu-id="27a59-123">Se viene assegnato un ID, i risultati della ricerca per tale ID verranno recuperati usando i parametri di query originali.</span><span class="sxs-lookup"><span data-stu-id="27a59-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-124">-Posthighlight</span><span class="sxs-lookup"><span data-stu-id="27a59-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-125">-Prehighlight</span><span class="sxs-lookup"><span data-stu-id="27a59-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-126">-Query</span><span class="sxs-lookup"><span data-stu-id="27a59-126">-Query</span></span>
<span data-ttu-id="27a59-127">Query di ricerca che verrà eseguita.</span><span class="sxs-lookup"><span data-stu-id="27a59-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a59-128">-ResourceGroupName</span></span>
<span data-ttu-id="27a59-129">Nome del gruppo di risorse che contiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="27a59-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-130">-Inizio</span><span class="sxs-lookup"><span data-stu-id="27a59-130">-Start</span></span>
<span data-ttu-id="27a59-131">Inizio dell'intervallo di tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="27a59-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-132">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="27a59-132">-Top</span></span>
<span data-ttu-id="27a59-133">Numero massimo di risultati da restituire, limitato a 5000.</span><span class="sxs-lookup"><span data-stu-id="27a59-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27a59-134">-WorkspaceName</span></span>
<span data-ttu-id="27a59-135">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="27a59-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a59-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a59-136">CommonParameters</span></span>
<span data-ttu-id="27a59-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a59-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a59-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a59-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a59-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27a59-139">INPUTS</span></span>

### <span data-ttu-id="27a59-140">System. String</span><span class="sxs-lookup"><span data-stu-id="27a59-140">System.String</span></span>

### <span data-ttu-id="27a59-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="27a59-141">System.Int64</span></span>

### <span data-ttu-id="27a59-142">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27a59-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="27a59-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27a59-143">OUTPUTS</span></span>

### <span data-ttu-id="27a59-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="27a59-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="27a59-145">Note</span><span class="sxs-lookup"><span data-stu-id="27a59-145">NOTES</span></span>

## <span data-ttu-id="27a59-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27a59-146">RELATED LINKS</span></span>

[<span data-ttu-id="27a59-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="27a59-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


