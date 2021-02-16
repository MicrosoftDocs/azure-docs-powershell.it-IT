---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199807"
---
# <span data-ttu-id="c164b-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="c164b-101">Get-AzAlert</span></span>

## <span data-ttu-id="c164b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c164b-102">SYNOPSIS</span></span>
<span data-ttu-id="c164b-103">Ottieni informazioni sugli avvisi</span><span class="sxs-lookup"><span data-stu-id="c164b-103">Get Alerts Information</span></span>

## <span data-ttu-id="c164b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c164b-104">SYNTAX</span></span>

### <span data-ttu-id="c164b-105">AlertsListByFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c164b-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c164b-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="c164b-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c164b-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="c164b-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c164b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c164b-108">DESCRIPTION</span></span>
<span data-ttu-id="c164b-109">Il cmdlet **Get-AzAlert** ottiene le istanze di avviso di avviso più disartiziate.</span><span class="sxs-lookup"><span data-stu-id="c164b-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="c164b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c164b-110">EXAMPLES</span></span>

### <span data-ttu-id="c164b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c164b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="c164b-112">Elencare tutti gli avvisi con gravità sev2 e condizione monitor monitor smersi.</span><span class="sxs-lookup"><span data-stu-id="c164b-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="c164b-113">Se si imposta IncludeContext su true, includere il payload personalizzato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="c164b-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="c164b-114">Usare Format-List per ottenere i dettagli completi di ogni avviso nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c164b-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="c164b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c164b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="c164b-116">Ottenere i dettagli dell'avviso in base all'ID (GUID) o all'ID risorsa (ID ARM risorsa)</span><span class="sxs-lookup"><span data-stu-id="c164b-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="c164b-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c164b-117">Example 3</span></span>

<span data-ttu-id="c164b-118">Ottieni informazioni sugli avvisi.</span><span class="sxs-lookup"><span data-stu-id="c164b-118">Get Alerts Information.</span></span> <span data-ttu-id="c164b-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c164b-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="c164b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c164b-120">PARAMETERS</span></span>

### <span data-ttu-id="c164b-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="c164b-121">-AlertId</span></span>
<span data-ttu-id="c164b-122">Identificatore univoco dell'avviso/ID risorsa dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="c164b-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c164b-123">-AlertRuleId</span></span>
<span data-ttu-id="c164b-124">Filtro in base all'ID regola di avviso</span><span class="sxs-lookup"><span data-stu-id="c164b-124">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="c164b-125">-CustomTimeRange</span></span>
<span data-ttu-id="c164b-126">Formato supportato, \<start-time\> / \<end-time\> in cui l'ora è in formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="c164b-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c164b-127">-DefaultProfile</span></span>
<span data-ttu-id="c164b-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c164b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c164b-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="c164b-129">-IncludeContext</span></span>
<span data-ttu-id="c164b-130">Includi contesto (payload personalizzato) dell'avviso</span><span class="sxs-lookup"><span data-stu-id="c164b-130">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="c164b-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="c164b-132">Includi EgressConfig</span><span class="sxs-lookup"><span data-stu-id="c164b-132">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="c164b-133">-MonitorCondition</span></span>
<span data-ttu-id="c164b-134">Filtro in base a condizione di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c164b-134">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="c164b-135">-MonitorService</span></span>
<span data-ttu-id="c164b-136">Filtro in base al servizio di sterno</span><span class="sxs-lookup"><span data-stu-id="c164b-136">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="c164b-137">-PageCount</span></span>
<span data-ttu-id="c164b-138">Numero di avvisi da recuperare in una pagina.</span><span class="sxs-lookup"><span data-stu-id="c164b-138">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-139">-Select</span><span class="sxs-lookup"><span data-stu-id="c164b-139">-Select</span></span>
<span data-ttu-id="c164b-140">Proiettare i campi obbligatori fuori dall'elemento essenziale.</span><span class="sxs-lookup"><span data-stu-id="c164b-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="c164b-141">L'input previsto è separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="c164b-141">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-142">-Gravità</span><span class="sxs-lookup"><span data-stu-id="c164b-142">-Severity</span></span>
<span data-ttu-id="c164b-143">Filtrare in base alla gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="c164b-143">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c164b-144">-SmartGroupId</span></span>
<span data-ttu-id="c164b-145">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="c164b-145">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="c164b-146">-SortBy</span></span>
<span data-ttu-id="c164b-147">Proprietà di avviso da usare durante l'ordinamento</span><span class="sxs-lookup"><span data-stu-id="c164b-147">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="c164b-148">-SortOrder</span></span>
<span data-ttu-id="c164b-149">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="c164b-149">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-150">-State</span><span class="sxs-lookup"><span data-stu-id="c164b-150">-State</span></span>
<span data-ttu-id="c164b-151">Filtrare in base allo stato di avviso</span><span class="sxs-lookup"><span data-stu-id="c164b-151">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c164b-152">-TargetResourceGroup</span></span>
<span data-ttu-id="c164b-153">Filtrare in base al nome del gruppo di risorse della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="c164b-153">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c164b-154">-TargetResourceId</span></span>
<span data-ttu-id="c164b-155">Filtrare in base all'ID risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="c164b-155">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="c164b-156">-TargetResourceType</span></span>
<span data-ttu-id="c164b-157">Filtrare in base al tipo di risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="c164b-157">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="c164b-158">-TimeRange</span></span>
<span data-ttu-id="c164b-159">Valori di intervallo di tempo supportati: 1h, 1d, 7d, 30d (il valore predefinito è 1d)</span><span class="sxs-lookup"><span data-stu-id="c164b-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c164b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c164b-160">CommonParameters</span></span>
<span data-ttu-id="c164b-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c164b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c164b-162">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c164b-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c164b-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="c164b-163">INPUTS</span></span>

### <span data-ttu-id="c164b-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c164b-164">None</span></span>

## <span data-ttu-id="c164b-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c164b-165">OUTPUTS</span></span>

### <span data-ttu-id="c164b-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="c164b-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="c164b-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="c164b-167">NOTES</span></span>

## <span data-ttu-id="c164b-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c164b-168">RELATED LINKS</span></span>
