---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676137"
---
# <span data-ttu-id="d0038-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d0038-101">Set-AzActionRule</span></span>

## <span data-ttu-id="d0038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0038-102">SYNOPSIS</span></span>
<span data-ttu-id="d0038-103">Creare o aggiornare una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="d0038-103">Create or update an action rule.</span></span>

## <span data-ttu-id="d0038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0038-104">SYNTAX</span></span>

### <span data-ttu-id="d0038-105">BySimplifiedFormatDiagnosticsActionRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0038-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0038-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0038-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0038-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="d0038-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0038-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="d0038-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0038-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0038-109">DESCRIPTION</span></span>
<span data-ttu-id="d0038-110">**Set-AzActionRule** crea o aggiorna una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="d0038-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="d0038-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0038-111">EXAMPLES</span></span>

### <span data-ttu-id="d0038-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0038-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="d0038-113">Questo cmdlet crea una regola di azione per Supression.</span><span class="sxs-lookup"><span data-stu-id="d0038-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="d0038-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d0038-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="d0038-115">Questo cmdlet crea una regola di azione per il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="d0038-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="d0038-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d0038-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="d0038-117">Questo cmdlet crea una regola di azione per le impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d0038-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="d0038-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0038-118">PARAMETERS</span></span>

### <span data-ttu-id="d0038-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="d0038-119">-ActionGroupId</span></span>
<span data-ttu-id="d0038-120">ID del gruppo di azioni che deve essere notificato.</span><span class="sxs-lookup"><span data-stu-id="d0038-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="d0038-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="d0038-121">-ActionRuleType</span></span>
<span data-ttu-id="d0038-122">Formato JSON della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d0038-122">Action rule Json format</span></span>

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

### <span data-ttu-id="d0038-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-123">-AlertContextCondition</span></span>
<span data-ttu-id="d0038-124">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-125">Contiene: smartgroups</span><span class="sxs-lookup"><span data-stu-id="d0038-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="d0038-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="d0038-127">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-128">Uguale a:/abbonamenti/ad825170-845c-47dB-8F00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. Insights/metricAlerts/test-MRMC-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="d0038-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="d0038-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0038-129">-DefaultProfile</span></span>
<span data-ttu-id="d0038-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0038-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0038-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0038-131">-Description</span></span>
<span data-ttu-id="d0038-132">Descrizione della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d0038-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="d0038-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-133">-DescriptionCondition</span></span>
<span data-ttu-id="d0038-134">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-135">Contains: Test Alert</span><span class="sxs-lookup"><span data-stu-id="d0038-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="d0038-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0038-136">-InputObject</span></span>
<span data-ttu-id="d0038-137">Risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d0038-137">The action rule resource</span></span>

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

### <span data-ttu-id="d0038-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-138">-MonitorCondition</span></span>
<span data-ttu-id="d0038-139">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-140">NotEquals: risolto</span><span class="sxs-lookup"><span data-stu-id="d0038-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="d0038-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="d0038-142">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-143">Uguale a: Platform, analisi log</span><span class="sxs-lookup"><span data-stu-id="d0038-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="d0038-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0038-144">-Name</span></span>
<span data-ttu-id="d0038-145">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d0038-145">Action rule Name</span></span>

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

### <span data-ttu-id="d0038-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="d0038-146">-ReccurenceType</span></span>
<span data-ttu-id="d0038-147">Specifica la durata in cui deve essere applicata la soppressione.</span><span class="sxs-lookup"><span data-stu-id="d0038-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="d0038-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="d0038-148">-ReccurentValue</span></span>
<span data-ttu-id="d0038-149">Valori reccurent, se applicabile. In caso di Weekly- \[ 1,2 \] in caso di mese- \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="d0038-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="d0038-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0038-150">-ResourceGroupName</span></span>
<span data-ttu-id="d0038-151">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d0038-151">Resource Group Name</span></span>

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

### <span data-ttu-id="d0038-152">-Ambito</span><span class="sxs-lookup"><span data-stu-id="d0038-152">-Scope</span></span>
<span data-ttu-id="d0038-153">Elenco di valori separati da virgole</span><span class="sxs-lookup"><span data-stu-id="d0038-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="d0038-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-154">-SeverityCondition</span></span>
<span data-ttu-id="d0038-155">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-156">Uguale a: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="d0038-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="d0038-157">-Stato</span><span class="sxs-lookup"><span data-stu-id="d0038-157">-Status</span></span>
<span data-ttu-id="d0038-158">Stato della regola di azione.</span><span class="sxs-lookup"><span data-stu-id="d0038-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="d0038-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="d0038-159">-SuppressionEndTime</span></span>
<span data-ttu-id="d0038-160">Ora di fine soppressione.</span><span class="sxs-lookup"><span data-stu-id="d0038-160">Suppression End Time.</span></span>
<span data-ttu-id="d0038-161">Il formato 12/09/2018 06:00:00 + deve essere menzionato in caso di programmazione reccurent Supression, giornaliera, settimanale o mensile.</span><span class="sxs-lookup"><span data-stu-id="d0038-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="d0038-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="d0038-162">-SuppressionStartTime</span></span>
<span data-ttu-id="d0038-163">Ora di inizio soppressione.</span><span class="sxs-lookup"><span data-stu-id="d0038-163">Suppression Start Time.</span></span>
<span data-ttu-id="d0038-164">Il formato 12/09/2018 06:00:00 + deve essere menzionato in caso di programmazione reccurent Supression, giornaliera, settimanale o mensile.</span><span class="sxs-lookup"><span data-stu-id="d0038-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="d0038-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="d0038-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="d0038-166">Formato previsto-{ \< Operation \> : \< elenco di valori separati da virgole \> } per EG.</span><span class="sxs-lookup"><span data-stu-id="d0038-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d0038-167">Contains: macchine virtuali, account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0038-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="d0038-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0038-168">-Confirm</span></span>
<span data-ttu-id="d0038-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0038-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0038-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0038-170">-WhatIf</span></span>
<span data-ttu-id="d0038-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0038-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0038-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0038-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0038-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0038-173">CommonParameters</span></span>
<span data-ttu-id="d0038-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0038-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0038-175">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0038-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0038-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0038-176">INPUTS</span></span>

### <span data-ttu-id="d0038-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d0038-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d0038-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0038-178">OUTPUTS</span></span>

### <span data-ttu-id="d0038-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d0038-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d0038-180">Note</span><span class="sxs-lookup"><span data-stu-id="d0038-180">NOTES</span></span>

## <span data-ttu-id="d0038-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0038-181">RELATED LINKS</span></span>
