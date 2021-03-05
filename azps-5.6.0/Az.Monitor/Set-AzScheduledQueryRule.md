---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: eefcebbcf1544205fd37201574ed0c3394123bcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960430"
---
# <span data-ttu-id="035a4-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="035a4-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="035a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="035a4-102">SYNOPSIS</span></span>
<span data-ttu-id="035a4-103">Aggiorna una regola di avviso per il log</span><span class="sxs-lookup"><span data-stu-id="035a4-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="035a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="035a4-104">SYNTAX</span></span>

### <span data-ttu-id="035a4-105">ByRuleName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="035a4-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="035a4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="035a4-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="035a4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="035a4-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035a4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="035a4-108">DESCRIPTION</span></span>
<span data-ttu-id="035a4-109">Aggiorna una regola di avviso log per semantica PUT</span><span class="sxs-lookup"><span data-stu-id="035a4-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="035a4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="035a4-110">EXAMPLES</span></span>

### <span data-ttu-id="035a4-111">Esempio 1: Impostare in base al nome della regola</span><span class="sxs-lookup"><span data-stu-id="035a4-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="035a4-112">Esempio 2: Impostare in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="035a4-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="035a4-113">Esempio 3: Impostare in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="035a4-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="035a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="035a4-114">PARAMETERS</span></span>

### <span data-ttu-id="035a4-115">-Action</span><span class="sxs-lookup"><span data-stu-id="035a4-115">-Action</span></span>
<span data-ttu-id="035a4-116">Azione di avviso per la regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="035a4-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="035a4-117">-AsJob</span></span>
<span data-ttu-id="035a4-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="035a4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="035a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035a4-119">-DefaultProfile</span></span>
<span data-ttu-id="035a4-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="035a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="035a4-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="035a4-121">-Description</span></span>
<span data-ttu-id="035a4-122">Descrizione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="035a4-122">The description for this alert</span></span>

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

### <span data-ttu-id="035a4-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="035a4-123">-Enabled</span></span>
<span data-ttu-id="035a4-124">Stato di avviso azure - valori validi - $true, $false</span><span class="sxs-lookup"><span data-stu-id="035a4-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="035a4-125">-InputObject</span></span>
<span data-ttu-id="035a4-126">Risorsa Regola query programmata</span><span class="sxs-lookup"><span data-stu-id="035a4-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-127">-Location</span><span class="sxs-lookup"><span data-stu-id="035a4-127">-Location</span></span>
<span data-ttu-id="035a4-128">Posizione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="035a4-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-129">-Name</span><span class="sxs-lookup"><span data-stu-id="035a4-129">-Name</span></span>
<span data-ttu-id="035a4-130">Nome dell'avviso</span><span class="sxs-lookup"><span data-stu-id="035a4-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="035a4-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="035a4-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="035a4-133">-ResourceId</span></span>
<span data-ttu-id="035a4-134">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="035a4-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-135">-Pianificazione</span><span class="sxs-lookup"><span data-stu-id="035a4-135">-Schedule</span></span>
<span data-ttu-id="035a4-136">Pianificazione delle regole di query pianificate</span><span class="sxs-lookup"><span data-stu-id="035a4-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-137">-Source</span><span class="sxs-lookup"><span data-stu-id="035a4-137">-Source</span></span>
<span data-ttu-id="035a4-138">Origine della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="035a4-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035a4-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="035a4-139">-Tag</span></span>
<span data-ttu-id="035a4-140">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="035a4-140">Resource tags</span></span>

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

### <span data-ttu-id="035a4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="035a4-141">-Confirm</span></span>
<span data-ttu-id="035a4-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035a4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035a4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035a4-143">-WhatIf</span></span>
<span data-ttu-id="035a4-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="035a4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035a4-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="035a4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035a4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035a4-146">CommonParameters</span></span>
<span data-ttu-id="035a4-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035a4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035a4-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="035a4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035a4-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="035a4-149">INPUTS</span></span>

### <span data-ttu-id="035a4-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="035a4-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="035a4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="035a4-151">System.String</span></span>

### <span data-ttu-id="035a4-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="035a4-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="035a4-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="035a4-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="035a4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="035a4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="035a4-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="035a4-155">OUTPUTS</span></span>

### <span data-ttu-id="035a4-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="035a4-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="035a4-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="035a4-157">NOTES</span></span>

## <span data-ttu-id="035a4-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="035a4-158">RELATED LINKS</span></span>
