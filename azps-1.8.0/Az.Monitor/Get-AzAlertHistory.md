---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1EDFCAC4-6A66-4124-8192-B7F0D3C5BCFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalerthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertHistory.md
ms.openlocfilehash: 559bc8183f6ac80e248099ea95bf6a957b5ea1f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835107"
---
# <span data-ttu-id="a501b-101">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a501b-101">Get-AzAlertHistory</span></span>

## <span data-ttu-id="a501b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a501b-102">SYNOPSIS</span></span>
<span data-ttu-id="a501b-103">Ottiene la cronologia degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="a501b-103">Gets the history of alerts.</span></span>

## <span data-ttu-id="a501b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a501b-104">SYNTAX</span></span>

```
Get-AzAlertHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a501b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a501b-105">DESCRIPTION</span></span>
<span data-ttu-id="a501b-106">Il cmdlet **Get-AzAlertHistory** ottiene la cronologia degli avvisi Man mano che vengono abilitati, disabilitati, licenziati, risolti e così via.</span><span class="sxs-lookup"><span data-stu-id="a501b-106">The **Get-AzAlertHistory** cmdlet gets the history of alerts as they are enabled, disabled, fired, resolved, and so on.</span></span>

## <span data-ttu-id="a501b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a501b-107">EXAMPLES</span></span>

### <span data-ttu-id="a501b-108">Esempio 1: ottenere la cronologia degli avvisi</span><span class="sxs-lookup"><span data-stu-id="a501b-108">Example 1: Get the alert history</span></span>
```
PS C:\>Get-AzAlertHistory -StartTime 2015-02-11T11:00:00 -EndTime 2015-02-11T12:00:00 -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' has been resolved for Website: 
                       garyyang1 (Default-Web-EastUS) 
EventDataId          : 769fab1c-fc9f-4e18-bc3a-fa79fbdd3616
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:14:45 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/769fab1c-fc
                       9f-4e18-bc3a-fa79fbdd3616/ticks/635592788857929926
Level                : Informational
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
OperationName        : ResolveAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Resolved
SubmissionTimestamp  : 2/11/2015 7:14:45 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : 66277c94-2097-4f5f-860d-e585f1206cd7
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.web/sites/garyyang1/events/66277c94-2097-4f5f-860d-e585f1206cd7/ticks/6355927828650595
                       14
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.web
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.web/sites/garyyang1
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : ec9f7b3c-c6ea-4b45-bd15-ff43e38491e3
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/ec9f7b3c-c6
                       ea-4b45-bd15-ff43e38491e3/ticks/635592782865059514
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="a501b-109">Questo comando consente di ottenere la cronologia degli avvisi per l'intervallo di tempo specificato per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a501b-109">This command gets the alert history for the specified time frame for the current subscription.</span></span>

### <span data-ttu-id="a501b-110">Esempio 2: ottenere la cronologia degli avvisi per una risorsa specificata</span><span class="sxs-lookup"><span data-stu-id="a501b-110">Example 2: Get alert history for a specified resource</span></span>
```
PS C:\>Get-AzAlertHistory -StartTime 2015-02-11T11:00:00 -EndTime 2015-02-11T12:00:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d" -DetailedOutput

Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' has been resolved for Website: 
                       garyyang1 (Default-Web-EastUS) 
EventDataId          : 769fab1c-fc9f-4e18-bc3a-fa79fbdd3616
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:14:45 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/769fab1c-fc
                       9f-4e18-bc3a-fa79fbdd3616/ticks/635592788857929926
Level                : Informational
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
OperationName        : ResolveAlert
Properties           : 
RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleDescription: 
Threshold      : 3
WindowSizeInMinutes: 5
Aggregation    : Total
Operator       : GreaterThan
MetricName     : CpuTime
MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Resolved
SubmissionTimestamp  : 2/11/2015 7:14:45 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : ec9f7b3c-c6ea-4b45-bd15-ff43e38491e3
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/ec9f7b3c-c6
                       ea-4b45-bd15-ff43e38491e3/ticks/635592782865059514
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleDescription: 
Threshold      : 3
WindowSizeInMinutes: 5
Aggregation    : Total
Operator       : GreaterThan
MetricName     : CpuTime
MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="a501b-111">Questo comando ottiene gli eventi correlati alle regole di avviso per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="a501b-111">This command gets the alert rule-related events for a specified resource.</span></span>

## <span data-ttu-id="a501b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a501b-112">PARAMETERS</span></span>

### <span data-ttu-id="a501b-113">-Chiamante</span><span class="sxs-lookup"><span data-stu-id="a501b-113">-Caller</span></span>
<span data-ttu-id="a501b-114">Specifica il chiamante.</span><span class="sxs-lookup"><span data-stu-id="a501b-114">Specifies the caller.</span></span>

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

### <span data-ttu-id="a501b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a501b-115">-DefaultProfile</span></span>
<span data-ttu-id="a501b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a501b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a501b-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="a501b-117">-DetailedOutput</span></span>
<span data-ttu-id="a501b-118">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="a501b-118">Displays full details in the output.</span></span>

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

### <span data-ttu-id="a501b-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a501b-119">-EndTime</span></span>
<span data-ttu-id="a501b-120">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="a501b-120">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="a501b-121">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a501b-121">The default is the current time.</span></span>

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

### <span data-ttu-id="a501b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a501b-122">-ResourceId</span></span>
<span data-ttu-id="a501b-123">Specifica l'ID risorsa a cui è associata la regola.</span><span class="sxs-lookup"><span data-stu-id="a501b-123">Specifies the resource ID the rule is associated with.</span></span>

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

### <span data-ttu-id="a501b-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a501b-124">-StartTime</span></span>
<span data-ttu-id="a501b-125">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="a501b-125">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="a501b-126">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="a501b-126">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="a501b-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="a501b-127">-Status</span></span>
<span data-ttu-id="a501b-128">Specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a501b-128">Specifies the status.</span></span>

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

### <span data-ttu-id="a501b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a501b-129">CommonParameters</span></span>
<span data-ttu-id="a501b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a501b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a501b-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a501b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a501b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a501b-132">INPUTS</span></span>

### <span data-ttu-id="a501b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a501b-133">System.String</span></span>

### <span data-ttu-id="a501b-134">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a501b-134">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a501b-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a501b-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a501b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a501b-136">OUTPUTS</span></span>

### <span data-ttu-id="a501b-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="a501b-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="a501b-138">Note</span><span class="sxs-lookup"><span data-stu-id="a501b-138">NOTES</span></span>

## <span data-ttu-id="a501b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a501b-139">RELATED LINKS</span></span>

[<span data-ttu-id="a501b-140">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a501b-140">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="a501b-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a501b-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="a501b-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a501b-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="a501b-143">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="a501b-143">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="a501b-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="a501b-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


