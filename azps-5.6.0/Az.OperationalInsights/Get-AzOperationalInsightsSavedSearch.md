---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958094"
---
# <span data-ttu-id="c9129-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c9129-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c9129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9129-102">SYNOPSIS</span></span>
<span data-ttu-id="c9129-103">Restituisce tutte le ricerche salvate per un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c9129-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="c9129-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9129-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9129-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9129-105">DESCRIPTION</span></span>
<span data-ttu-id="c9129-106">Il cmdlet **Get-AzOperationalInsightsSavedSearch** restituisce tutte le ricerche salvate per un'area di lavoro specificata all'interno del gruppo di risorse specificata se non si specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="c9129-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="c9129-107">Se si specifica un ID di ricerca salvato, viene restituita la ricerca salvata corrispondente a tale ID.</span><span class="sxs-lookup"><span data-stu-id="c9129-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="c9129-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9129-108">EXAMPLES</span></span>

### <span data-ttu-id="c9129-109">Esempio 1: Recuperare tutte le ricerche salvate per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9129-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c9129-110">Questo comando recupera tutte le risorse salvate associate a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9129-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="c9129-111">Esempio 2: Ottenere una ricerca salvata specifica in base all'ID</span><span class="sxs-lookup"><span data-stu-id="c9129-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="c9129-112">Questo comando ottiene una ricerca salvata specifica in base al relativo ID.</span><span class="sxs-lookup"><span data-stu-id="c9129-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="c9129-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9129-113">PARAMETERS</span></span>

### <span data-ttu-id="c9129-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9129-114">-DefaultProfile</span></span>
<span data-ttu-id="c9129-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c9129-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9129-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9129-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9129-117">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9129-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c9129-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c9129-118">-SavedSearchId</span></span>
<span data-ttu-id="c9129-119">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="c9129-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9129-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9129-120">-WorkspaceName</span></span>
<span data-ttu-id="c9129-121">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9129-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c9129-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9129-122">CommonParameters</span></span>
<span data-ttu-id="c9129-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9129-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9129-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9129-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9129-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9129-125">INPUTS</span></span>

### <span data-ttu-id="c9129-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c9129-126">System.String</span></span>

## <span data-ttu-id="c9129-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9129-127">OUTPUTS</span></span>

### <span data-ttu-id="c9129-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9129-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="c9129-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9129-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="c9129-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9129-130">NOTES</span></span>

## <span data-ttu-id="c9129-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9129-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9129-132">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="c9129-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


