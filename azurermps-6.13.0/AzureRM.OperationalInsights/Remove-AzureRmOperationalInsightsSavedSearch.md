---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517364"
---
# <span data-ttu-id="790a1-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="790a1-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="790a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="790a1-102">SYNOPSIS</span></span>
<span data-ttu-id="790a1-103">Rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="790a1-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="790a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="790a1-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="790a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="790a1-105">DESCRIPTION</span></span>
<span data-ttu-id="790a1-106">Il cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="790a1-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="790a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="790a1-107">EXAMPLES</span></span>

### <span data-ttu-id="790a1-108">Esempio 1: rimuovere una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="790a1-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="790a1-109">Questo comando rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="790a1-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="790a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="790a1-110">PARAMETERS</span></span>

### <span data-ttu-id="790a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790a1-111">-DefaultProfile</span></span>
<span data-ttu-id="790a1-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="790a1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="790a1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790a1-113">-ResourceGroupName</span></span>
<span data-ttu-id="790a1-114">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="790a1-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="790a1-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="790a1-115">-SavedSearchId</span></span>
<span data-ttu-id="790a1-116">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="790a1-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="790a1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="790a1-117">-WorkspaceName</span></span>
<span data-ttu-id="790a1-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="790a1-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="790a1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="790a1-119">-Confirm</span></span>
<span data-ttu-id="790a1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="790a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="790a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="790a1-121">-WhatIf</span></span>
<span data-ttu-id="790a1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="790a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="790a1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="790a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="790a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790a1-124">CommonParameters</span></span>
<span data-ttu-id="790a1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790a1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790a1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790a1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="790a1-127">INPUTS</span></span>

### <span data-ttu-id="790a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="790a1-128">System.String</span></span>

## <span data-ttu-id="790a1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="790a1-129">OUTPUTS</span></span>

### <span data-ttu-id="790a1-130">System. void</span><span class="sxs-lookup"><span data-stu-id="790a1-130">System.Void</span></span>

## <span data-ttu-id="790a1-131">Note</span><span class="sxs-lookup"><span data-stu-id="790a1-131">NOTES</span></span>

## <span data-ttu-id="790a1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="790a1-132">RELATED LINKS</span></span>

[<span data-ttu-id="790a1-133">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="790a1-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


