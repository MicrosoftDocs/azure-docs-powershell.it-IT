---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: c88cd3bbf132ccb7b8913b15dcc66f58ea2d2db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980109"
---
# <span data-ttu-id="da613-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="da613-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="da613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da613-102">SYNOPSIS</span></span>
<span data-ttu-id="da613-103">Ottiene la cronologia della scala automatica.</span><span class="sxs-lookup"><span data-stu-id="da613-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="da613-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da613-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da613-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da613-105">DESCRIPTION</span></span>
<span data-ttu-id="da613-106">Il cmdlet **Get-AzAutoscaleHistory** recupera la cronologia degli eventi correlati a un'impostazione di scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="da613-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="da613-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da613-107">EXAMPLES</span></span>

### <span data-ttu-id="da613-108">Esempio 1: Ottenere tutti gli eventi associati a una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="da613-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="da613-109">Questo comando recupera tutti gli eventi correlati alla scala automatica associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="da613-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="da613-110">Esempio 2: GetAutoscaleHistory per una particolare risorsa</span><span class="sxs-lookup"><span data-stu-id="da613-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="da613-111">Questo comando recupera tutti gli eventi correlati alla scala automatica associati a una particolare risorsa identificata dall'ID della risorsa, essenzialmente ResourceUri.</span><span class="sxs-lookup"><span data-stu-id="da613-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="da613-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da613-112">PARAMETERS</span></span>

### <span data-ttu-id="da613-113">-Caller</span><span class="sxs-lookup"><span data-stu-id="da613-113">-Caller</span></span>
<span data-ttu-id="da613-114">Specifica un chiamante.</span><span class="sxs-lookup"><span data-stu-id="da613-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="da613-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da613-115">-DefaultProfile</span></span>
<span data-ttu-id="da613-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da613-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da613-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="da613-117">-DetailedOutput</span></span>
<span data-ttu-id="da613-118">Indica che questa operazione includeva un output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="da613-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="da613-119">Se non si specifica questo parametro, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="da613-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="da613-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="da613-120">-EndTime</span></span>
<span data-ttu-id="da613-121">Specifica l'ora di fine della query nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="da613-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="da613-122">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da613-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da613-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da613-123">-ResourceId</span></span>
<span data-ttu-id="da613-124">Specifica l'ID della risorsa a cui è associata l'impostazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="da613-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="da613-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="da613-125">-StartTime</span></span>
<span data-ttu-id="da613-126">Specifica l'ora di inizio della query nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="da613-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="da613-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da613-127">This parameter is optional.</span></span>
<span data-ttu-id="da613-128">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="da613-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da613-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="da613-129">-Status</span></span>
<span data-ttu-id="da613-130">Specifica un filtro in base allo stato.</span><span class="sxs-lookup"><span data-stu-id="da613-130">Specifies a filter by status.</span></span>
<span data-ttu-id="da613-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da613-131">This parameter is optional.</span></span>
<span data-ttu-id="da613-132">L'errore è una stringa vuota (ad esempio nessun filtro)</span><span class="sxs-lookup"><span data-stu-id="da613-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="da613-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da613-133">CommonParameters</span></span>
<span data-ttu-id="da613-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da613-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da613-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da613-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da613-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="da613-136">INPUTS</span></span>

### <span data-ttu-id="da613-137">System.String</span><span class="sxs-lookup"><span data-stu-id="da613-137">System.String</span></span>

### <span data-ttu-id="da613-138">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da613-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da613-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da613-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da613-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da613-140">OUTPUTS</span></span>

### <span data-ttu-id="da613-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="da613-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="da613-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="da613-142">NOTES</span></span>

## <span data-ttu-id="da613-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da613-143">RELATED LINKS</span></span>

[<span data-ttu-id="da613-144">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="da613-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="da613-145">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="da613-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="da613-146">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="da613-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


