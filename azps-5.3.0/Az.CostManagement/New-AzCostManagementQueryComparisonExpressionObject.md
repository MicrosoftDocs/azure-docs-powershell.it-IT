---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477316"
---
# <span data-ttu-id="646cc-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="646cc-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="646cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="646cc-102">SYNOPSIS</span></span>
<span data-ttu-id="646cc-103">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="646cc-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="646cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="646cc-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="646cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="646cc-105">DESCRIPTION</span></span>
<span data-ttu-id="646cc-106">Creare un oggetto in memoria per QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="646cc-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="646cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="646cc-107">EXAMPLES</span></span>

### <span data-ttu-id="646cc-108">Esempio 1: creare un oggetto di espressione di confronto di query per l'esportazione di gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="646cc-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="646cc-109">Questo comando crea un oggetto espressione di confronto di query per l'esportazione di gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="646cc-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="646cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="646cc-110">PARAMETERS</span></span>

### <span data-ttu-id="646cc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="646cc-111">-Name</span></span>
<span data-ttu-id="646cc-112">Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="646cc-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="646cc-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="646cc-113">-Operator</span></span>
<span data-ttu-id="646cc-114">Operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="646cc-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="646cc-115">-Valore</span><span class="sxs-lookup"><span data-stu-id="646cc-115">-Value</span></span>
<span data-ttu-id="646cc-116">Matrice di valori da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="646cc-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="646cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646cc-117">CommonParameters</span></span>
<span data-ttu-id="646cc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646cc-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="646cc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646cc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="646cc-120">INPUTS</span></span>

## <span data-ttu-id="646cc-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="646cc-121">OUTPUTS</span></span>

### <span data-ttu-id="646cc-122">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="646cc-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="646cc-123">Note</span><span class="sxs-lookup"><span data-stu-id="646cc-123">NOTES</span></span>

<span data-ttu-id="646cc-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="646cc-124">ALIASES</span></span>

## <span data-ttu-id="646cc-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="646cc-125">RELATED LINKS</span></span>

