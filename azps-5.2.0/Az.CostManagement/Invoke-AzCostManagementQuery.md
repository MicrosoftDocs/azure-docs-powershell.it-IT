---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334651"
---
# <span data-ttu-id="c2f66-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="c2f66-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="c2f66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2f66-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f66-103">Eseguire una query sui dati di utilizzo per l'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="c2f66-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="c2f66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2f66-104">SYNTAX</span></span>

### <span data-ttu-id="c2f66-105">UsageExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2f66-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2f66-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="c2f66-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2f66-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2f66-107">DESCRIPTION</span></span>
<span data-ttu-id="c2f66-108">Eseguire una query sui dati di utilizzo per l'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="c2f66-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="c2f66-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2f66-109">EXAMPLES</span></span>

### <span data-ttu-id="c2f66-110">Esempio 1: richiamare AzCostManagementQuery per ambito</span><span class="sxs-lookup"><span data-stu-id="c2f66-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="c2f66-111">Richiamare AzCostManagementQuery per ambito</span><span class="sxs-lookup"><span data-stu-id="c2f66-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="c2f66-112">Esempio 2: richiamare AzCostManagementQuery per ambito con le dimensioni</span><span class="sxs-lookup"><span data-stu-id="c2f66-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="c2f66-113">Richiamare AzCostManagementQuery per ambito con le dimensioni</span><span class="sxs-lookup"><span data-stu-id="c2f66-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="c2f66-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2f66-114">PARAMETERS</span></span>

### <span data-ttu-id="c2f66-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="c2f66-115">-ConfigurationColumn</span></span>
<span data-ttu-id="c2f66-116">Matrice di nomi di colonna da includere nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="c2f66-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="c2f66-117">-DatasetAggregation</span></span>
<span data-ttu-id="c2f66-118">Dizionario di espressione di aggregazione da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="c2f66-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="c2f66-119">-DatasetFilter</span></span>
<span data-ttu-id="c2f66-120">Ha un'espressione di filtro da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="c2f66-121">Per costruire, vedere la sezione Note per le proprietà di DATASETFILTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c2f66-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2f66-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="c2f66-122">-DatasetGranularity</span></span>
<span data-ttu-id="c2f66-123">Granularità delle righe nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="c2f66-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="c2f66-124">-DatasetGrouping</span></span>
<span data-ttu-id="c2f66-125">Matrice di espressione Group by da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="c2f66-126">Per costruire, vedere la sezione Note per le proprietà di DATASETGROUPING e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c2f66-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2f66-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f66-127">-DefaultProfile</span></span>
<span data-ttu-id="c2f66-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f66-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f66-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="c2f66-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="c2f66-130">Può essere "{externalSubscriptionId}" per l'account collegato o "{externalBillingAccountId}" per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

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

### <span data-ttu-id="c2f66-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="c2f66-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="c2f66-132">Il tipo di provider cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-132">The external cloud provider type associated with dimension/query operations.</span></span>

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

### <span data-ttu-id="c2f66-133">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c2f66-133">-Scope</span></span>
<span data-ttu-id="c2f66-134">Questo include "abbonamenti/{subscriptionId}/" per l'ambito dell'abbonamento, "abbonamenti/{subscriptionId}/resourceGroups/{resourceGroupName}" per resourceGroup ambito, "providers/Microsoft. Billing/billingAccounts/{billingAccountId}' per l'ambito dell'account di fatturazione è Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/repartis/{IDReparto}' per l'ambito Department,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope,' Providers/Microsoft. Management/managementGroups/{managementGroupId} per l'ambito del gruppo di gestione" provider/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "per billingProfile ambito," providers/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' per invoiceSection ambito è Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/Customers/{customerId}' specifico per i partner.</span><span class="sxs-lookup"><span data-stu-id="c2f66-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

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

