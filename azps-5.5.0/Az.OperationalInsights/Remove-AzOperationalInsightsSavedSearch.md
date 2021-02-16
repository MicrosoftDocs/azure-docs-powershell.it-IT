---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184070"
---
# <span data-ttu-id="e1bb0-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e1bb0-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e1bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bb0-103">Rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e1bb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1bb0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1bb0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bb0-106">Il cmdlet **Remove-AzOperationalInsightsSavedSearch** rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e1bb0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bb0-108">Esempio 1: Rimuovere una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="e1bb0-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="e1bb0-109">Questo comando rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e1bb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1bb0-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bb0-111">-DefaultProfile</span></span>
<span data-ttu-id="e1bb0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e1bb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1bb0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bb0-113">-ResourceGroupName</span></span>
<span data-ttu-id="e1bb0-114">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e1bb0-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e1bb0-115">-SavedSearchId</span></span>
<span data-ttu-id="e1bb0-116">Specifica l'ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="e1bb0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1bb0-117">-WorkspaceName</span></span>
<span data-ttu-id="e1bb0-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e1bb0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1bb0-119">-Confirm</span></span>
<span data-ttu-id="e1bb0-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bb0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1bb0-121">-WhatIf</span></span>
<span data-ttu-id="e1bb0-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1bb0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bb0-124">CommonParameters</span></span>
<span data-ttu-id="e1bb0-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bb0-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bb0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bb0-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1bb0-127">INPUTS</span></span>

### <span data-ttu-id="e1bb0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e1bb0-128">System.String</span></span>

## <span data-ttu-id="e1bb0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1bb0-129">OUTPUTS</span></span>

### <span data-ttu-id="e1bb0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e1bb0-130">System.Void</span></span>

## <span data-ttu-id="e1bb0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1bb0-131">NOTES</span></span>

## <span data-ttu-id="e1bb0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1bb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1bb0-133">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="e1bb0-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


