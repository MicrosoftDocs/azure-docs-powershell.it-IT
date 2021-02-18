---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181174"
---
# <span data-ttu-id="ae63e-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="ae63e-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="ae63e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae63e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae63e-103">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="ae63e-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="ae63e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae63e-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="ae63e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae63e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae63e-106">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="ae63e-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="ae63e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae63e-107">EXAMPLES</span></span>

### <span data-ttu-id="ae63e-108">Esempio 1: Creare un oggetto espressione di confronto di una query per l'esportazione della gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="ae63e-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="ae63e-109">Questo comando crea un oggetto espressione di confronto della query per l'esportazione della gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="ae63e-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="ae63e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae63e-110">PARAMETERS</span></span>

### <span data-ttu-id="ae63e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="ae63e-111">-Name</span></span>
<span data-ttu-id="ae63e-112">Nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="ae63e-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="ae63e-113">-Operatore</span><span class="sxs-lookup"><span data-stu-id="ae63e-113">-Operator</span></span>
<span data-ttu-id="ae63e-114">Operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="ae63e-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="ae63e-115">-Value</span><span class="sxs-lookup"><span data-stu-id="ae63e-115">-Value</span></span>
<span data-ttu-id="ae63e-116">Matrice di valori da utilizzare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="ae63e-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="ae63e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae63e-117">CommonParameters</span></span>
<span data-ttu-id="ae63e-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae63e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae63e-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae63e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae63e-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae63e-120">INPUTS</span></span>

## <span data-ttu-id="ae63e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae63e-121">OUTPUTS</span></span>

### <span data-ttu-id="ae63e-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="ae63e-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="ae63e-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae63e-123">NOTES</span></span>

<span data-ttu-id="ae63e-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ae63e-124">ALIASES</span></span>

## <span data-ttu-id="ae63e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae63e-125">RELATED LINKS</span></span>

