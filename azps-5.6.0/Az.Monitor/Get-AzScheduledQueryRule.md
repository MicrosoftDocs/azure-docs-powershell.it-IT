---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 98590e23035810317bf4290513a1c0030b0fcac0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979933"
---
# <span data-ttu-id="1e256-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e256-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="1e256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e256-102">SYNOPSIS</span></span>
<span data-ttu-id="1e256-103">Ottiene risorse query pianificate</span><span class="sxs-lookup"><span data-stu-id="1e256-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="1e256-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e256-104">SYNTAX</span></span>

### <span data-ttu-id="1e256-105">BySubscriptionOrResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e256-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e256-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="1e256-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e256-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e256-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e256-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e256-108">DESCRIPTION</span></span>
<span data-ttu-id="1e256-109">Ottiene risorse query pianificate</span><span class="sxs-lookup"><span data-stu-id="1e256-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="1e256-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e256-110">EXAMPLES</span></span>

### <span data-ttu-id="1e256-111">Esempio 1: Elencare in base alla sottoscrizione o al gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1e256-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="1e256-112">Esempio 2: Ottenere in base al nome della regola</span><span class="sxs-lookup"><span data-stu-id="1e256-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

### <span data-ttu-id="1e256-113">Esempio 3: Ottenere per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="1e256-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

## <span data-ttu-id="1e256-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e256-114">PARAMETERS</span></span>

### <span data-ttu-id="1e256-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e256-115">-DefaultProfile</span></span>
<span data-ttu-id="1e256-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e256-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e256-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e256-117">-Name</span></span>
<span data-ttu-id="1e256-118">Nome della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="1e256-118">The alert rule name</span></span>

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

### <span data-ttu-id="1e256-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e256-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e256-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1e256-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="1e256-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e256-121">-ResourceId</span></span>
<span data-ttu-id="1e256-122">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="1e256-122">The resource Id</span></span>

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

### <span data-ttu-id="1e256-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e256-123">CommonParameters</span></span>
<span data-ttu-id="1e256-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e256-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e256-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e256-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e256-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e256-126">INPUTS</span></span>

### <span data-ttu-id="1e256-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1e256-127">None</span></span>

## <span data-ttu-id="1e256-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e256-128">OUTPUTS</span></span>

### <span data-ttu-id="1e256-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="1e256-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="1e256-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e256-130">NOTES</span></span>

## <span data-ttu-id="1e256-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e256-131">RELATED LINKS</span></span>
