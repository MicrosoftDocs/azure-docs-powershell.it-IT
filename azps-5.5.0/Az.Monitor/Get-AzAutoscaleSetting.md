---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
ms.openlocfilehash: 9cc5fe5d6b65a45b74244971566009d7b3a069eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207147"
---
# <span data-ttu-id="f242f-101">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f242f-101">Get-AzAutoscaleSetting</span></span>

## <span data-ttu-id="f242f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f242f-102">SYNOPSIS</span></span>
<span data-ttu-id="f242f-103">Recupera le impostazioni di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="f242f-103">Gets Autoscale settings.</span></span>

## <span data-ttu-id="f242f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f242f-104">SYNTAX</span></span>

```
Get-AzAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f242f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f242f-105">DESCRIPTION</span></span>
<span data-ttu-id="f242f-106">Il **cmdlet Get-AzAutoscaleSetting** ottiene tutte le impostazioni di scala automatica associate a un gruppo di risorse o a un'impostazione di gradazione automatica specificata.</span><span class="sxs-lookup"><span data-stu-id="f242f-106">The **Get-AzAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="f242f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f242f-107">EXAMPLES</span></span>

### <span data-ttu-id="f242f-108">Esempio 1: Ottenere le impostazioni di scala automatica</span><span class="sxs-lookup"><span data-stu-id="f242f-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="f242f-109">Questo comando ottiene le impostazioni di scala automatica assegnate al gruppo di risorse Default-Web-EastUS.</span><span class="sxs-lookup"><span data-stu-id="f242f-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="f242f-110">Esempio 2: Ottenere un'impostazione di scala automatica in base al nome</span><span class="sxs-lookup"><span data-stu-id="f242f-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="f242f-111">Questo comando recupera l'impostazione di scala automatica denominata DefaultServerFarm-Default-Web-EastUS.</span><span class="sxs-lookup"><span data-stu-id="f242f-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="f242f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f242f-112">PARAMETERS</span></span>

### <span data-ttu-id="f242f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f242f-113">-DefaultProfile</span></span>
<span data-ttu-id="f242f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f242f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f242f-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f242f-115">-DetailedOutput</span></span>
<span data-ttu-id="f242f-116">Indica che questa operazione visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="f242f-116">Indicates that this operation displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f242f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f242f-117">-Name</span></span>
<span data-ttu-id="f242f-118">Specifica il nome dell'impostazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f242f-118">Specifies the name of the setting to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f242f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f242f-119">-ResourceGroupName</span></span>
<span data-ttu-id="f242f-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f242f-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f242f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f242f-121">CommonParameters</span></span>
<span data-ttu-id="f242f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f242f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f242f-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f242f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f242f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="f242f-124">INPUTS</span></span>

### <span data-ttu-id="f242f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f242f-125">System.String</span></span>

### <span data-ttu-id="f242f-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f242f-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f242f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f242f-127">OUTPUTS</span></span>

### <span data-ttu-id="f242f-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f242f-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="f242f-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="f242f-129">NOTES</span></span>

## <span data-ttu-id="f242f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f242f-130">RELATED LINKS</span></span>

[<span data-ttu-id="f242f-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f242f-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="f242f-132">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f242f-132">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


