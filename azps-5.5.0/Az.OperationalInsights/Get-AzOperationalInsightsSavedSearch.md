---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179238"
---
# <span data-ttu-id="3a250-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3a250-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3a250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a250-102">SYNOPSIS</span></span>
<span data-ttu-id="3a250-103">Restituisce tutte le ricerche salvate per un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="3a250-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="3a250-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a250-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a250-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a250-105">DESCRIPTION</span></span>
<span data-ttu-id="3a250-106">Il cmdlet **Get-AzOperationalInsightsSavedSearch** restituisce tutte le ricerche salvate per un'area di lavoro specificata all'interno del gruppo di risorse specificata se non si specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="3a250-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="3a250-107">Se si specifica un ID di ricerca salvato, viene restituita la ricerca salvata corrispondente a tale ID.</span><span class="sxs-lookup"><span data-stu-id="3a250-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="3a250-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a250-108">EXAMPLES</span></span>

### <span data-ttu-id="3a250-109">Esempio 1: Recuperare tutte le ricerche salvate per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3a250-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3a250-110">Questo comando recupera tutte le risorse salvate associate a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3a250-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="3a250-111">Esempio 2: Ottenere una ricerca salvata specifica in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3a250-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="3a250-112">Questo comando ottiene una ricerca salvata specifica in base al relativo ID.</span><span class="sxs-lookup"><span data-stu-id="3a250-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="3a250-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a250-113">PARAMETERS</span></span>

### <span data-ttu-id="3a250-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a250-114">-DefaultProfile</span></span>
<span data-ttu-id="3a250-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3a250-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a250-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a250-116">-ResourceGroupName</span></span>
<span data-ttu-id="3a250-117">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3a250-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3a250-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3a250-118">-SavedSearchId</span></span>
<span data-ttu-id="3a250-119">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="3a250-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="3a250-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a250-120">-WorkspaceName</span></span>
<span data-ttu-id="3a250-121">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3a250-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="3a250-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a250-122">CommonParameters</span></span>
<span data-ttu-id="3a250-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a250-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a250-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a250-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a250-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a250-125">INPUTS</span></span>

### <span data-ttu-id="3a250-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3a250-126">System.String</span></span>

## <span data-ttu-id="3a250-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a250-127">OUTPUTS</span></span>

### <span data-ttu-id="3a250-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="3a250-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="3a250-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="3a250-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="3a250-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a250-130">NOTES</span></span>

## <span data-ttu-id="3a250-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a250-131">RELATED LINKS</span></span>

[<span data-ttu-id="3a250-132">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="3a250-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


