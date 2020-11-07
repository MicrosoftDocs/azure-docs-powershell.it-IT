---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 161365ee947a118221fa922ab9e7d05486d3908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687133"
---
# <span data-ttu-id="bcbe3-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="bcbe3-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="bcbe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbe3-103">Restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcbe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcbe3-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcbe3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcbe3-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbe3-106">Il cmdlet **Get-AzureRmOperationalInsightsSearchResults** restituisce i risultati della ricerca in base ai parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="bcbe3-107">Puoi accedere allo stato della ricerca nella proprietà Metadata dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="bcbe3-108">Se lo stato è in sospeso, la ricerca non è stata completata e i risultati verranno dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="bcbe3-109">Puoi recuperare i risultati della ricerca dalla proprietà Value dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="bcbe3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcbe3-110">EXAMPLES</span></span>

### <span data-ttu-id="bcbe3-111">Esempio 1: ottenere i risultati della ricerca tramite una query</span><span class="sxs-lookup"><span data-stu-id="bcbe3-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="bcbe3-112">Questo comando ottiene tutti i risultati della ricerca usando una query.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="bcbe3-113">Esempio 2: ottenere i risultati della ricerca usando un ID</span><span class="sxs-lookup"><span data-stu-id="bcbe3-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="bcbe3-114">Questo comando ottiene i risultati della ricerca usando un ID.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="bcbe3-115">Esempio 3: attendere il completamento di una ricerca prima di visualizzare i risultati</span><span class="sxs-lookup"><span data-stu-id="bcbe3-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="bcbe3-116">Questo script avvia una ricerca e attende finché non viene completata prima di visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="bcbe3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcbe3-117">PARAMETERS</span></span>

### <span data-ttu-id="bcbe3-118">-Fine</span><span class="sxs-lookup"><span data-stu-id="bcbe3-118">-End</span></span>
<span data-ttu-id="bcbe3-119">Fine dell'intervallo di tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-119">End of the queried time range.</span></span>

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

### <span data-ttu-id="bcbe3-120">-ID</span><span class="sxs-lookup"><span data-stu-id="bcbe3-120">-Id</span></span>
<span data-ttu-id="bcbe3-121">Se viene assegnato un ID, i risultati della ricerca per tale ID verranno recuperati usando i parametri di query originali.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-121">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="bcbe3-122">-Posthighlight</span><span class="sxs-lookup"><span data-stu-id="bcbe3-122">-PostHighlight</span></span>
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

### <span data-ttu-id="bcbe3-123">-Prehighlight</span><span class="sxs-lookup"><span data-stu-id="bcbe3-123">-PreHighlight</span></span>
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

### <span data-ttu-id="bcbe3-124">-Query</span><span class="sxs-lookup"><span data-stu-id="bcbe3-124">-Query</span></span>
<span data-ttu-id="bcbe3-125">Query di ricerca che verrà eseguita.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-125">The search query that will be executed.</span></span>

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

### <span data-ttu-id="bcbe3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbe3-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcbe3-127">Nome del gruppo di risorse che contiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-127">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="bcbe3-128">-Inizio</span><span class="sxs-lookup"><span data-stu-id="bcbe3-128">-Start</span></span>
<span data-ttu-id="bcbe3-129">Inizio dell'intervallo di tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-129">Start of the queried time range.</span></span>

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

### <span data-ttu-id="bcbe3-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="bcbe3-130">-Top</span></span>
<span data-ttu-id="bcbe3-131">Numero massimo di risultati da restituire, limitato a 5000.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-131">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="bcbe3-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcbe3-132">-WorkspaceName</span></span>
<span data-ttu-id="bcbe3-133">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-133">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="bcbe3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbe3-134">-DefaultProfile</span></span>
<span data-ttu-id="bcbe3-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbe3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbe3-136">CommonParameters</span></span>
<span data-ttu-id="bcbe3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbe3-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbe3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbe3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcbe3-139">INPUTS</span></span>

## <span data-ttu-id="bcbe3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcbe3-140">OUTPUTS</span></span>

### <span data-ttu-id="bcbe3-141">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="bcbe3-141">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="bcbe3-142">L'oggetto **PSSearchGetSearchResultsResponse** include una proprietà Value che include i record restituiti dalla ricerca in formato JSON e un oggetto Metadata che include informazioni sui risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-142">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="bcbe3-143">Note</span><span class="sxs-lookup"><span data-stu-id="bcbe3-143">NOTES</span></span>

## <span data-ttu-id="bcbe3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcbe3-144">RELATED LINKS</span></span>

[<span data-ttu-id="bcbe3-145">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="bcbe3-145">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


