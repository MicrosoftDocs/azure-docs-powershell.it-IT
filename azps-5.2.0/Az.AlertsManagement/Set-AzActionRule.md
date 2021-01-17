---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329632"
---
# <span data-ttu-id="7a52c-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="7a52c-101">Set-AzActionRule</span></span>

## <span data-ttu-id="7a52c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a52c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a52c-103">Creare o aggiornare una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-103">Create or update an action rule.</span></span>

## <span data-ttu-id="7a52c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a52c-104">SYNTAX</span></span>

### <span data-ttu-id="7a52c-105">BySimplifiedFormatDiagnosticsActionRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a52c-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a52c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a52c-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a52c-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="7a52c-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a52c-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="7a52c-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a52c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a52c-109">DESCRIPTION</span></span>
<span data-ttu-id="7a52c-110">**Set-AzActionRule** crea o aggiorna una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="7a52c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a52c-111">EXAMPLES</span></span>

### <span data-ttu-id="7a52c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a52c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="7a52c-113">Questo cmdlet crea una regola di azione per Supression, con un ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="7a52c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7a52c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="7a52c-115">Questo cmdlet crea una regola di azione per il gruppo di azioni, con un elenco di ambito gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a52c-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="7a52c-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7a52c-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="7a52c-117">Questo cmdlet crea una regola di azione per le impostazioni di diagnostica, con un ambito delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7a52c-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="7a52c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a52c-118">PARAMETERS</span></span>

### <span data-ttu-id="7a52c-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="7a52c-119">-ActionGroupId</span></span>
<span data-ttu-id="7a52c-120">ID del gruppo di azioni che deve essere notificato.</span><span class="sxs-lookup"><span data-stu-id="7a52c-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="7a52c-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="7a52c-121">-ActionRuleType</span></span>
<span data-ttu-id="7a52c-122">Formato JSON della regola di azione</span><span class="sxs-lookup"><span data-stu-id="7a52c-122">Action rule Json format</span></span>

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

### <span data-ttu-id="7a52c-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-123">-AlertContextCondition</span></span>
<span data-ttu-id="7a52c-124">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-125">Contiene: smartgroups</span><span class="sxs-lookup"><span data-stu-id="7a52c-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="7a52c-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="7a52c-127">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-128">Uguale a:/abbonamenti/ad825170-845c-47dB-8F00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. Insights/metricAlerts/test-MRMC-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="7a52c-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="7a52c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a52c-129">-DefaultProfile</span></span>
<span data-ttu-id="7a52c-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a52c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a52c-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a52c-131">-Description</span></span>
<span data-ttu-id="7a52c-132">Descrizione della regola di azione</span><span class="sxs-lookup"><span data-stu-id="7a52c-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="7a52c-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-133">-DescriptionCondition</span></span>
<span data-ttu-id="7a52c-134">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-135">Contains: Test Alert</span><span class="sxs-lookup"><span data-stu-id="7a52c-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="7a52c-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a52c-136">-InputObject</span></span>
<span data-ttu-id="7a52c-137">Risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="7a52c-137">The action rule resource</span></span>

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

### <span data-ttu-id="7a52c-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-138">-MonitorCondition</span></span>
<span data-ttu-id="7a52c-139">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-140">NotEquals: risolto</span><span class="sxs-lookup"><span data-stu-id="7a52c-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="7a52c-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="7a52c-142">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-143">Uguale a: Platform, analisi log</span><span class="sxs-lookup"><span data-stu-id="7a52c-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="7a52c-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a52c-144">-Name</span></span>
<span data-ttu-id="7a52c-145">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="7a52c-145">Action rule Name</span></span>

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

### <span data-ttu-id="7a52c-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="7a52c-146">-ReccurenceType</span></span>
<span data-ttu-id="7a52c-147">Specifica la durata in cui deve essere applicata la soppressione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="7a52c-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="7a52c-148">-ReccurentValue</span></span>
<span data-ttu-id="7a52c-149">Valori reccurent, se applicabile. In caso di Weekly- \[ 1,2 \] in caso di mese- \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="7a52c-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="7a52c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a52c-150">-ResourceGroupName</span></span>
<span data-ttu-id="7a52c-151">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7a52c-151">Resource Group Name</span></span>

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

### <span data-ttu-id="7a52c-152">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7a52c-152">-Scope</span></span>
<span data-ttu-id="7a52c-153">Elenco di valori separati da virgole</span><span class="sxs-lookup"><span data-stu-id="7a52c-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="7a52c-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-154">-SeverityCondition</span></span>
<span data-ttu-id="7a52c-155">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-156">Uguale a: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="7a52c-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="7a52c-157">-Stato</span><span class="sxs-lookup"><span data-stu-id="7a52c-157">-Status</span></span>
<span data-ttu-id="7a52c-158">Stato della regola di azione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="7a52c-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="7a52c-159">-SuppressionEndTime</span></span>
<span data-ttu-id="7a52c-160">Ora di fine soppressione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-160">Suppression End Time.</span></span>
<span data-ttu-id="7a52c-161">Il formato 12/09/2018 06:00:00 + deve essere menzionato in caso di programmazione reccurent Supression, giornaliera, settimanale o mensile.</span><span class="sxs-lookup"><span data-stu-id="7a52c-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="7a52c-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="7a52c-162">-SuppressionStartTime</span></span>
<span data-ttu-id="7a52c-163">Ora di inizio soppressione.</span><span class="sxs-lookup"><span data-stu-id="7a52c-163">Suppression Start Time.</span></span>
<span data-ttu-id="7a52c-164">Il formato 12/09/2018 06:00:00 + deve essere menzionato in caso di programmazione reccurent Supression, giornaliera, settimanale o mensile.</span><span class="sxs-lookup"><span data-stu-id="7a52c-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="7a52c-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="7a52c-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="7a52c-166">Formato previsto-{ \<operation\> : \<comma separated list of values\> } per EG.</span><span class="sxs-lookup"><span data-stu-id="7a52c-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="7a52c-167">Contains: macchine virtuali, account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7a52c-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="7a52c-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a52c-168">-Confirm</span></span>
<span data-ttu-id="7a52c-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a52c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a52c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a52c-170">-WhatIf</span></span>
<span data-ttu-id="7a52c-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a52c-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a52c-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a52c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a52c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a52c-173">CommonParameters</span></span>
<span data-ttu-id="7a52c-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a52c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a52c-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a52c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a52c-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a52c-176">INPUTS</span></span>

### <span data-ttu-id="7a52c-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7a52c-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7a52c-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a52c-178">OUTPUTS</span></span>

### <span data-ttu-id="7a52c-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7a52c-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7a52c-180">Note</span><span class="sxs-lookup"><span data-stu-id="7a52c-180">NOTES</span></span>

## <span data-ttu-id="7a52c-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a52c-181">RELATED LINKS</span></span>
