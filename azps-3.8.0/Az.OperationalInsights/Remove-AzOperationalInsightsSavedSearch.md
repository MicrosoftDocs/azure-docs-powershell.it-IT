---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 931c85b649393d33f03e778d0e34cf6644e4c2d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030751"
---
# <span data-ttu-id="61c77-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="61c77-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="61c77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61c77-102">SYNOPSIS</span></span>
<span data-ttu-id="61c77-103">Rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61c77-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="61c77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61c77-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61c77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61c77-105">DESCRIPTION</span></span>
<span data-ttu-id="61c77-106">Il cmdlet **Remove-AzOperationalInsightsSavedSearch** rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61c77-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="61c77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61c77-107">EXAMPLES</span></span>

### <span data-ttu-id="61c77-108">Esempio 1: rimuovere una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="61c77-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="61c77-109">Questo comando rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61c77-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="61c77-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61c77-110">PARAMETERS</span></span>

### <span data-ttu-id="61c77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c77-111">-DefaultProfile</span></span>
<span data-ttu-id="61c77-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61c77-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61c77-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c77-113">-ResourceGroupName</span></span>
<span data-ttu-id="61c77-114">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61c77-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="61c77-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="61c77-115">-SavedSearchId</span></span>
<span data-ttu-id="61c77-116">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="61c77-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="61c77-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61c77-117">-WorkspaceName</span></span>
<span data-ttu-id="61c77-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61c77-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="61c77-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61c77-119">-Confirm</span></span>
<span data-ttu-id="61c77-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61c77-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c77-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c77-121">-WhatIf</span></span>
<span data-ttu-id="61c77-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61c77-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c77-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61c77-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c77-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c77-124">CommonParameters</span></span>
<span data-ttu-id="61c77-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c77-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c77-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c77-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c77-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61c77-127">INPUTS</span></span>

### <span data-ttu-id="61c77-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61c77-128">System.String</span></span>

## <span data-ttu-id="61c77-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61c77-129">OUTPUTS</span></span>

### <span data-ttu-id="61c77-130">System. void</span><span class="sxs-lookup"><span data-stu-id="61c77-130">System.Void</span></span>

## <span data-ttu-id="61c77-131">Note</span><span class="sxs-lookup"><span data-stu-id="61c77-131">NOTES</span></span>

## <span data-ttu-id="61c77-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61c77-132">RELATED LINKS</span></span>

[<span data-ttu-id="61c77-133">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="61c77-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


