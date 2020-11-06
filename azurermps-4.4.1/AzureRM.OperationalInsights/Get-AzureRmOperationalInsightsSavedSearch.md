---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 4daf2a86515522c3843d5d0225c133f0ff3686ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519558"
---
# <span data-ttu-id="ae2c2-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ae2c2-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ae2c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2c2-103">Restituisce tutte le ricerche salvate per un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae2c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae2c2-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae2c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ae2c2-106">Il cmdlet **Get-AzureRmOperationalInsightsSavedSearch** restituisce tutte le ricerche salvate di un'area di lavoro specificata nel gruppo di risorse specificato se non si specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="ae2c2-107">Se si specifica un ID di ricerca salvato, viene restituita la ricerca salvata corrispondente a tale ID.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="ae2c2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae2c2-108">EXAMPLES</span></span>

### <span data-ttu-id="ae2c2-109">Esempio 1: ottenere tutte le ricerche salvate per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ae2c2-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ae2c2-110">Questo comando consente di ottenere tutte le risorse salvate associate a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="ae2c2-111">Esempio 2: ottenere una ricerca salvata specifica in base all'ID</span><span class="sxs-lookup"><span data-stu-id="ae2c2-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="ae2c2-112">Questo comando consente di ottenere una ricerca salvata specifica in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="ae2c2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="ae2c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="ae2c2-115">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-115">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ae2c2-116">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ae2c2-116">-SavedSearchId</span></span>
<span data-ttu-id="ae2c2-117">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-117">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="ae2c2-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ae2c2-118">-WorkspaceName</span></span>
<span data-ttu-id="ae2c2-119">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-119">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="ae2c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2c2-120">-DefaultProfile</span></span>
<span data-ttu-id="ae2c2-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae2c2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2c2-122">CommonParameters</span></span>
<span data-ttu-id="ae2c2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2c2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2c2-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2c2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2c2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae2c2-125">INPUTS</span></span>

## <span data-ttu-id="ae2c2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae2c2-126">OUTPUTS</span></span>

### <span data-ttu-id="ae2c2-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="ae2c2-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="ae2c2-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="ae2c2-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="ae2c2-129">Note</span><span class="sxs-lookup"><span data-stu-id="ae2c2-129">NOTES</span></span>

## <span data-ttu-id="ae2c2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae2c2-130">RELATED LINKS</span></span>

[<span data-ttu-id="ae2c2-131">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="ae2c2-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


