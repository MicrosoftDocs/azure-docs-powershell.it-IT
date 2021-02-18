---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 37f4d4b5650060b490e8c6bb691d938b78fa1166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181190"
---
# <span data-ttu-id="467da-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="467da-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="467da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="467da-102">SYNOPSIS</span></span>
<span data-ttu-id="467da-103">Eseguire una query sui dati di utilizzo per l'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="467da-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="467da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="467da-104">SYNTAX</span></span>

### <span data-ttu-id="467da-105">UsageExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="467da-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="467da-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="467da-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="467da-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="467da-107">DESCRIPTION</span></span>
<span data-ttu-id="467da-108">Eseguire una query sui dati di utilizzo per l'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="467da-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="467da-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="467da-109">EXAMPLES</span></span>

### <span data-ttu-id="467da-110">Esempio 1: Richiamare AzCostManagementQuery per ambito</span><span class="sxs-lookup"><span data-stu-id="467da-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="467da-111">Richiamare AzCostManagementQuery per ambito</span><span class="sxs-lookup"><span data-stu-id="467da-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="467da-112">Esempio 2: Richiamare AzCostManagementQuery per ambito con dimensioni</span><span class="sxs-lookup"><span data-stu-id="467da-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="467da-113">Richiamare AzCostManagementQuery per ambito con dimensioni</span><span class="sxs-lookup"><span data-stu-id="467da-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="467da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="467da-114">PARAMETERS</span></span>

### <span data-ttu-id="467da-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="467da-115">-ConfigurationColumn</span></span>
<span data-ttu-id="467da-116">Matrice di nomi di colonna da includere nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-116">Array of column names to be included in the query.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="467da-117">-DatasetAggregation</span></span>
<span data-ttu-id="467da-118">Dizionario dell'espressione di aggregazione da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="467da-119">-DatasetFilter</span></span>
<span data-ttu-id="467da-120">Include un'espressione di filtro da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="467da-121">Per creare, vedere la sezione NOTE per le proprietà DI DATASETFILTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="467da-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="467da-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="467da-122">-DatasetGranularity</span></span>
<span data-ttu-id="467da-123">Granularità delle righe nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-123">The granularity of rows in the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="467da-124">-DatasetGrouping</span></span>
<span data-ttu-id="467da-125">Matrice dell'espressione di raggruppamento da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="467da-126">Per creare, vedere la sezione NOTE per le proprietà DATASETGROUPING e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="467da-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467da-127">-DefaultProfile</span></span>
<span data-ttu-id="467da-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="467da-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="467da-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="467da-130">Può essere '{externalSubscriptionId}' per l'account collegato o '{externalBillingAccountId}' per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="467da-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="467da-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="467da-132">Tipo di provider di cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="467da-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="467da-133">-Scope</span></span>
<span data-ttu-id="467da-134">Ciò include 'subscriptions/{subscriptionId}/' per l'ambito della sottoscrizione, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' per l'ambito resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' per l'ambito Account di fatturazione e 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' per l'ambito del reparto, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' per l'ambito EnrollmentAccount, 'providers/Microsoft.Management/managementGroups/{managementGroupId} per l'ambito del gruppo di gestione, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' per l'ambito billingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' per l'ambito invoiceSection e 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific per i partner.</span><span class="sxs-lookup"><span data-stu-id="467da-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="467da-135">-Timeframe</span></span>
<span data-ttu-id="467da-136">Intervallo di tempo per il pull dei dati per la query.</span><span class="sxs-lookup"><span data-stu-id="467da-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="467da-137">-TimePeriodFrom</span></span>
<span data-ttu-id="467da-138">Data di inizio da cui estrarre i dati.</span><span class="sxs-lookup"><span data-stu-id="467da-138">The start date to pull data from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="467da-139">-TimePeriodTo</span></span>
<span data-ttu-id="467da-140">Data di fine in cui estrarre i dati.</span><span class="sxs-lookup"><span data-stu-id="467da-140">The end date to pull data to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-141">-Type</span><span class="sxs-lookup"><span data-stu-id="467da-141">-Type</span></span>
<span data-ttu-id="467da-142">Tipo di query.</span><span class="sxs-lookup"><span data-stu-id="467da-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="467da-143">-Confirm</span></span>
<span data-ttu-id="467da-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="467da-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467da-145">-WhatIf</span></span>
<span data-ttu-id="467da-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="467da-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="467da-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="467da-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467da-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467da-148">CommonParameters</span></span>
<span data-ttu-id="467da-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467da-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467da-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="467da-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467da-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="467da-151">INPUTS</span></span>

## <span data-ttu-id="467da-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="467da-152">OUTPUTS</span></span>

### <span data-ttu-id="467da-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="467da-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="467da-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="467da-154">NOTES</span></span>

<span data-ttu-id="467da-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="467da-155">ALIASES</span></span>

<span data-ttu-id="467da-156">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="467da-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="467da-157">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="467da-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="467da-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="467da-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="467da-159"><IQueryFilter>DATASETFILTER: include un'espressione di filtro da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="467da-160">`[And <IQueryFilter[]>]`: l'espressione logica "AND".</span><span class="sxs-lookup"><span data-stu-id="467da-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="467da-161">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="467da-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="467da-162">`[Dimensions <IQueryComparisonExpression>]`: include un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="467da-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="467da-163">`Name <String>`: nome della colonna da usare nel confronto.</span><span class="sxs-lookup"><span data-stu-id="467da-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="467da-164">`Value <String[]>`: matrice di valori da utilizzare per il confronto</span><span class="sxs-lookup"><span data-stu-id="467da-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="467da-165">`[Not <IQueryFilter>]`: Espressione logica "NON".</span><span class="sxs-lookup"><span data-stu-id="467da-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="467da-166">`[Or <IQueryFilter[]>]`: Espressione logica "OR".</span><span class="sxs-lookup"><span data-stu-id="467da-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="467da-167">Devono contenere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="467da-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="467da-168">`[Tag <IQueryComparisonExpression>]`: include un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="467da-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="467da-169">DATASETGROUPING <IQueryGrouping[]>: matrice di espressioni group by da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="467da-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="467da-170">`Name <String>`: nome della colonna da raggruppare.</span><span class="sxs-lookup"><span data-stu-id="467da-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="467da-171">`Type <QueryColumnType>`: include il tipo della colonna da raggruppare.</span><span class="sxs-lookup"><span data-stu-id="467da-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="467da-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="467da-172">RELATED LINKS</span></span>

