---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336616"
---
# <span data-ttu-id="4e8eb-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="4e8eb-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="4e8eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8eb-103">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="4e8eb-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="4e8eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="4e8eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e8eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8eb-106">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="4e8eb-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="4e8eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-107">EXAMPLES</span></span>

### <span data-ttu-id="4e8eb-108">Esempio 1: creare un oggetto Filter di query per l'esportazione di gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="4e8eb-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="4e8eb-109">Questo comando crea un oggetto Filter di query per l'esportazione di gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="4e8eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-110">PARAMETERS</span></span>

### <span data-ttu-id="4e8eb-111">-E</span><span class="sxs-lookup"><span data-stu-id="4e8eb-111">-And</span></span>
<span data-ttu-id="4e8eb-112">Espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-112">The logical "AND" expression.</span></span>
<span data-ttu-id="4e8eb-113">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-113">Must have at least 2 items.</span></span>
<span data-ttu-id="4e8eb-114">Per costruire, vedere la sezione Note per le proprietà e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8eb-115">-Dimensioni</span><span class="sxs-lookup"><span data-stu-id="4e8eb-115">-Dimensions</span></span>
<span data-ttu-id="4e8eb-116">Ha un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="4e8eb-117">Per costruire, vedere la sezione Note per le proprietà delle dimensioni e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8eb-118">-Not</span><span class="sxs-lookup"><span data-stu-id="4e8eb-118">-Not</span></span>
<span data-ttu-id="4e8eb-119">Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="4e8eb-120">Per costruire, vedere la sezione Note per le proprietà NOT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8eb-121">-Oppure</span><span class="sxs-lookup"><span data-stu-id="4e8eb-121">-Or</span></span>
<span data-ttu-id="4e8eb-122">Espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-122">The logical "OR" expression.</span></span>
<span data-ttu-id="4e8eb-123">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-123">Must have at least 2 items.</span></span>
<span data-ttu-id="4e8eb-124">Per creare una tabella hash, vedere la sezione Note o proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8eb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e8eb-125">-Tag</span></span>
<span data-ttu-id="4e8eb-126">Ha un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="4e8eb-127">Per costruire, vedere la sezione Note per le proprietà dei TAG e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8eb-128">CommonParameters</span></span>
<span data-ttu-id="4e8eb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8eb-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e8eb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8eb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-131">INPUTS</span></span>

## <span data-ttu-id="4e8eb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e8eb-132">OUTPUTS</span></span>

### <span data-ttu-id="4e8eb-133">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. QueryFilter</span><span class="sxs-lookup"><span data-stu-id="4e8eb-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="4e8eb-134">Note</span><span class="sxs-lookup"><span data-stu-id="4e8eb-134">NOTES</span></span>

<span data-ttu-id="4e8eb-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4e8eb-135">ALIASES</span></span>

<span data-ttu-id="4e8eb-136">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e8eb-137">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e8eb-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e8eb-139">E <IQueryFilter [] >: l'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="4e8eb-140">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-141">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4e8eb-142">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-143">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="4e8eb-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4e8eb-144">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4e8eb-145">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="4e8eb-146">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="4e8eb-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4e8eb-147">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4e8eb-148">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4e8eb-149">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-150">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="4e8eb-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4e8eb-151">DIMENSIONI <IQueryComparisonExpression> : contiene un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="4e8eb-152">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="4e8eb-153">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="4e8eb-154">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="4e8eb-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="4e8eb-155">NOT <IQueryFilter> : l'espressione "not" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4e8eb-156">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4e8eb-157">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-158">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="4e8eb-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4e8eb-159">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4e8eb-160">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="4e8eb-161">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="4e8eb-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4e8eb-162">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4e8eb-163">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4e8eb-164">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-165">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="4e8eb-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4e8eb-166">O <IQueryFilter [] >: l'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="4e8eb-167">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-168">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4e8eb-169">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-170">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="4e8eb-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4e8eb-171">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4e8eb-172">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="4e8eb-173">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="4e8eb-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4e8eb-174">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4e8eb-175">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4e8eb-176">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4e8eb-177">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="4e8eb-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4e8eb-178">TAG <IQueryComparisonExpression> : contiene un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="4e8eb-179">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="4e8eb-180">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="4e8eb-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="4e8eb-181">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="4e8eb-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="4e8eb-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e8eb-182">RELATED LINKS</span></span>

