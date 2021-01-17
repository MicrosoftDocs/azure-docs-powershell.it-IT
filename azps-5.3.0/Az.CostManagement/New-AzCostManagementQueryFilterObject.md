---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487779"
---
# <span data-ttu-id="a75e6-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="a75e6-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="a75e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a75e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a75e6-103">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a75e6-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="a75e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a75e6-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="a75e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a75e6-105">DESCRIPTION</span></span>
<span data-ttu-id="a75e6-106">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a75e6-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="a75e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a75e6-107">EXAMPLES</span></span>

### <span data-ttu-id="a75e6-108">Esempio 1: creare un oggetto Filter di query per l'esportazione di gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="a75e6-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="a75e6-109">Questo comando crea un oggetto Filter di query per l'esportazione di gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="a75e6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a75e6-110">PARAMETERS</span></span>

### <span data-ttu-id="a75e6-111">-E</span><span class="sxs-lookup"><span data-stu-id="a75e6-111">-And</span></span>
<span data-ttu-id="a75e6-112">Espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-112">The logical "AND" expression.</span></span>
<span data-ttu-id="a75e6-113">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-113">Must have at least 2 items.</span></span>
<span data-ttu-id="a75e6-114">Per costruire, vedere la sezione Note per le proprietà e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a75e6-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75e6-115">-Dimensioni</span><span class="sxs-lookup"><span data-stu-id="a75e6-115">-Dimensions</span></span>
<span data-ttu-id="a75e6-116">Ha un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a75e6-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="a75e6-117">Per costruire, vedere la sezione Note per le proprietà delle dimensioni e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a75e6-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75e6-118">-Not</span><span class="sxs-lookup"><span data-stu-id="a75e6-118">-Not</span></span>
<span data-ttu-id="a75e6-119">Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="a75e6-120">Per costruire, vedere la sezione Note per le proprietà NOT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a75e6-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75e6-121">-Oppure</span><span class="sxs-lookup"><span data-stu-id="a75e6-121">-Or</span></span>
<span data-ttu-id="a75e6-122">Espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-122">The logical "OR" expression.</span></span>
<span data-ttu-id="a75e6-123">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-123">Must have at least 2 items.</span></span>
<span data-ttu-id="a75e6-124">Per creare una tabella hash, vedere la sezione Note o proprietà.</span><span class="sxs-lookup"><span data-stu-id="a75e6-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75e6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a75e6-125">-Tag</span></span>
<span data-ttu-id="a75e6-126">Ha un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="a75e6-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="a75e6-127">Per costruire, vedere la sezione Note per le proprietà dei TAG e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a75e6-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75e6-128">CommonParameters</span></span>
<span data-ttu-id="a75e6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75e6-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a75e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75e6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a75e6-131">INPUTS</span></span>

## <span data-ttu-id="a75e6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a75e6-132">OUTPUTS</span></span>

### <span data-ttu-id="a75e6-133">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a75e6-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="a75e6-134">Note</span><span class="sxs-lookup"><span data-stu-id="a75e6-134">NOTES</span></span>

<span data-ttu-id="a75e6-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a75e6-135">ALIASES</span></span>

<span data-ttu-id="a75e6-136">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a75e6-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a75e6-137">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a75e6-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a75e6-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a75e6-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a75e6-139">E <IQueryFilter [] >: l'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="a75e6-140">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-141">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a75e6-142">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-143">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a75e6-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a75e6-144">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a75e6-145">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="a75e6-146">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a75e6-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a75e6-147">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a75e6-148">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a75e6-149">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-150">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a75e6-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a75e6-151">DIMENSIONI <IQueryComparisonExpression> : contiene un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a75e6-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="a75e6-152">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="a75e6-153">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="a75e6-154">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a75e6-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="a75e6-155">NOT <IQueryFilter> : l'espressione "not" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a75e6-156">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a75e6-157">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-158">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a75e6-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a75e6-159">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a75e6-160">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="a75e6-161">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a75e6-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a75e6-162">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a75e6-163">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a75e6-164">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-165">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a75e6-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a75e6-166">O <IQueryFilter [] >: l'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="a75e6-167">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-168">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a75e6-169">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-170">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a75e6-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a75e6-171">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a75e6-172">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="a75e6-173">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a75e6-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a75e6-174">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a75e6-175">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="a75e6-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a75e6-176">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a75e6-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a75e6-177">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a75e6-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a75e6-178">TAG <IQueryComparisonExpression> : contiene un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="a75e6-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="a75e6-179">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="a75e6-180">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="a75e6-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="a75e6-181">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a75e6-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="a75e6-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a75e6-182">RELATED LINKS</span></span>

