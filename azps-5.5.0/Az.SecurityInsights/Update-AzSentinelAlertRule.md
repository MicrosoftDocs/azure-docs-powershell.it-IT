---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191199"
---
# <span data-ttu-id="5646e-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="5646e-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="5646e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5646e-102">SYNOPSIS</span></span>
<span data-ttu-id="5646e-103">Creare una regola analitica (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="5646e-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="5646e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5646e-104">SYNTAX</span></span>

### <span data-ttu-id="5646e-105">AlertRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5646e-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5646e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5646e-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5646e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5646e-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5646e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5646e-108">DESCRIPTION</span></span>
<span data-ttu-id="5646e-109">Il cmdlet **Update-AzSentinelAlertRule** aggiorna un'analisi (regola di avviso) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="5646e-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="5646e-110">È possibile usare un valore -InputObject o -ResourceId o -AlertId.</span><span class="sxs-lookup"><span data-stu-id="5646e-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="5646e-111">È possibile aggiornare 1 o più parmaglie di proprtery.</span><span class="sxs-lookup"><span data-stu-id="5646e-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="5646e-112">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="5646e-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="5646e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5646e-113">EXAMPLES</span></span>

### <span data-ttu-id="5646e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5646e-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="5646e-115">Questo esempio aggiorna **un'impostazione di AlertRule** su *Disabilitato* e la rinomina in *Disabled-AlertRuleDisplayName.*</span><span class="sxs-lookup"><span data-stu-id="5646e-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="5646e-116">Tutte le altre proprietà rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="5646e-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="5646e-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5646e-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="5646e-118">Questo esempio aggiorna un **oggetto AlertRule** usando un oggetto InputObject impostato su *Disabled.*</span><span class="sxs-lookup"><span data-stu-id="5646e-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="5646e-119">Tutte le altre proprietà rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="5646e-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="5646e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5646e-120">PARAMETERS</span></span>

### <span data-ttu-id="5646e-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="5646e-121">-AlertRuleId</span></span>
<span data-ttu-id="5646e-122">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="5646e-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="5646e-124">Modello di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5646e-125">-DefaultProfile</span></span>
<span data-ttu-id="5646e-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5646e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5646e-127">-Description</span></span>
<span data-ttu-id="5646e-128">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="5646e-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="5646e-129">-Disabled</span></span>
<span data-ttu-id="5646e-130">Regola di avviso disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5646e-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5646e-131">-DisplayName</span></span>
<span data-ttu-id="5646e-132">Nome visualizzato della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="5646e-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="5646e-134">Filtro di esclusione dei nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="5646e-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="5646e-136">Filtro dei nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5646e-137">-Enabled</span></span>
<span data-ttu-id="5646e-138">Regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="5646e-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5646e-139">-InputObject</span></span>
<span data-ttu-id="5646e-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="5646e-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="5646e-141">-ProductFilter</span></span>
<span data-ttu-id="5646e-142">Filtro prodotto della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-143">-Query</span><span class="sxs-lookup"><span data-stu-id="5646e-143">-Query</span></span>
<span data-ttu-id="5646e-144">Query delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="5646e-145">-QueryFrequency</span></span>
<span data-ttu-id="5646e-146">Frequenza query regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="5646e-147">-QueryPeriod</span></span>
<span data-ttu-id="5646e-148">Periodo di query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5646e-149">-ResourceGroupName</span></span>
<span data-ttu-id="5646e-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5646e-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5646e-151">-ResourceId</span></span>
<span data-ttu-id="5646e-152">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5646e-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="5646e-153">-SeveritiesFilter</span></span>
<span data-ttu-id="5646e-154">Filtro dei livelli di gravità della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-155">-Gravità</span><span class="sxs-lookup"><span data-stu-id="5646e-155">-Severity</span></span>
<span data-ttu-id="5646e-156">Gravità dell'incidente.</span><span class="sxs-lookup"><span data-stu-id="5646e-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="5646e-157">-SuppressionDisabled</span></span>
<span data-ttu-id="5646e-158">Eliminazione della regola di avviso disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5646e-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="5646e-159">-SuppressionDuration</span></span>
<span data-ttu-id="5646e-160">Durata eliminazione regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="5646e-161">-SuppressionEnabled</span></span>
<span data-ttu-id="5646e-162">Eliminazione della regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="5646e-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-163">-Tattiche</span><span class="sxs-lookup"><span data-stu-id="5646e-163">-Tactics</span></span>
<span data-ttu-id="5646e-164">Tattiche delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="5646e-165">-TriggerOperator</span></span>
<span data-ttu-id="5646e-166">Operatore trigger regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="5646e-167">-TriggerThreshold</span></span>
<span data-ttu-id="5646e-168">Soglia di attivazione regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="5646e-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5646e-169">-WorkspaceName</span></span>
<span data-ttu-id="5646e-170">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5646e-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5646e-171">-Confirm</span></span>
<span data-ttu-id="5646e-172">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5646e-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5646e-173">-WhatIf</span></span>
<span data-ttu-id="5646e-174">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5646e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5646e-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5646e-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5646e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5646e-176">CommonParameters</span></span>
<span data-ttu-id="5646e-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5646e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5646e-178">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5646e-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5646e-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="5646e-179">INPUTS</span></span>

### <span data-ttu-id="5646e-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="5646e-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="5646e-181">System.String</span><span class="sxs-lookup"><span data-stu-id="5646e-181">System.String</span></span>

## <span data-ttu-id="5646e-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5646e-182">OUTPUTS</span></span>

### <span data-ttu-id="5646e-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="5646e-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="5646e-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="5646e-184">NOTES</span></span>

## <span data-ttu-id="5646e-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5646e-185">RELATED LINKS</span></span>
