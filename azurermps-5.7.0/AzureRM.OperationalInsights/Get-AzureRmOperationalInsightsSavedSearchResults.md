---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685825"
---
# <span data-ttu-id="19606-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="19606-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="19606-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19606-102">SYNOPSIS</span></span>
<span data-ttu-id="19606-103">Restituisce i risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="19606-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19606-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19606-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19606-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19606-105">DESCRIPTION</span></span>
<span data-ttu-id="19606-106">Il cmdlet **Get-AzureRmOperationalInsightsSavedSearchResults** restituisce i risultati della query specificata dall'ID ricerca.</span><span class="sxs-lookup"><span data-stu-id="19606-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="19606-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19606-107">EXAMPLES</span></span>

### <span data-ttu-id="19606-108">Esempio 1: ottenere tutti i risultati della ricerca per una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="19606-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="19606-109">Questo comando consente di ottenere tutti i risultati della ricerca per una ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="19606-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="19606-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19606-110">PARAMETERS</span></span>

### <span data-ttu-id="19606-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19606-111">-DefaultProfile</span></span>
<span data-ttu-id="19606-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19606-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19606-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19606-113">-ResourceGroupName</span></span>
<span data-ttu-id="19606-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19606-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19606-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="19606-115">-SavedSearchId</span></span>
<span data-ttu-id="19606-116">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="19606-116">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19606-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19606-117">-WorkspaceName</span></span>
<span data-ttu-id="19606-118">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19606-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19606-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19606-119">CommonParameters</span></span>
<span data-ttu-id="19606-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19606-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19606-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19606-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19606-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19606-122">INPUTS</span></span>

### <span data-ttu-id="19606-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19606-123">None</span></span>
<span data-ttu-id="19606-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="19606-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19606-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19606-125">OUTPUTS</span></span>

### <span data-ttu-id="19606-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="19606-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="19606-127">Note</span><span class="sxs-lookup"><span data-stu-id="19606-127">NOTES</span></span>

## <span data-ttu-id="19606-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19606-128">RELATED LINKS</span></span>

[<span data-ttu-id="19606-129">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="19606-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