### <span data-ttu-id="c2f66-135">-Intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="c2f66-135">-Timeframe</span></span>
<span data-ttu-id="c2f66-136">Intervallo di tempo per l'estrazione dei dati per la query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-136">The time frame for pulling data for the query.</span></span>

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

### <span data-ttu-id="c2f66-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="c2f66-137">-TimePeriodFrom</span></span>
<span data-ttu-id="c2f66-138">Data di inizio in cui estrarre i dati.</span><span class="sxs-lookup"><span data-stu-id="c2f66-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="c2f66-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="c2f66-139">-TimePeriodTo</span></span>
<span data-ttu-id="c2f66-140">Data di fine in cui estrarre i dati.</span><span class="sxs-lookup"><span data-stu-id="c2f66-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="c2f66-141">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c2f66-141">-Type</span></span>
<span data-ttu-id="c2f66-142">Tipo della query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-142">The type of the query.</span></span>

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

### <span data-ttu-id="c2f66-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2f66-143">-Confirm</span></span>
<span data-ttu-id="c2f66-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f66-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f66-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f66-145">-WhatIf</span></span>
<span data-ttu-id="c2f66-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2f66-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f66-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2f66-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f66-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f66-148">CommonParameters</span></span>
<span data-ttu-id="c2f66-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f66-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f66-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2f66-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f66-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2f66-151">INPUTS</span></span>

## <span data-ttu-id="c2f66-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2f66-152">OUTPUTS</span></span>

### <span data-ttu-id="c2f66-153">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. IQueryResult</span><span class="sxs-lookup"><span data-stu-id="c2f66-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="c2f66-154">Note</span><span class="sxs-lookup"><span data-stu-id="c2f66-154">NOTES</span></span>

<span data-ttu-id="c2f66-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c2f66-155">ALIASES</span></span>

<span data-ttu-id="c2f66-156">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2f66-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2f66-157">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c2f66-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2f66-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2f66-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2f66-159">DATASETFILTER <IQueryFilter> : contiene l'espressione di filtro da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="c2f66-160">`[And <IQueryFilter[]>]`: L'espressione "e" logica.</span><span class="sxs-lookup"><span data-stu-id="c2f66-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="c2f66-161">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="c2f66-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="c2f66-162">`[Dimensions <IQueryComparisonExpression>]`: Contiene un'espressione di confronto per una dimensione</span><span class="sxs-lookup"><span data-stu-id="c2f66-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="c2f66-163">`Name <String>`: Nome della colonna da usare in confronto.</span><span class="sxs-lookup"><span data-stu-id="c2f66-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="c2f66-164">`Operator <OperatorType>`: L'operatore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="c2f66-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="c2f66-165">`Value <String[]>`: Matrice di valori da usare per il confronto</span><span class="sxs-lookup"><span data-stu-id="c2f66-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="c2f66-166">`[Not <IQueryFilter>]`: Espressione "NOT" logica.</span><span class="sxs-lookup"><span data-stu-id="c2f66-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="c2f66-167">`[Or <IQueryFilter[]>]`: L'espressione "OR" logica.</span><span class="sxs-lookup"><span data-stu-id="c2f66-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="c2f66-168">Devono avere almeno 2 elementi.</span><span class="sxs-lookup"><span data-stu-id="c2f66-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="c2f66-169">`[Tag <IQueryComparisonExpression>]`: Ha un'espressione di confronto per un tag</span><span class="sxs-lookup"><span data-stu-id="c2f66-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="c2f66-170">DATASETGROUPING <IQueryGrouping [] >: matrice di espressione Group by da usare nella query.</span><span class="sxs-lookup"><span data-stu-id="c2f66-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="c2f66-171">`Name <String>`: Nome della colonna da raggruppare.</span><span class="sxs-lookup"><span data-stu-id="c2f66-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="c2f66-172">`Type <QueryColumnType>`: Ha tipo della colonna da raggruppare.</span><span class="sxs-lookup"><span data-stu-id="c2f66-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="c2f66-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2f66-173">RELATED LINKS</span></span>

