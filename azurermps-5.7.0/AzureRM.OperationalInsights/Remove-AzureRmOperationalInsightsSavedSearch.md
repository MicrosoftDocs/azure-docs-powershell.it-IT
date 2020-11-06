---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508111"
---
# <span data-ttu-id="da21c-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="da21c-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="da21c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da21c-102">SYNOPSIS</span></span>
<span data-ttu-id="da21c-103">Rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da21c-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da21c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da21c-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da21c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da21c-105">DESCRIPTION</span></span>
<span data-ttu-id="da21c-106">Il cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da21c-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="da21c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da21c-107">EXAMPLES</span></span>

### <span data-ttu-id="da21c-108">Esempio 1: rimuovere una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="da21c-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="da21c-109">Questo comando rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da21c-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="da21c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da21c-110">PARAMETERS</span></span>

### <span data-ttu-id="da21c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da21c-111">-DefaultProfile</span></span>
<span data-ttu-id="da21c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da21c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da21c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da21c-113">-ResourceGroupName</span></span>
<span data-ttu-id="da21c-114">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da21c-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="da21c-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="da21c-115">-SavedSearchId</span></span>
<span data-ttu-id="da21c-116">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="da21c-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="da21c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da21c-117">-WorkspaceName</span></span>
<span data-ttu-id="da21c-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da21c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="da21c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da21c-119">-Confirm</span></span>
<span data-ttu-id="da21c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da21c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da21c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da21c-121">-WhatIf</span></span>
<span data-ttu-id="da21c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da21c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da21c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da21c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da21c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da21c-124">CommonParameters</span></span>
<span data-ttu-id="da21c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da21c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da21c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da21c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da21c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da21c-127">INPUTS</span></span>

### <span data-ttu-id="da21c-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da21c-128">None</span></span>
<span data-ttu-id="da21c-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="da21c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da21c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da21c-130">OUTPUTS</span></span>

## <span data-ttu-id="da21c-131">Note</span><span class="sxs-lookup"><span data-stu-id="da21c-131">NOTES</span></span>

## <span data-ttu-id="da21c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da21c-132">RELATED LINKS</span></span>

[<span data-ttu-id="da21c-133">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="da21c-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


