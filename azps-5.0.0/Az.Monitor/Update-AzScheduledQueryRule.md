---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203489"
---
# <span data-ttu-id="f18de-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f18de-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f18de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f18de-102">SYNOPSIS</span></span>
<span data-ttu-id="f18de-103">Aggiorna una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="f18de-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="f18de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f18de-104">SYNTAX</span></span>

### <span data-ttu-id="f18de-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f18de-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f18de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f18de-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f18de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f18de-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f18de-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f18de-108">DESCRIPTION</span></span>
<span data-ttu-id="f18de-109">Aggiorna una regola di avviso del log, l'aggiornamento solo della proprietà "Enabled" è supportato da questo comando.</span><span class="sxs-lookup"><span data-stu-id="f18de-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="f18de-110">Per aggiornare altre proprietà, vedi comando [set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) .</span><span class="sxs-lookup"><span data-stu-id="f18de-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="f18de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f18de-111">EXAMPLES</span></span>

### <span data-ttu-id="f18de-112">Esempio 1: aggiornamento per nome regola</span><span class="sxs-lookup"><span data-stu-id="f18de-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="f18de-113">Esempio 2: aggiornamento per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="f18de-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="f18de-114">Esempio 3: aggiornamento per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="f18de-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="f18de-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f18de-115">PARAMETERS</span></span>

### <span data-ttu-id="f18de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18de-116">-DefaultProfile</span></span>
<span data-ttu-id="f18de-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f18de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f18de-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f18de-118">-Enabled</span></span>
<span data-ttu-id="f18de-119">Stato di avviso di Azure-valori validi-$true $false</span><span class="sxs-lookup"><span data-stu-id="f18de-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="f18de-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f18de-120">-InputObject</span></span>
<span data-ttu-id="f18de-121">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="f18de-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="f18de-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f18de-122">-Name</span></span>
<span data-ttu-id="f18de-123">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="f18de-123">The alert name</span></span>

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

### <span data-ttu-id="f18de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18de-124">-ResourceGroupName</span></span>
<span data-ttu-id="f18de-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f18de-125">The resource group name</span></span>

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

### <span data-ttu-id="f18de-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f18de-126">-ResourceId</span></span>
<span data-ttu-id="f18de-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="f18de-127">The resource Id</span></span>

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

### <span data-ttu-id="f18de-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f18de-128">-Confirm</span></span>
<span data-ttu-id="f18de-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f18de-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f18de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f18de-130">-WhatIf</span></span>
<span data-ttu-id="f18de-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f18de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f18de-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f18de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f18de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18de-133">CommonParameters</span></span>
<span data-ttu-id="f18de-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f18de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18de-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f18de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18de-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f18de-136">INPUTS</span></span>

### <span data-ttu-id="f18de-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f18de-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="f18de-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f18de-138">System.String</span></span>

## <span data-ttu-id="f18de-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f18de-139">OUTPUTS</span></span>

### <span data-ttu-id="f18de-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f18de-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f18de-141">Note</span><span class="sxs-lookup"><span data-stu-id="f18de-141">NOTES</span></span>

## <span data-ttu-id="f18de-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f18de-142">RELATED LINKS</span></span>
