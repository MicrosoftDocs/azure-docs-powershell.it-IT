---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338923"
---
# <span data-ttu-id="77309-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="77309-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="77309-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77309-102">SYNOPSIS</span></span>
<span data-ttu-id="77309-103">Ottiene le informazioni di riepilogo degli avvisi</span><span class="sxs-lookup"><span data-stu-id="77309-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="77309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77309-104">SYNTAX</span></span>

### <span data-ttu-id="77309-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="77309-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77309-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="77309-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77309-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77309-107">DESCRIPTION</span></span>
<span data-ttu-id="77309-108">Il cmdlet **Measure-AzAlertStatistic** ottiene i dettagli di riepilogo degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="77309-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="77309-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77309-109">EXAMPLES</span></span>

### <span data-ttu-id="77309-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77309-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="77309-111">Riepilogare gli avvisi contati raggruppati per gravità e stato filtrati per stato attivo.</span><span class="sxs-lookup"><span data-stu-id="77309-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="77309-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77309-112">PARAMETERS</span></span>

### <span data-ttu-id="77309-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="77309-113">-AlertRuleId</span></span>
<span data-ttu-id="77309-114">Filtrare l'ID della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="77309-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="77309-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="77309-115">-CustomTimeRange</span></span>
<span data-ttu-id="77309-116">Formato supportato- \<start-time\> / \<end-time\> dove il tempo è in formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="77309-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="77309-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77309-117">-DefaultProfile</span></span>
<span data-ttu-id="77309-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77309-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77309-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="77309-119">-GroupBy</span></span>
<span data-ttu-id="77309-120">Riepilogo per proprietà</span><span class="sxs-lookup"><span data-stu-id="77309-120">Summarize by property</span></span>

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

### <span data-ttu-id="77309-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="77309-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="77309-122">Includi conteggio SmartGroups</span><span class="sxs-lookup"><span data-stu-id="77309-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="77309-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="77309-123">-MonitorCondition</span></span>
<span data-ttu-id="77309-124">Filtrare le condizioni del monitor</span><span class="sxs-lookup"><span data-stu-id="77309-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="77309-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="77309-125">-MonitorService</span></span>
<span data-ttu-id="77309-126">Filtrare il servizio moniter</span><span class="sxs-lookup"><span data-stu-id="77309-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="77309-127">-Gravità</span><span class="sxs-lookup"><span data-stu-id="77309-127">-Severity</span></span>
<span data-ttu-id="77309-128">Filtrare la gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="77309-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="77309-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="77309-129">-State</span></span>
<span data-ttu-id="77309-130">Filtrare lo stato di allerta</span><span class="sxs-lookup"><span data-stu-id="77309-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="77309-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77309-131">-TargetResourceGroup</span></span>
<span data-ttu-id="77309-132">Filtrare il nome del gruppo di risorse della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="77309-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="77309-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="77309-133">-TargetResourceId</span></span>
<span data-ttu-id="77309-134">Filtrare l'ID risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="77309-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="77309-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="77309-135">-TargetResourceType</span></span>
<span data-ttu-id="77309-136">Filtrare il tipo di risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="77309-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="77309-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="77309-137">-TimeRange</span></span>
<span data-ttu-id="77309-138">Valori di intervallo di tempo supportati-1h, 1D, 7D, 30D (il valore predefinito è 1D)</span><span class="sxs-lookup"><span data-stu-id="77309-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="77309-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77309-139">CommonParameters</span></span>
<span data-ttu-id="77309-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77309-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77309-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77309-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77309-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77309-142">INPUTS</span></span>

### <span data-ttu-id="77309-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77309-143">None</span></span>

## <span data-ttu-id="77309-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77309-144">OUTPUTS</span></span>

### <span data-ttu-id="77309-145">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="77309-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="77309-146">Note</span><span class="sxs-lookup"><span data-stu-id="77309-146">NOTES</span></span>

## <span data-ttu-id="77309-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77309-147">RELATED LINKS</span></span>
