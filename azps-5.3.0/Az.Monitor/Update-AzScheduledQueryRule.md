---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475560"
---
# <span data-ttu-id="23954-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23954-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="23954-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23954-102">SYNOPSIS</span></span>
<span data-ttu-id="23954-103">Aggiorna una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="23954-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="23954-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23954-104">SYNTAX</span></span>

### <span data-ttu-id="23954-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23954-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23954-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23954-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23954-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23954-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23954-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23954-108">DESCRIPTION</span></span>
<span data-ttu-id="23954-109">Aggiorna una regola di avviso del log, l'aggiornamento solo della proprietà "Enabled" è supportato da questo comando.</span><span class="sxs-lookup"><span data-stu-id="23954-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="23954-110">Per aggiornare altre proprietà, vedi comando [set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) .</span><span class="sxs-lookup"><span data-stu-id="23954-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="23954-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23954-111">EXAMPLES</span></span>

### <span data-ttu-id="23954-112">Esempio 1: aggiornamento per nome regola</span><span class="sxs-lookup"><span data-stu-id="23954-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="23954-113">Esempio 2: aggiornamento per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="23954-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="23954-114">Esempio 3: aggiornamento per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="23954-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="23954-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23954-115">PARAMETERS</span></span>

### <span data-ttu-id="23954-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23954-116">-DefaultProfile</span></span>
<span data-ttu-id="23954-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23954-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23954-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="23954-118">-Enabled</span></span>
<span data-ttu-id="23954-119">Stato di avviso di Azure-valori validi-$true $false</span><span class="sxs-lookup"><span data-stu-id="23954-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23954-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23954-120">-InputObject</span></span>
<span data-ttu-id="23954-121">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="23954-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="23954-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="23954-122">-Name</span></span>
<span data-ttu-id="23954-123">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="23954-123">The alert name</span></span>

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

### <span data-ttu-id="23954-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23954-124">-ResourceGroupName</span></span>
<span data-ttu-id="23954-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="23954-125">The resource group name</span></span>

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

### <span data-ttu-id="23954-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23954-126">-ResourceId</span></span>
<span data-ttu-id="23954-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="23954-127">The resource Id</span></span>

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

### <span data-ttu-id="23954-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23954-128">-Confirm</span></span>
<span data-ttu-id="23954-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23954-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23954-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23954-130">-WhatIf</span></span>
<span data-ttu-id="23954-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23954-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23954-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23954-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23954-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23954-133">CommonParameters</span></span>
<span data-ttu-id="23954-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23954-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23954-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23954-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23954-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23954-136">INPUTS</span></span>

### <span data-ttu-id="23954-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="23954-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="23954-138">System. String</span><span class="sxs-lookup"><span data-stu-id="23954-138">System.String</span></span>

## <span data-ttu-id="23954-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23954-139">OUTPUTS</span></span>

### <span data-ttu-id="23954-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="23954-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="23954-141">Note</span><span class="sxs-lookup"><span data-stu-id="23954-141">NOTES</span></span>

## <span data-ttu-id="23954-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23954-142">RELATED LINKS</span></span>
