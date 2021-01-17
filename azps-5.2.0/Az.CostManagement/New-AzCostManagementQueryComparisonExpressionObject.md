---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336640"
---
# <span data-ttu-id="26fa9-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="26fa9-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="26fa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="26fa9-103">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="26fa9-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="26fa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26fa9-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="26fa9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="26fa9-106">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="26fa9-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="26fa9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="26fa9-108">Esempio 1: creare un oggetto di espressione di confronto di query per l'esportazione di gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="26fa9-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="26fa9-109">Questo comando crea un oggetto espressione di confronto di query per l'esportazione di gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="26fa9-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="26fa9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="26fa9-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="26fa9-111">-Name</span></span>
<span data-ttu-id="26fa9-112">Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="26fa9-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="26fa9-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="26fa9-113">-Operator</span></span>
<span data-ttu-id="26fa9-114">Operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="26fa9-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="26fa9-115">-Valore</span><span class="sxs-lookup"><span data-stu-id="26fa9-115">-Value</span></span>
<span data-ttu-id="26fa9-116">Matrice di valori da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="26fa9-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="26fa9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fa9-117">CommonParameters</span></span>
<span data-ttu-id="26fa9-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fa9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fa9-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26fa9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fa9-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26fa9-120">INPUTS</span></span>

## <span data-ttu-id="26fa9-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26fa9-121">OUTPUTS</span></span>

### <span data-ttu-id="26fa9-122">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="26fa9-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="26fa9-123">Note</span><span class="sxs-lookup"><span data-stu-id="26fa9-123">NOTES</span></span>

<span data-ttu-id="26fa9-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="26fa9-124">ALIASES</span></span>

## <span data-ttu-id="26fa9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26fa9-125">RELATED LINKS</span></span>

