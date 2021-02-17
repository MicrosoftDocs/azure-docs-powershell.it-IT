---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205898"
---
# <span data-ttu-id="0f1d0-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="0f1d0-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="0f1d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1d0-103">Recupera informazioni di riepilogo degli avvisi</span><span class="sxs-lookup"><span data-stu-id="0f1d0-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="0f1d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f1d0-104">SYNTAX</span></span>

### <span data-ttu-id="0f1d0-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="0f1d0-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f1d0-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="0f1d0-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f1d0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f1d0-107">DESCRIPTION</span></span>
<span data-ttu-id="0f1d0-108">Il cmdlet **Measure-AzAlertStatistic** riceve i dettagli del riepilogo degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="0f1d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f1d0-109">EXAMPLES</span></span>

### <span data-ttu-id="0f1d0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f1d0-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="0f1d0-111">Riepilogare il conteggio degli avvisi raggruppati per gravità e stato filtrato per stato attivo.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="0f1d0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f1d0-112">PARAMETERS</span></span>

### <span data-ttu-id="0f1d0-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0f1d0-113">-AlertRuleId</span></span>
<span data-ttu-id="0f1d0-114">Filtro in base all'ID regola di avviso</span><span class="sxs-lookup"><span data-stu-id="0f1d0-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="0f1d0-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="0f1d0-115">-CustomTimeRange</span></span>
<span data-ttu-id="0f1d0-116">Formato supportato, \<start-time\> / \<end-time\> in cui l'ora è in formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="0f1d0-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="0f1d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1d0-117">-DefaultProfile</span></span>
<span data-ttu-id="0f1d0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f1d0-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="0f1d0-119">-GroupBy</span></span>
<span data-ttu-id="0f1d0-120">Riepiloga per proprietà</span><span class="sxs-lookup"><span data-stu-id="0f1d0-120">Summarize by property</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1d0-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="0f1d0-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="0f1d0-122">Includi conteggio smartgroup</span><span class="sxs-lookup"><span data-stu-id="0f1d0-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="0f1d0-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="0f1d0-123">-MonitorCondition</span></span>
<span data-ttu-id="0f1d0-124">Filtro in base a condizione di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="0f1d0-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="0f1d0-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="0f1d0-125">-MonitorService</span></span>
<span data-ttu-id="0f1d0-126">Filtro in base al servizio di sterno</span><span class="sxs-lookup"><span data-stu-id="0f1d0-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="0f1d0-127">-Gravità</span><span class="sxs-lookup"><span data-stu-id="0f1d0-127">-Severity</span></span>
<span data-ttu-id="0f1d0-128">Filtrare in base alla gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="0f1d0-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="0f1d0-129">-State</span><span class="sxs-lookup"><span data-stu-id="0f1d0-129">-State</span></span>
<span data-ttu-id="0f1d0-130">Filtrare in base allo stato di avviso</span><span class="sxs-lookup"><span data-stu-id="0f1d0-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="0f1d0-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0f1d0-131">-TargetResourceGroup</span></span>
<span data-ttu-id="0f1d0-132">Filtrare in base al nome del gruppo di risorse della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1d0-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0f1d0-133">-TargetResourceId</span></span>
<span data-ttu-id="0f1d0-134">Filtrare in base all'ID risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1d0-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="0f1d0-135">-TargetResourceType</span></span>
<span data-ttu-id="0f1d0-136">Filtrare in base al tipo di risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1d0-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="0f1d0-137">-TimeRange</span></span>
<span data-ttu-id="0f1d0-138">Valori di intervallo di tempo supportati: 1h, 1d, 7d, 30d (il valore predefinito è 1d)</span><span class="sxs-lookup"><span data-stu-id="0f1d0-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="0f1d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1d0-139">CommonParameters</span></span>
<span data-ttu-id="0f1d0-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1d0-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f1d0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1d0-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f1d0-142">INPUTS</span></span>

### <span data-ttu-id="0f1d0-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f1d0-143">None</span></span>

## <span data-ttu-id="0f1d0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f1d0-144">OUTPUTS</span></span>

### <span data-ttu-id="0f1d0-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="0f1d0-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="0f1d0-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f1d0-146">NOTES</span></span>

## <span data-ttu-id="0f1d0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f1d0-147">RELATED LINKS</span></span>
