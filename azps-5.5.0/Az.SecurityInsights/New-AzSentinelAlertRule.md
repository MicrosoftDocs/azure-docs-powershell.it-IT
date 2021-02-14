---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201759"
---
# <span data-ttu-id="f9e0f-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9e0f-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="f9e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e0f-103">Creare una regola analitica (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="f9e0f-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="f9e0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9e0f-104">SYNTAX</span></span>

### <span data-ttu-id="f9e0f-105">ScheduledAlertRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9e0f-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e0f-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9e0f-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e0f-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="f9e0f-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9e0f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9e0f-108">DESCRIPTION</span></span>
<span data-ttu-id="f9e0f-109">Il cmdlet **New-AzSentinelAlertRule** crea un'analisi (regola di avviso) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="f9e0f-110">È necessario specificare uno dei tre parametri, *Fusion,* *Scheduled* o *MicrosoftSecurityIncidentCreation,* per specificare il tipo di regola di avviso da creare.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="f9e0f-111">Ogni tipo ha paracadute obbligatori diversi.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="f9e0f-112">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f9e0f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9e0f-113">EXAMPLES</span></span>

### <span data-ttu-id="f9e0f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9e0f-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="f9e0f-115">Questo esempio crea un **oggetto AlertRule** del tipo *Fusione* basato sul modello per il rilevamento avanzato di attacchi *multistage* e quindi lo archivia nella $AlertRule variabile.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="f9e0f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f9e0f-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="f9e0f-117">Questo esempio crea **un oggetto AlertRule** del tipo *MicrosoftSecurityIncidentCreation* basato sul modello Per creare eventi imprevisti basati su Centro sicurezza e protezione di Azure per gli avvisi *IoT* e quindi lo archivia nel formato $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="f9e0f-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f9e0f-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="f9e0f-119">Questo esempio crea **un DataConnector** di tipo *Pianificato* e quindi lo archivia nella $AlertRule varabile.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="f9e0f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9e0f-120">PARAMETERS</span></span>

### <span data-ttu-id="f9e0f-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f9e0f-121">-AlertRuleId</span></span>
<span data-ttu-id="f9e0f-122">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-122">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="f9e0f-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="f9e0f-124">Modello di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e0f-125">-DefaultProfile</span></span>
<span data-ttu-id="f9e0f-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e0f-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9e0f-127">-Description</span></span>
<span data-ttu-id="f9e0f-128">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f9e0f-129">-DisplayName</span></span>
<span data-ttu-id="f9e0f-130">Nome visualizzato della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="f9e0f-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="f9e0f-132">Filtro di esclusione dei nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="f9e0f-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="f9e0f-134">Filtro dei nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f9e0f-135">-Enabled</span></span>
<span data-ttu-id="f9e0f-136">Regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-136">Alert Rule Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="f9e0f-137">-Fusion</span></span>
<span data-ttu-id="f9e0f-138">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="f9e0f-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="f9e0f-140">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="f9e0f-141">-ProductFilter</span></span>
<span data-ttu-id="f9e0f-142">Filtro prodotto della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-143">-Query</span><span class="sxs-lookup"><span data-stu-id="f9e0f-143">-Query</span></span>
<span data-ttu-id="f9e0f-144">Query delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="f9e0f-145">-QueryFrequency</span></span>
<span data-ttu-id="f9e0f-146">Frequenza query regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="f9e0f-147">-QueryPeriod</span></span>
<span data-ttu-id="f9e0f-148">Periodo di query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e0f-149">-ResourceGroupName</span></span>
<span data-ttu-id="f9e0f-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-150">Resource group name.</span></span>

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

### <span data-ttu-id="f9e0f-151">-Pianificata</span><span class="sxs-lookup"><span data-stu-id="f9e0f-151">-Scheduled</span></span>
<span data-ttu-id="f9e0f-152">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="f9e0f-153">-SeveritiesFilter</span></span>
<span data-ttu-id="f9e0f-154">Filtro dei livelli di gravità della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-155">-Gravità</span><span class="sxs-lookup"><span data-stu-id="f9e0f-155">-Severity</span></span>
<span data-ttu-id="f9e0f-156">Gravità dell'incidente.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="f9e0f-157">-SuppressionDuration</span></span>
<span data-ttu-id="f9e0f-158">Durata eliminazione regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f9e0f-159">-SuppressionEnabled</span></span>
<span data-ttu-id="f9e0f-160">Eliminazione della regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-161">-Tattiche</span><span class="sxs-lookup"><span data-stu-id="f9e0f-161">-Tactics</span></span>
<span data-ttu-id="f9e0f-162">Tattiche delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="f9e0f-163">-TriggerOperator</span></span>
<span data-ttu-id="f9e0f-164">Operatore trigger regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="f9e0f-165">-TriggerThreshold</span></span>
<span data-ttu-id="f9e0f-166">Soglia di attivazione regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e0f-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9e0f-167">-WorkspaceName</span></span>
<span data-ttu-id="f9e0f-168">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-168">Workspace Name.</span></span>

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

### <span data-ttu-id="f9e0f-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9e0f-169">-Confirm</span></span>
<span data-ttu-id="f9e0f-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9e0f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9e0f-171">-WhatIf</span></span>
<span data-ttu-id="f9e0f-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9e0f-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9e0f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e0f-174">CommonParameters</span></span>
<span data-ttu-id="f9e0f-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e0f-176">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9e0f-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e0f-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9e0f-177">INPUTS</span></span>

### <span data-ttu-id="f9e0f-178">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f9e0f-178">None</span></span>
## <span data-ttu-id="f9e0f-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9e0f-179">OUTPUTS</span></span>

### <span data-ttu-id="f9e0f-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9e0f-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="f9e0f-181">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9e0f-181">NOTES</span></span>

## <span data-ttu-id="f9e0f-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9e0f-182">RELATED LINKS</span></span>
