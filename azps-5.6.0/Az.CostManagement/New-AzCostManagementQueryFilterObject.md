---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010653"
---
# <span data-ttu-id="a58dc-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="a58dc-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="a58dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a58dc-103">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a58dc-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="a58dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a58dc-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="a58dc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a58dc-105">DESCRIPTION</span></span>
<span data-ttu-id="a58dc-106">Creare un oggetto in memoria per QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a58dc-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="a58dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a58dc-107">EXAMPLES</span></span>

### <span data-ttu-id="a58dc-108">Esempio 1: Creare un oggetto filtro della query per l'esportazione della gestione dei costi</span><span class="sxs-lookup"><span data-stu-id="a58dc-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="a58dc-109">Questo comando crea un oggetto filtro della query per l'esportazione della gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="a58dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a58dc-110">PARAMETERS</span></span>

### <span data-ttu-id="a58dc-111">-And</span><span class="sxs-lookup"><span data-stu-id="a58dc-111">-And</span></span>
<span data-ttu-id="a58dc-112">Espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="a58dc-112">The logical "AND" expression.</span></span>
<span data-ttu-id="a58dc-113">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-113">Must have at least 2 items.</span></span>
<span data-ttu-id="a58dc-114">Per creare, vedere la sezione NOTE relativa alle proprietà AND e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a58dc-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="a58dc-115">-Dimensions</span><span class="sxs-lookup"><span data-stu-id="a58dc-115">-Dimensions</span></span>
<span data-ttu-id="a58dc-116">Ha un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a58dc-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="a58dc-117">Per creare, vedere la sezione NOTE relativa alle proprietà DIMENSIONS e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a58dc-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="a58dc-118">-Not</span><span class="sxs-lookup"><span data-stu-id="a58dc-118">-Not</span></span>
<span data-ttu-id="a58dc-119">Espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="a58dc-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="a58dc-120">Per creare, vedere la sezione NOTE per le proprietà NOT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a58dc-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a58dc-121">-Oppure</span><span class="sxs-lookup"><span data-stu-id="a58dc-121">-Or</span></span>
<span data-ttu-id="a58dc-122">Espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="a58dc-122">The logical "OR" expression.</span></span>
<span data-ttu-id="a58dc-123">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-123">Must have at least 2 items.</span></span>
<span data-ttu-id="a58dc-124">Per creare, vedere la sezione NOTE relativa alle proprietà OR e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a58dc-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="a58dc-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a58dc-125">-Tag</span></span>
<span data-ttu-id="a58dc-126">Ha un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="a58dc-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="a58dc-127">Per creare, vedere la sezione NOTE relativa alle proprietà TAG e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a58dc-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="a58dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58dc-128">CommonParameters</span></span>
<span data-ttu-id="a58dc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58dc-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a58dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58dc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a58dc-131">INPUTS</span></span>

## <span data-ttu-id="a58dc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a58dc-132">OUTPUTS</span></span>

### <span data-ttu-id="a58dc-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="a58dc-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="a58dc-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="a58dc-134">NOTES</span></span>

<span data-ttu-id="a58dc-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a58dc-135">ALIASES</span></span>

<span data-ttu-id="a58dc-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a58dc-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a58dc-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a58dc-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a58dc-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a58dc-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a58dc-139">AND <IQueryFilter[]>: espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="a58dc-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="a58dc-140">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-141">`[And <IQueryFilter[]>]`: Espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="a58dc-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a58dc-142">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-143">`[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a58dc-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a58dc-144">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="a58dc-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a58dc-145">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a58dc-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a58dc-146">`[Not <IQueryFilter>]`: Espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="a58dc-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a58dc-147">`[Or <IQueryFilter[]>]`: Espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="a58dc-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a58dc-148">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-149">`[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a58dc-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a58dc-150">DIMENSIONS: <IQueryComparisonExpression> ha un'espressione di confronto per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a58dc-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="a58dc-151">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="a58dc-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="a58dc-152">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a58dc-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="a58dc-153">NOT: <IQueryFilter> espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="a58dc-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a58dc-154">`[And <IQueryFilter[]>]`: Espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="a58dc-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a58dc-155">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-156">`[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a58dc-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a58dc-157">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="a58dc-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a58dc-158">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a58dc-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a58dc-159">`[Not <IQueryFilter>]`: Espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="a58dc-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a58dc-160">`[Or <IQueryFilter[]>]`: Espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="a58dc-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a58dc-161">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-162">`[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a58dc-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a58dc-163">OR <IQueryFilter[]>: espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="a58dc-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="a58dc-164">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-165">`[And <IQueryFilter[]>]`: Espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="a58dc-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="a58dc-166">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-167">`[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="a58dc-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="a58dc-168">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="a58dc-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="a58dc-169">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a58dc-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="a58dc-170">`[Not <IQueryFilter>]`: Espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="a58dc-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="a58dc-171">`[Or <IQueryFilter[]>]`: Espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="a58dc-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="a58dc-172">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="a58dc-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="a58dc-173">`[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="a58dc-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="a58dc-174">TAG: <IQueryComparisonExpression> include un'espressione di confronto per un tag.</span><span class="sxs-lookup"><span data-stu-id="a58dc-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="a58dc-175">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="a58dc-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="a58dc-176">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="a58dc-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="a58dc-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a58dc-177">RELATED LINKS</span></span>

