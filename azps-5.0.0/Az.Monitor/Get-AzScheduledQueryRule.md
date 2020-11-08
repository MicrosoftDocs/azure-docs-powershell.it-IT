---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203506"
---
# <span data-ttu-id="ac174-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ac174-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ac174-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac174-102">SYNOPSIS</span></span>
<span data-ttu-id="ac174-103">Ottiene le risorse di query pianificate</span><span class="sxs-lookup"><span data-stu-id="ac174-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="ac174-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac174-104">SYNTAX</span></span>

### <span data-ttu-id="ac174-105">BySubscriptionOrResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac174-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac174-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="ac174-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac174-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac174-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac174-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac174-108">DESCRIPTION</span></span>
<span data-ttu-id="ac174-109">Ottiene le risorse di query pianificate</span><span class="sxs-lookup"><span data-stu-id="ac174-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="ac174-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac174-110">EXAMPLES</span></span>

### <span data-ttu-id="ac174-111">Esempio 1: elenco per abbonamento o gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ac174-111">Example 1: List by subscription or resource group</span></span>
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

### <span data-ttu-id="ac174-112">Esempio 2: ottenere il nome della regola</span><span class="sxs-lookup"><span data-stu-id="ac174-112">Example 2: Get by rule name</span></span>
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

### <span data-ttu-id="ac174-113">Esempio 3: ottenere per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ac174-113">Example 3: Get by resource Id</span></span>
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

## <span data-ttu-id="ac174-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac174-114">PARAMETERS</span></span>

### <span data-ttu-id="ac174-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac174-115">-DefaultProfile</span></span>
<span data-ttu-id="ac174-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac174-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac174-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac174-117">-Name</span></span>
<span data-ttu-id="ac174-118">Nome della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="ac174-118">The alert rule name</span></span>

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

### <span data-ttu-id="ac174-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac174-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac174-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ac174-120">The resource group name</span></span>

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

### <span data-ttu-id="ac174-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac174-121">-ResourceId</span></span>
<span data-ttu-id="ac174-122">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ac174-122">The resource Id</span></span>

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

### <span data-ttu-id="ac174-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac174-123">CommonParameters</span></span>
<span data-ttu-id="ac174-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac174-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac174-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac174-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac174-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac174-126">INPUTS</span></span>

### <span data-ttu-id="ac174-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac174-127">None</span></span>

## <span data-ttu-id="ac174-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac174-128">OUTPUTS</span></span>

### <span data-ttu-id="ac174-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ac174-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ac174-130">Note</span><span class="sxs-lookup"><span data-stu-id="ac174-130">NOTES</span></span>

## <span data-ttu-id="ac174-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac174-131">RELATED LINKS</span></span>
