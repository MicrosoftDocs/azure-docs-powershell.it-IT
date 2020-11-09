---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296802"
---
# <span data-ttu-id="05c1f-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05c1f-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="05c1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="05c1f-103">Aggiorna una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="05c1f-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="05c1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05c1f-104">SYNTAX</span></span>

### <span data-ttu-id="05c1f-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05c1f-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c1f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05c1f-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05c1f-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c1f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="05c1f-109">Aggiorna una regola di avviso del log inserendo la semantica</span><span class="sxs-lookup"><span data-stu-id="05c1f-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="05c1f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="05c1f-111">Esempio 1: impostare il nome della regola</span><span class="sxs-lookup"><span data-stu-id="05c1f-111">Example 1: Set by rule name</span></span>
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

### <span data-ttu-id="05c1f-112">Esempio 2: imposta per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="05c1f-112">Example 2: Set by Input Object</span></span>
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

### <span data-ttu-id="05c1f-113">Esempio 3: impostato dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="05c1f-113">Example 3: Set by resource Id</span></span>
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

## <span data-ttu-id="05c1f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="05c1f-115">-Azione</span><span class="sxs-lookup"><span data-stu-id="05c1f-115">-Action</span></span>
<span data-ttu-id="05c1f-116">Azione di avviso della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="05c1f-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="05c1f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05c1f-117">-AsJob</span></span>
<span data-ttu-id="05c1f-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="05c1f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05c1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c1f-119">-DefaultProfile</span></span>
<span data-ttu-id="05c1f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05c1f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c1f-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="05c1f-121">-Description</span></span>
<span data-ttu-id="05c1f-122">Descrizione di questo avviso</span><span class="sxs-lookup"><span data-stu-id="05c1f-122">The description for this alert</span></span>

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

### <span data-ttu-id="05c1f-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="05c1f-123">-Enabled</span></span>
<span data-ttu-id="05c1f-124">Stato di avviso di Azure-valori validi-$true $false</span><span class="sxs-lookup"><span data-stu-id="05c1f-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="05c1f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05c1f-125">-InputObject</span></span>
<span data-ttu-id="05c1f-126">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="05c1f-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="05c1f-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="05c1f-127">-Location</span></span>
<span data-ttu-id="05c1f-128">Posizione per l'avviso</span><span class="sxs-lookup"><span data-stu-id="05c1f-128">The location for this alert</span></span>

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

### <span data-ttu-id="05c1f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="05c1f-129">-Name</span></span>
<span data-ttu-id="05c1f-130">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="05c1f-130">The alert name</span></span>

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

### <span data-ttu-id="05c1f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c1f-131">-ResourceGroupName</span></span>
<span data-ttu-id="05c1f-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="05c1f-132">The resource group name</span></span>

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

### <span data-ttu-id="05c1f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05c1f-133">-ResourceId</span></span>
<span data-ttu-id="05c1f-134">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="05c1f-134">The resource Id</span></span>

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

### <span data-ttu-id="05c1f-135">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="05c1f-135">-Schedule</span></span>
<span data-ttu-id="05c1f-136">Pianificazione della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="05c1f-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="05c1f-137">-Origine</span><span class="sxs-lookup"><span data-stu-id="05c1f-137">-Source</span></span>
<span data-ttu-id="05c1f-138">Origine della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="05c1f-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="05c1f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="05c1f-139">-Tag</span></span>
<span data-ttu-id="05c1f-140">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="05c1f-140">Resource tags</span></span>

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

### <span data-ttu-id="05c1f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05c1f-141">-Confirm</span></span>
<span data-ttu-id="05c1f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05c1f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c1f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c1f-143">-WhatIf</span></span>
<span data-ttu-id="05c1f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05c1f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c1f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05c1f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c1f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c1f-146">CommonParameters</span></span>
<span data-ttu-id="05c1f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c1f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c1f-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05c1f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c1f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05c1f-149">INPUTS</span></span>

### <span data-ttu-id="05c1f-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="05c1f-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="05c1f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="05c1f-151">System.String</span></span>

### <span data-ttu-id="05c1f-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="05c1f-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="05c1f-153">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="05c1f-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="05c1f-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="05c1f-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="05c1f-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05c1f-155">OUTPUTS</span></span>

### <span data-ttu-id="05c1f-156">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="05c1f-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="05c1f-157">Note</span><span class="sxs-lookup"><span data-stu-id="05c1f-157">NOTES</span></span>

## <span data-ttu-id="05c1f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05c1f-158">RELATED LINKS</span></span>
