---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1d58fba402f292c0935fc10715e06b323353046c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864224"
---
# <span data-ttu-id="cf194-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cf194-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="cf194-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf194-102">SYNOPSIS</span></span>
<span data-ttu-id="cf194-103">Aggiorna una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="cf194-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="cf194-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf194-104">SYNTAX</span></span>

### <span data-ttu-id="cf194-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf194-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf194-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf194-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf194-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf194-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf194-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf194-108">DESCRIPTION</span></span>
<span data-ttu-id="cf194-109">Aggiorna una regola di avviso del log, l'aggiornamento solo della proprietà "Enabled" è supportato da questo comando.</span><span class="sxs-lookup"><span data-stu-id="cf194-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="cf194-110">Per aggiornare altre proprietà, vedi comando "set-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="cf194-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="cf194-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf194-111">EXAMPLES</span></span>

### <span data-ttu-id="cf194-112">Esempio 1-aggiornamento per nome regola</span><span class="sxs-lookup"><span data-stu-id="cf194-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="cf194-113">Esempio 2-aggiornamento per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="cf194-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="cf194-114">Esempio 3-aggiornamento per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cf194-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="cf194-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf194-115">PARAMETERS</span></span>

### <span data-ttu-id="cf194-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf194-116">-DefaultProfile</span></span>
<span data-ttu-id="cf194-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf194-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf194-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="cf194-118">-Enabled</span></span>
<span data-ttu-id="cf194-119">Stato di avviso di Azure-valori validi-$true $false</span><span class="sxs-lookup"><span data-stu-id="cf194-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="cf194-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf194-120">-InputObject</span></span>
<span data-ttu-id="cf194-121">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="cf194-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="cf194-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf194-122">-Name</span></span>
<span data-ttu-id="cf194-123">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="cf194-123">The alert name</span></span>

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

### <span data-ttu-id="cf194-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf194-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf194-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cf194-125">The resource group name</span></span>

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

### <span data-ttu-id="cf194-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf194-126">-ResourceId</span></span>
<span data-ttu-id="cf194-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cf194-127">The resource Id</span></span>

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

### <span data-ttu-id="cf194-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf194-128">-Confirm</span></span>
<span data-ttu-id="cf194-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf194-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf194-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf194-130">-WhatIf</span></span>
<span data-ttu-id="cf194-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf194-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf194-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf194-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf194-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf194-133">CommonParameters</span></span>
<span data-ttu-id="cf194-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf194-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf194-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf194-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf194-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf194-136">INPUTS</span></span>

### <span data-ttu-id="cf194-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="cf194-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="cf194-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cf194-138">System.String</span></span>

## <span data-ttu-id="cf194-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf194-139">OUTPUTS</span></span>

### <span data-ttu-id="cf194-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="cf194-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="cf194-141">Note</span><span class="sxs-lookup"><span data-stu-id="cf194-141">NOTES</span></span>

## <span data-ttu-id="cf194-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf194-142">RELATED LINKS</span></span>
