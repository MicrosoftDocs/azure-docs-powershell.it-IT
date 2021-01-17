---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486207"
---
# <span data-ttu-id="8175a-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8175a-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="8175a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8175a-102">SYNOPSIS</span></span>
<span data-ttu-id="8175a-103">Creare un analitico (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="8175a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="8175a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8175a-104">SYNTAX</span></span>

### <span data-ttu-id="8175a-105">ScheduledAlertRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8175a-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8175a-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="8175a-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8175a-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="8175a-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8175a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8175a-108">DESCRIPTION</span></span>
<span data-ttu-id="8175a-109">Il cmdlet **New-AzSentinelAlertRule** crea una regola analitica (avviso) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="8175a-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="8175a-110">Per specificare il tipo di regola di avviso da creare, devi specificare uno dei tre parametri, *Fusion*, *scheduled* o *MicrosoftSecurityIncidentCreation*.</span><span class="sxs-lookup"><span data-stu-id="8175a-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="8175a-111">Ogni tipo ha diversi parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="8175a-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="8175a-112">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8175a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8175a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8175a-113">EXAMPLES</span></span>

### <span data-ttu-id="8175a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8175a-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="8175a-115">Questo esempio crea un **AlertRule** del tipo *Fusion* basato sul modello per il *rilevamento degli attacchi multistadio avanzato* e lo archivia nella variabile $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="8175a-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="8175a-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8175a-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="8175a-117">Questo esempio crea un **AlertRule** del tipo *MicrosoftSecurityIncidentCreation* in base al modello per la *creazione di eventi imprevisti basati su Azure Security Center for Alerts*, quindi lo archivia nel $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="8175a-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="8175a-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8175a-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="8175a-119">Questo esempio crea un **DataConnector** del tipo *programmato* e lo archivia nel $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="8175a-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="8175a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8175a-120">PARAMETERS</span></span>

### <span data-ttu-id="8175a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8175a-121">-AlertRuleId</span></span>
<span data-ttu-id="8175a-122">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="8175a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="8175a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="8175a-124">Modello di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="8175a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8175a-125">-DefaultProfile</span></span>
<span data-ttu-id="8175a-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8175a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8175a-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8175a-127">-Description</span></span>
<span data-ttu-id="8175a-128">Descrizione.</span><span class="sxs-lookup"><span data-stu-id="8175a-128">Description.</span></span>

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

### <span data-ttu-id="8175a-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8175a-129">-DisplayName</span></span>
<span data-ttu-id="8175a-130">Nome visualizzato della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="8175a-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="8175a-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="8175a-132">I nomi visualizzati della regola di avviso Escludi filtro.</span><span class="sxs-lookup"><span data-stu-id="8175a-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="8175a-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="8175a-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="8175a-134">Filtro per i nomi visualizzati della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="8175a-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="8175a-135">-Enabled</span></span>
<span data-ttu-id="8175a-136">Regola di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="8175a-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="8175a-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="8175a-137">-Fusion</span></span>
<span data-ttu-id="8175a-138">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="8175a-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="8175a-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="8175a-140">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="8175a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="8175a-141">-ProductFilter</span></span>
<span data-ttu-id="8175a-142">Filtro prodotto regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="8175a-143">-Query</span><span class="sxs-lookup"><span data-stu-id="8175a-143">-Query</span></span>
<span data-ttu-id="8175a-144">Query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="8175a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="8175a-145">-QueryFrequency</span></span>
<span data-ttu-id="8175a-146">Frequenza della query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="8175a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="8175a-147">-QueryPeriod</span></span>
<span data-ttu-id="8175a-148">Periodo di query della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="8175a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8175a-149">-ResourceGroupName</span></span>
<span data-ttu-id="8175a-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8175a-150">Resource group name.</span></span>

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

### <span data-ttu-id="8175a-151">-Programmato</span><span class="sxs-lookup"><span data-stu-id="8175a-151">-Scheduled</span></span>
<span data-ttu-id="8175a-152">Tipo di regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="8175a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="8175a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="8175a-154">Filtro di gravità della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="8175a-155">-Gravità</span><span class="sxs-lookup"><span data-stu-id="8175a-155">-Severity</span></span>
<span data-ttu-id="8175a-156">Gravità degli incidenti.</span><span class="sxs-lookup"><span data-stu-id="8175a-156">Incident Severity.</span></span>

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

### <span data-ttu-id="8175a-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="8175a-157">-SuppressionDuration</span></span>
<span data-ttu-id="8175a-158">Durata della soppressione delle regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="8175a-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="8175a-159">-SuppressionEnabled</span></span>
<span data-ttu-id="8175a-160">Soppressione delle regole di avviso abilitata.</span><span class="sxs-lookup"><span data-stu-id="8175a-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="8175a-161">-Tattica</span><span class="sxs-lookup"><span data-stu-id="8175a-161">-Tactics</span></span>
<span data-ttu-id="8175a-162">Tattica della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="8175a-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="8175a-163">-TriggerOperator</span></span>
<span data-ttu-id="8175a-164">Operatore trigger regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="8175a-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="8175a-165">-TriggerThreshold</span></span>
<span data-ttu-id="8175a-166">Soglia del trigger della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8175a-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="8175a-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8175a-167">-WorkspaceName</span></span>
<span data-ttu-id="8175a-168">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8175a-168">Workspace Name.</span></span>

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

### <span data-ttu-id="8175a-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8175a-169">-Confirm</span></span>
<span data-ttu-id="8175a-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8175a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8175a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8175a-171">-WhatIf</span></span>
<span data-ttu-id="8175a-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8175a-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8175a-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8175a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8175a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8175a-174">CommonParameters</span></span>
<span data-ttu-id="8175a-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8175a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8175a-176">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8175a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8175a-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8175a-177">INPUTS</span></span>

### <span data-ttu-id="8175a-178">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8175a-178">None</span></span>
## <span data-ttu-id="8175a-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8175a-179">OUTPUTS</span></span>

### <span data-ttu-id="8175a-180">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8175a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="8175a-181">Note</span><span class="sxs-lookup"><span data-stu-id="8175a-181">NOTES</span></span>

## <span data-ttu-id="8175a-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8175a-182">RELATED LINKS</span></span>
