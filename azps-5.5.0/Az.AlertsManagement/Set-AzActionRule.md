---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192591"
---
# <span data-ttu-id="36410-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="36410-101">Set-AzActionRule</span></span>

## <span data-ttu-id="36410-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36410-102">SYNOPSIS</span></span>
<span data-ttu-id="36410-103">Creare o aggiornare una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="36410-103">Create or update an action rule.</span></span>

## <span data-ttu-id="36410-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36410-104">SYNTAX</span></span>

### <span data-ttu-id="36410-105">BySimplifiedFormatDiagnosticsActionRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36410-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36410-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36410-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36410-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="36410-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36410-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="36410-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36410-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36410-109">DESCRIPTION</span></span>
<span data-ttu-id="36410-110">**Set-AzActionRule crea** o aggiorna una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="36410-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="36410-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36410-111">EXAMPLES</span></span>

### <span data-ttu-id="36410-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36410-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="36410-113">Questo cmdlet crea una regola di azione per la compressione, con un ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="36410-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="36410-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="36410-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="36410-115">Questo cmdlet crea una regola azione per il gruppo di azioni, con un elenco dell'ambito dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="36410-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="36410-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="36410-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="36410-117">Questo cmdlet crea una regola azione per le impostazioni di diagnostica, con un ambito di risorse.</span><span class="sxs-lookup"><span data-stu-id="36410-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="36410-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36410-118">PARAMETERS</span></span>

### <span data-ttu-id="36410-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="36410-119">-ActionGroupId</span></span>
<span data-ttu-id="36410-120">ID gruppo azioni che deve essere notificato.</span><span class="sxs-lookup"><span data-stu-id="36410-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="36410-121">-ActionRuleType</span></span>
<span data-ttu-id="36410-122">Formato Json della regola di azione</span><span class="sxs-lookup"><span data-stu-id="36410-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="36410-123">-AlertContextCondition</span></span>
<span data-ttu-id="36410-124">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-125">Contiene:smartgroup</span><span class="sxs-lookup"><span data-stu-id="36410-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="36410-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="36410-127">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-128">Uguale a:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="36410-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36410-129">-DefaultProfile</span></span>
<span data-ttu-id="36410-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36410-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36410-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="36410-131">-Description</span></span>
<span data-ttu-id="36410-132">Descrizione della regola di azione</span><span class="sxs-lookup"><span data-stu-id="36410-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="36410-133">-DescriptionCondition</span></span>
<span data-ttu-id="36410-134">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-135">Contiene:avviso di test</span><span class="sxs-lookup"><span data-stu-id="36410-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36410-136">-InputObject</span></span>
<span data-ttu-id="36410-137">Risorsa regola azione</span><span class="sxs-lookup"><span data-stu-id="36410-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36410-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="36410-138">-MonitorCondition</span></span>
<span data-ttu-id="36410-139">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-140">NotEquals:Risolto</span><span class="sxs-lookup"><span data-stu-id="36410-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="36410-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="36410-142">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-143">Uguale a:Piattaforma,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="36410-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-144">-Name</span><span class="sxs-lookup"><span data-stu-id="36410-144">-Name</span></span>
<span data-ttu-id="36410-145">Nome regola azione</span><span class="sxs-lookup"><span data-stu-id="36410-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="36410-146">-ReccurenceType</span></span>
<span data-ttu-id="36410-147">Specifica la durata in cui deve essere applicata l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="36410-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="36410-148">-ReccurentValue</span></span>
<span data-ttu-id="36410-149">Valori ricorrenza, se applicabile. Nel caso di Settimanale - \[ 1,2 Nel caso \] di Mensile - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="36410-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36410-150">-ResourceGroupName</span></span>
<span data-ttu-id="36410-151">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="36410-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="36410-152">-Scope</span></span>
<span data-ttu-id="36410-153">Elenco di valori separati da virgola</span><span class="sxs-lookup"><span data-stu-id="36410-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="36410-154">-SeverityCondition</span></span>
<span data-ttu-id="36410-155">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-156">Uguale a:Sv0,Sev1</span><span class="sxs-lookup"><span data-stu-id="36410-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-157">-Stato</span><span class="sxs-lookup"><span data-stu-id="36410-157">-Status</span></span>
<span data-ttu-id="36410-158">Stato della regola azione.</span><span class="sxs-lookup"><span data-stu-id="36410-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="36410-159">-SuppressionEndTime</span></span>
<span data-ttu-id="36410-160">Ora di fine eliminazione.</span><span class="sxs-lookup"><span data-stu-id="36410-160">Suppression End Time.</span></span>
<span data-ttu-id="36410-161">Formato 09/12/2018 06:00:00 +Deve essere menzionato in caso di Pianificazione soppressione ricorsiva - Una volta, Ogni giorno, Ogni settimana o Ogni mese.</span><span class="sxs-lookup"><span data-stu-id="36410-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="36410-162">-SuppressionStartTime</span></span>
<span data-ttu-id="36410-163">Ora di inizio della sospensione.</span><span class="sxs-lookup"><span data-stu-id="36410-163">Suppression Start Time.</span></span>
<span data-ttu-id="36410-164">Formato 09/12/2018 06:00:00 +Deve essere menzionato in caso di Pianificazione soppressione ricorsiva - Una volta, Ogni giorno, Ogni settimana o Ogni mese.</span><span class="sxs-lookup"><span data-stu-id="36410-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="36410-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="36410-166">Formato previsto: { \<operation\> : \<comma separated list of values\> } ad esempio.</span><span class="sxs-lookup"><span data-stu-id="36410-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="36410-167">Contiene:Macchine virtuali,Account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="36410-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36410-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36410-168">-Confirm</span></span>
<span data-ttu-id="36410-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36410-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36410-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36410-170">-WhatIf</span></span>
<span data-ttu-id="36410-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36410-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36410-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36410-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36410-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36410-173">CommonParameters</span></span>
<span data-ttu-id="36410-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36410-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36410-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36410-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36410-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="36410-176">INPUTS</span></span>

### <span data-ttu-id="36410-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="36410-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="36410-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36410-178">OUTPUTS</span></span>

### <span data-ttu-id="36410-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="36410-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="36410-180">NOTE</span><span class="sxs-lookup"><span data-stu-id="36410-180">NOTES</span></span>

## <span data-ttu-id="36410-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36410-181">RELATED LINKS</span></span>
