---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998170"
---
# <span data-ttu-id="12314-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="12314-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="12314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12314-102">SYNOPSIS</span></span>
<span data-ttu-id="12314-103">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="12314-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="12314-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12314-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="12314-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12314-105">DESCRIPTION</span></span>
<span data-ttu-id="12314-106">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="12314-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="12314-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12314-107">EXAMPLES</span></span>

### <span data-ttu-id="12314-108">Esempio 1: Creare un oggetto espressione di confronto di una query per l'esportazione di gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="12314-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="12314-109">Questo comando crea un oggetto espressione di confronto della query per l'esportazione della gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="12314-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="12314-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12314-110">PARAMETERS</span></span>

### <span data-ttu-id="12314-111">-Name</span><span class="sxs-lookup"><span data-stu-id="12314-111">-Name</span></span>
<span data-ttu-id="12314-112">Nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="12314-112">The name of the column to use in comparison.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12314-113">-Operatore</span><span class="sxs-lookup"><span data-stu-id="12314-113">-Operator</span></span>
<span data-ttu-id="12314-114">Operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="12314-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12314-115">-Value</span><span class="sxs-lookup"><span data-stu-id="12314-115">-Value</span></span>
<span data-ttu-id="12314-116">Matrice di valori da utilizzare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="12314-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12314-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12314-117">CommonParameters</span></span>
<span data-ttu-id="12314-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12314-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12314-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12314-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12314-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="12314-120">INPUTS</span></span>

## <span data-ttu-id="12314-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12314-121">OUTPUTS</span></span>

### <span data-ttu-id="12314-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="12314-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="12314-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="12314-123">NOTES</span></span>

<span data-ttu-id="12314-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="12314-124">ALIASES</span></span>

## <span data-ttu-id="12314-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12314-125">RELATED LINKS</span></span>

