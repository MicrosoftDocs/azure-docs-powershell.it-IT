---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180198"
---
# <span data-ttu-id="45c76-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c76-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="45c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c76-102">SYNOPSIS</span></span>
<span data-ttu-id="45c76-103">Aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="45c76-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="45c76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45c76-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c76-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45c76-105">DESCRIPTION</span></span>
<span data-ttu-id="45c76-106">Il cmdlet **Add-AzMetricAlertRule** aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="45c76-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="45c76-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="45c76-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="45c76-108">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="45c76-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="45c76-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45c76-109">EXAMPLES</span></span>

### <span data-ttu-id="45c76-110">Esempio 1: Aggiungere una regola di avviso metrica a un sito Web</span><span class="sxs-lookup"><span data-stu-id="45c76-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="45c76-111">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="45c76-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="45c76-112">Esempio 2: Disabilitare una regola</span><span class="sxs-lookup"><span data-stu-id="45c76-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="45c76-113">Questo comando disabilita una regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-113">This command disables a rule.</span></span>
<span data-ttu-id="45c76-114">Se la regola non esiste, la regola viene creata e disabilitata.</span><span class="sxs-lookup"><span data-stu-id="45c76-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="45c76-115">Se la regola esiste, viene semplicemente disabilitata.</span><span class="sxs-lookup"><span data-stu-id="45c76-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="45c76-116">Esempio 3: Aggiungere una regola con azioni</span><span class="sxs-lookup"><span data-stu-id="45c76-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="45c76-117">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="45c76-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="45c76-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45c76-118">PARAMETERS</span></span>

### <span data-ttu-id="45c76-119">-Action</span><span class="sxs-lookup"><span data-stu-id="45c76-119">-Action</span></span>
<span data-ttu-id="45c76-120">Specifica un elenco di azioni separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="45c76-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c76-121">-DefaultProfile</span></span>
<span data-ttu-id="45c76-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="45c76-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45c76-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="45c76-123">-Description</span></span>
<span data-ttu-id="45c76-124">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="45c76-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="45c76-125">-DisableRule</span></span>
<span data-ttu-id="45c76-126">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-126">Disables the rule.</span></span>
<span data-ttu-id="45c76-127">Se non si specifica questo parametro, la regola viene abilitata.</span><span class="sxs-lookup"><span data-stu-id="45c76-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="45c76-128">-Location</span><span class="sxs-lookup"><span data-stu-id="45c76-128">-Location</span></span>
<span data-ttu-id="45c76-129">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="45c76-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="45c76-130">-MetricName</span></span>
<span data-ttu-id="45c76-131">Specifica il nome della metrica che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="45c76-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="45c76-132">Specificare questo parametro solo per le regole basate su metriche.</span><span class="sxs-lookup"><span data-stu-id="45c76-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="45c76-133">-Name</span><span class="sxs-lookup"><span data-stu-id="45c76-133">-Name</span></span>
<span data-ttu-id="45c76-134">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="45c76-135">-Operatore</span><span class="sxs-lookup"><span data-stu-id="45c76-135">-Operator</span></span>
<span data-ttu-id="45c76-136">Specifica l'operatore relazionale per la condizione della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="45c76-137">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="45c76-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45c76-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="45c76-138">GreaterThan</span></span>
- <span data-ttu-id="45c76-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="45c76-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="45c76-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="45c76-140">LessThan</span></span>
- <span data-ttu-id="45c76-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="45c76-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c76-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c76-142">-ResourceGroupName</span></span>
<span data-ttu-id="45c76-143">Specifica il nome del gruppo di risorse per la regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="45c76-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="45c76-144">-TargetResourceId</span></span>
<span data-ttu-id="45c76-145">Specifica l'ID della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="45c76-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="45c76-146">NOTA: questa proprietà non può essere aggiornata per una regola di avviso esistente.</span><span class="sxs-lookup"><span data-stu-id="45c76-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="45c76-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="45c76-147">-Threshold</span></span>
<span data-ttu-id="45c76-148">Specifica la soglia della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c76-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="45c76-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="45c76-150">Specifica l'operatore di aggregazione da applicare al periodo di tempo durante la valutazione della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c76-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="45c76-151">-WindowSize</span></span>
<span data-ttu-id="45c76-152">Specifica le dimensioni dell'intervallo di tempo per il calcolo dei dati da parte della regola.</span><span class="sxs-lookup"><span data-stu-id="45c76-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="45c76-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45c76-153">-Confirm</span></span>
<span data-ttu-id="45c76-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c76-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c76-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c76-155">-WhatIf</span></span>
<span data-ttu-id="45c76-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45c76-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45c76-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45c76-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c76-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c76-158">CommonParameters</span></span>
<span data-ttu-id="45c76-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c76-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c76-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45c76-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c76-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="45c76-161">INPUTS</span></span>

### <span data-ttu-id="45c76-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="45c76-162">System.TimeSpan</span></span>

### <span data-ttu-id="45c76-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="45c76-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="45c76-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="45c76-164">System.Double</span></span>

### <span data-ttu-id="45c76-165">System.String</span><span class="sxs-lookup"><span data-stu-id="45c76-165">System.String</span></span>

### <span data-ttu-id="45c76-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="45c76-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="45c76-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45c76-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="45c76-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="45c76-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="45c76-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45c76-169">OUTPUTS</span></span>

### <span data-ttu-id="45c76-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="45c76-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="45c76-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="45c76-171">NOTES</span></span>

## <span data-ttu-id="45c76-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45c76-172">RELATED LINKS</span></span>

[<span data-ttu-id="45c76-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45c76-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="45c76-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c76-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="45c76-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="45c76-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="45c76-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c76-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="45c76-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="45c76-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="45c76-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="45c76-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="45c76-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="45c76-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


