---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512455"
---
# <span data-ttu-id="3f3a6-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3f3a6-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3f3a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3a6-103">Restituisce tutte le ricerche salvate per un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f3a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f3a6-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f3a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="3f3a6-106">Il cmdlet **Get-AzureRmOperationalInsightsSavedSearch** restituisce tutte le ricerche salvate di un'area di lavoro specificata nel gruppo di risorse specificato se non si specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="3f3a6-107">Se si specifica un ID di ricerca salvato, viene restituita la ricerca salvata corrispondente a tale ID.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="3f3a6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f3a6-108">EXAMPLES</span></span>

### <span data-ttu-id="3f3a6-109">Esempio 1: ottenere tutte le ricerche salvate per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3f3a6-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3f3a6-110">Questo comando consente di ottenere tutte le risorse salvate associate a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="3f3a6-111">Esempio 2: ottenere una ricerca salvata specifica in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3f3a6-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="3f3a6-112">Questo comando consente di ottenere una ricerca salvata specifica in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="3f3a6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f3a6-113">PARAMETERS</span></span>

### <span data-ttu-id="3f3a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3a6-114">-DefaultProfile</span></span>
<span data-ttu-id="3f3a6-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3f3a6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f3a6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f3a6-116">-ResourceGroupName</span></span>
<span data-ttu-id="3f3a6-117">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3f3a6-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3f3a6-118">-SavedSearchId</span></span>
<span data-ttu-id="3f3a6-119">Specifica un ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f3a6-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f3a6-120">-WorkspaceName</span></span>
<span data-ttu-id="3f3a6-121">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="3f3a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3a6-122">CommonParameters</span></span>
<span data-ttu-id="3f3a6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3a6-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3a6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3a6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f3a6-125">INPUTS</span></span>

### <span data-ttu-id="3f3a6-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f3a6-126">None</span></span>
<span data-ttu-id="3f3a6-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f3a6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f3a6-128">OUTPUTS</span></span>

### <span data-ttu-id="3f3a6-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="3f3a6-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="3f3a6-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="3f3a6-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="3f3a6-131">Note</span><span class="sxs-lookup"><span data-stu-id="3f3a6-131">NOTES</span></span>

## <span data-ttu-id="3f3a6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f3a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f3a6-133">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="3f3a6-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


