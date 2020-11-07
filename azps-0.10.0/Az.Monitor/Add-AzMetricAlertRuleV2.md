---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 3c0178ebae2237730d7f0d11eb832a30988ffdb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862962"
---
# <span data-ttu-id="c2541-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c2541-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="c2541-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2541-102">SYNOPSIS</span></span>
<span data-ttu-id="c2541-103">Aggiunge o aggiorna una regola di avviso basata su metriche V2 (non classica).</span><span class="sxs-lookup"><span data-stu-id="c2541-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="c2541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2541-104">SYNTAX</span></span>

### <span data-ttu-id="c2541-105">CreateAlertByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2541-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2541-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="c2541-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2541-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c2541-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2541-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="c2541-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2541-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="c2541-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2541-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c2541-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2541-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2541-111">DESCRIPTION</span></span>
<span data-ttu-id="c2541-112">Aggiunge o aggiorna una **regola di avviso basata su metriche V2 (non classica)**.</span><span class="sxs-lookup"><span data-stu-id="c2541-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="c2541-113">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="c2541-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="c2541-114">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2541-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c2541-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2541-115">EXAMPLES</span></span>

### <span data-ttu-id="c2541-116">Esempio 1: aggiungere una regola di avviso metrica a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c2541-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c2541-117">Questo comando crea una regola di avviso metrica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2541-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="c2541-118">$condition è l'output di New-AzMetricAlertRuleV2Criteria cmdlet e $act è l'output del cmdlet New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c2541-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="c2541-119">Esempio 2: aggiungere una regola di avviso metrica per tutte le macchine virtuali in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="c2541-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c2541-120">Questo comando crea una regola di avviso metrica per tutte le macchine virtuali nell'abbonamento che si trovano in eastus</span><span class="sxs-lookup"><span data-stu-id="c2541-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="c2541-121">Esempio 3: disabilitare una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="c2541-121">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c2541-122">Questo comando Disabilita una regola di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="c2541-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="c2541-123">In questo caso, siamo in uscita piping di Get-AzMetricAlertRuleV2 Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c2541-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="c2541-124">Esempio 4: aggiungere una regola di avviso metrica con le dimensioni</span><span class="sxs-lookup"><span data-stu-id="c2541-124">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c2541-125">Per creare una regola di avviso metrica più complessa, ad esempio quelle che prevedono la selezione di valori di dimensione o che hanno più criteri, è possibile usare i cmdlet Helper New-AzMetricAlertRuleV2DimensionSelection e New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="c2541-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="c2541-126">Sopra set di cmdlet verrà creata una regola di avviso metrica con le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c2541-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="c2541-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2541-127">PARAMETERS</span></span>

### <span data-ttu-id="c2541-128">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="c2541-128">-ActionGroup</span></span>
<span data-ttu-id="c2541-129">Gruppo di azioni per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c2541-130">-ActionGroupId</span></span>
<span data-ttu-id="c2541-131">ID del gruppo di azioni per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-132">-Condition</span><span class="sxs-lookup"><span data-stu-id="c2541-132">-Condition</span></span>
<span data-ttu-id="c2541-133">Condizione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-133">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2541-134">-DefaultProfile</span></span>
<span data-ttu-id="c2541-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2541-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-136">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2541-136">-Description</span></span>
<span data-ttu-id="c2541-137">Descrizione della regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="c2541-137">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c2541-138">-DisableRule</span></span>
<span data-ttu-id="c2541-139">Il contrassegno Disabilita regola (stato)</span><span class="sxs-lookup"><span data-stu-id="c2541-139">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-140">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="c2541-140">-Frequency</span></span>
<span data-ttu-id="c2541-141">Frequenza di valutazione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-141">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2541-142">-Name</span></span>
<span data-ttu-id="c2541-143">Nome della regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="c2541-143">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2541-144">-ResourceGroupName</span></span>
<span data-ttu-id="c2541-145">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c2541-145">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-146">-Gravità</span><span class="sxs-lookup"><span data-stu-id="c2541-146">-Severity</span></span>
<span data-ttu-id="c2541-147">Gravità della regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="c2541-147">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c2541-148">-TargetResourceId</span></span>
<span data-ttu-id="c2541-149">ID risorsa di destinazione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="c2541-150">-TargetResourceRegion</span></span>
<span data-ttu-id="c2541-151">Area della risorsa di destinazione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="c2541-152">-TargetResourceScope</span></span>
<span data-ttu-id="c2541-153">Ambito delle risorse di destinazione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="c2541-154">-TargetResourceType</span></span>
<span data-ttu-id="c2541-155">Tipo di risorsa di destinazione per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-156">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="c2541-156">-WindowSize</span></span>
<span data-ttu-id="c2541-157">Dimensioni della finestra per la regola</span><span class="sxs-lookup"><span data-stu-id="c2541-157">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2541-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2541-158">-Confirm</span></span>
<span data-ttu-id="c2541-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2541-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2541-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2541-160">-WhatIf</span></span>
<span data-ttu-id="c2541-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2541-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2541-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2541-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2541-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2541-163">CommonParameters</span></span>
<span data-ttu-id="c2541-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2541-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2541-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2541-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2541-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2541-166">INPUTS</span></span>

### <span data-ttu-id="c2541-167">System. String</span><span class="sxs-lookup"><span data-stu-id="c2541-167">System.String</span></span>

### <span data-ttu-id="c2541-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c2541-168">System.TimeSpan</span></span>

### <span data-ttu-id="c2541-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="c2541-169">System.String[]</span></span>

### <span data-ttu-id="c2541-170">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. Cmdlets. monitor, Version = 1.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c2541-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c2541-171">Microsoft. Azure. Management. monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="c2541-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="c2541-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2541-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c2541-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2541-173">System.Int32</span></span>

## <span data-ttu-id="c2541-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2541-174">OUTPUTS</span></span>

### <span data-ttu-id="c2541-175">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c2541-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="c2541-176">Note</span><span class="sxs-lookup"><span data-stu-id="c2541-176">NOTES</span></span>

## <span data-ttu-id="c2541-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2541-177">RELATED LINKS</span></span>
