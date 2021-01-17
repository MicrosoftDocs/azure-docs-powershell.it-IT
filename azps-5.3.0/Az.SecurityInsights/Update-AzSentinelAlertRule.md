---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486163"
---
# <span data-ttu-id="709b4-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="709b4-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="709b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="709b4-102">SYNOPSIS</span></span>
<span data-ttu-id="709b4-103">Creare un analitico (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="709b4-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="709b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="709b4-104">SYNTAX</span></span>

### <span data-ttu-id="709b4-105">AlertRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="709b4-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="709b4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="709b4-106">InputObject</span></span>
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

### <span data-ttu-id="709b4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="709b4-107">ResourceId</span></span>
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

## <span data-ttu-id="709b4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="709b4-108">DESCRIPTION</span></span>
<span data-ttu-id="709b4-109">Il cmdlet **Update-AzSentinelAlertRule** aggiorna una regola analitica (Alert Rule) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="709b4-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="709b4-110">Puoi usare an-InputObject oppure-ResourceId o-AlertId.</span><span class="sxs-lookup"><span data-stu-id="709b4-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="709b4-111">È possibile aggiornare 1 o più proprtery parmaters.</span><span class="sxs-lookup"><span data-stu-id="709b4-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="709b4-112">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="709b4-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="709b4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="709b4-113">EXAMPLES</span></span>

### <span data-ttu-id="709b4-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="709b4-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="709b4-115">Questo esempio aggiorna un **AlertRule** impostandolo su *disabled* e Rinomina in *disabled-AlertRuleDisplayName*.</span><span class="sxs-lookup"><span data-stu-id="709b4-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="709b4-116">Tutte le altre proprietà rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="709b4-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="709b4-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="709b4-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="709b4-118">Questo esempio aggiorna un **AlertRule** usando un InputObject impostandolo su *disabled*.</span><span class="sxs-lookup"><span data-stu-id="709b4-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="709b4-119">Tutte le altre proprietà rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="709b4-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="709b4-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="709b4-120">PARAMETERS</span></span>

### <span data-ttu-id="709b4-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="709b4-121">-AlertRuleId</span></span>
<span data-ttu-id="709b4-122">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="709b4-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="709b4-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="709b4-124">Modello di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="709b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709b4-125">-DefaultProfile</span></span>
<span data-ttu-id="709b4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="709b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709b4-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="709b4-127">-Description</span></span>
<span data-ttu-id="709b4-128">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="709b4-128">Description.</span></span>

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

### <span data-ttu-id="709b4-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="709b4-129">-Disabled</span></span>
<span data-ttu-id="709b4-130">Regola di avviso disabilitata.</span><span class="sxs-lookup"><span data-stu-id="709b4-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="709b4-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="709b4-131">-DisplayName</span></span>
<span data-ttu-id="709b4-132">Nome visualizzato della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="709b4-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="709b4-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="709b4-134">I nomi visualizzati della regola di avviso Escludi filtro.</span><span class="sxs-lookup"><span data-stu-id="709b4-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="709b4-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="709b4-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="709b4-136">Filtro per i nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="709b4-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="709b4-137">-Enabled</span></span>
<span data-ttu-id="709b4-138">Regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="709b4-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="709b4-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="709b4-139">-InputObject</span></span>
<span data-ttu-id="709b4-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="709b4-140">InputObject.</span></span>

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

### <span data-ttu-id="709b4-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="709b4-141">-ProductFilter</span></span>
<span data-ttu-id="709b4-142">Filtro prodotto regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="709b4-143">-Query</span><span class="sxs-lookup"><span data-stu-id="709b4-143">-Query</span></span>
<span data-ttu-id="709b4-144">Query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="709b4-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="709b4-145">-QueryFrequency</span></span>
<span data-ttu-id="709b4-146">Frequenza della query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="709b4-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="709b4-147">-QueryPeriod</span></span>
<span data-ttu-id="709b4-148">Periodo di query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="709b4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="709b4-149">-ResourceGroupName</span></span>
<span data-ttu-id="709b4-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="709b4-150">Resource group name.</span></span>

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

### <span data-ttu-id="709b4-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="709b4-151">-ResourceId</span></span>
<span data-ttu-id="709b4-152">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="709b4-152">Resource Id.</span></span>

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

### <span data-ttu-id="709b4-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="709b4-153">-SeveritiesFilter</span></span>
<span data-ttu-id="709b4-154">Filtro di gravità della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="709b4-155">-Gravità</span><span class="sxs-lookup"><span data-stu-id="709b4-155">-Severity</span></span>
<span data-ttu-id="709b4-156">Gravità degli incidenti.</span><span class="sxs-lookup"><span data-stu-id="709b4-156">Incident Severity.</span></span>

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

### <span data-ttu-id="709b4-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="709b4-157">-SuppressionDisabled</span></span>
<span data-ttu-id="709b4-158">Soppressione della regola di avviso disabilitata.</span><span class="sxs-lookup"><span data-stu-id="709b4-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="709b4-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="709b4-159">-SuppressionDuration</span></span>
<span data-ttu-id="709b4-160">Durata della soppressione delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="709b4-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="709b4-161">-SuppressionEnabled</span></span>
<span data-ttu-id="709b4-162">Soppressione delle regole di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="709b4-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="709b4-163">-Tattica</span><span class="sxs-lookup"><span data-stu-id="709b4-163">-Tactics</span></span>
<span data-ttu-id="709b4-164">Tattica della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="709b4-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="709b4-165">-TriggerOperator</span></span>
<span data-ttu-id="709b4-166">Operatore trigger regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="709b4-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="709b4-167">-TriggerThreshold</span></span>
<span data-ttu-id="709b4-168">Soglia del trigger della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="709b4-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="709b4-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="709b4-169">-WorkspaceName</span></span>
<span data-ttu-id="709b4-170">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="709b4-170">Workspace Name.</span></span>

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

### <span data-ttu-id="709b4-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="709b4-171">-Confirm</span></span>
<span data-ttu-id="709b4-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="709b4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709b4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709b4-173">-WhatIf</span></span>
<span data-ttu-id="709b4-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="709b4-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="709b4-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="709b4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709b4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709b4-176">CommonParameters</span></span>
<span data-ttu-id="709b4-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709b4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709b4-178">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="709b4-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709b4-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="709b4-179">INPUTS</span></span>

### <span data-ttu-id="709b4-180">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="709b4-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="709b4-181">System. String</span><span class="sxs-lookup"><span data-stu-id="709b4-181">System.String</span></span>

## <span data-ttu-id="709b4-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="709b4-182">OUTPUTS</span></span>

### <span data-ttu-id="709b4-183">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="709b4-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="709b4-184">Note</span><span class="sxs-lookup"><span data-stu-id="709b4-184">NOTES</span></span>

## <span data-ttu-id="709b4-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="709b4-185">RELATED LINKS</span></span>
