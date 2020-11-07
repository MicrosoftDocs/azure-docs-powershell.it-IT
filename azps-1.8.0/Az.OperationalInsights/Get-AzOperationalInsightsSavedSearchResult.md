---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685399"
---
# <span data-ttu-id="1512f-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="1512f-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="1512f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1512f-102">SYNOPSIS</span></span>
<span data-ttu-id="1512f-103">Restituisce i risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="1512f-103">Returns the results from a query.</span></span>

## <span data-ttu-id="1512f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1512f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1512f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1512f-105">DESCRIPTION</span></span>
<span data-ttu-id="1512f-106">Il cmdlet **Get-AzOperationalInsightsSavedSearchResult** restituisce i risultati della query specificata dall'ID ricerca.</span><span class="sxs-lookup"><span data-stu-id="1512f-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="1512f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1512f-107">EXAMPLES</span></span>

### <span data-ttu-id="1512f-108">Esempio 1: ottenere tutti i risultati della ricerca per una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="1512f-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="1512f-109">Questo comando consente di ottenere tutti i risultati della ricerca per una ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="1512f-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="1512f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1512f-110">PARAMETERS</span></span>

### <span data-ttu-id="1512f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1512f-111">-DefaultProfile</span></span>
<span data-ttu-id="1512f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1512f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1512f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1512f-113">-ResourceGroupName</span></span>
<span data-ttu-id="1512f-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1512f-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="1512f-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1512f-115">-SavedSearchId</span></span>
<span data-ttu-id="1512f-116">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="1512f-116">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1512f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1512f-117">-WorkspaceName</span></span>
<span data-ttu-id="1512f-118">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1512f-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="1512f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1512f-119">CommonParameters</span></span>
<span data-ttu-id="1512f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1512f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1512f-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1512f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1512f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1512f-122">INPUTS</span></span>

### <span data-ttu-id="1512f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1512f-123">System.String</span></span>

## <span data-ttu-id="1512f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1512f-124">OUTPUTS</span></span>

### <span data-ttu-id="1512f-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="1512f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="1512f-126">Note</span><span class="sxs-lookup"><span data-stu-id="1512f-126">NOTES</span></span>

## <span data-ttu-id="1512f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1512f-127">RELATED LINKS</span></span>

[<span data-ttu-id="1512f-128">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="1512f-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


