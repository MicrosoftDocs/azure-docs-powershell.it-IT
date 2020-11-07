---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676148"
---
# <span data-ttu-id="8288f-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="8288f-101">Get-AzAlert</span></span>

## <span data-ttu-id="8288f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8288f-102">SYNOPSIS</span></span>
<span data-ttu-id="8288f-103">Ottenere informazioni sugli avvisi</span><span class="sxs-lookup"><span data-stu-id="8288f-103">Get Alerts Information</span></span>

## <span data-ttu-id="8288f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8288f-104">SYNTAX</span></span>

### <span data-ttu-id="8288f-105">AlertsListByFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8288f-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8288f-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="8288f-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8288f-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="8288f-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8288f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8288f-108">DESCRIPTION</span></span>
<span data-ttu-id="8288f-109">Cmdlet **Get-AzAlert** viene generato istanze di avviso.</span><span class="sxs-lookup"><span data-stu-id="8288f-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="8288f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8288f-110">EXAMPLES</span></span>

### <span data-ttu-id="8288f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8288f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="8288f-112">Elenca tutti gli avvisi con la gravità Sev2 e la condizione del monitor licenziato.</span><span class="sxs-lookup"><span data-stu-id="8288f-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="8288f-113">L'impostazione di IncludeContext su true include il payload personalizzato di Alert.</span><span class="sxs-lookup"><span data-stu-id="8288f-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="8288f-114">Usare Format-List per ottenere i dettagli completi di ogni avviso nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="8288f-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="8288f-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8288f-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="8288f-116">Ottenere i dettagli degli avvisi per ID (GUID) o ID risorsa (ID ARM completo)</span><span class="sxs-lookup"><span data-stu-id="8288f-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="8288f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8288f-117">PARAMETERS</span></span>

### <span data-ttu-id="8288f-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="8288f-118">-AlertId</span></span>
<span data-ttu-id="8288f-119">Identificatore univoco di Alert/ResourceId of Alert.</span><span class="sxs-lookup"><span data-stu-id="8288f-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="8288f-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8288f-120">-AlertRuleId</span></span>
<span data-ttu-id="8288f-121">Filtrare l'ID della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="8288f-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="8288f-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="8288f-122">-CustomTimeRange</span></span>
<span data-ttu-id="8288f-123">Formato supportato- \< inizio-ora \> / \< di fine periodo \> in cui il tempo è in formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="8288f-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="8288f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8288f-124">-DefaultProfile</span></span>
<span data-ttu-id="8288f-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8288f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8288f-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="8288f-126">-IncludeContext</span></span>
<span data-ttu-id="8288f-127">Includi contesto (payload personalizzato) di Alert</span><span class="sxs-lookup"><span data-stu-id="8288f-127">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="8288f-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="8288f-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="8288f-129">Includi EgressConfig</span><span class="sxs-lookup"><span data-stu-id="8288f-129">Include EgressConfig</span></span>

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

### <span data-ttu-id="8288f-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="8288f-130">-MonitorCondition</span></span>
<span data-ttu-id="8288f-131">Filtrare le condizioni del monitor</span><span class="sxs-lookup"><span data-stu-id="8288f-131">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="8288f-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="8288f-132">-MonitorService</span></span>
<span data-ttu-id="8288f-133">Filtrare il servizio moniter</span><span class="sxs-lookup"><span data-stu-id="8288f-133">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="8288f-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="8288f-134">-PageCount</span></span>
<span data-ttu-id="8288f-135">Numero di avvisi da recuperare in una pagina.</span><span class="sxs-lookup"><span data-stu-id="8288f-135">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="8288f-136">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="8288f-136">-Select</span></span>
<span data-ttu-id="8288f-137">Proiettare i campi obbligatori fuori da Essentials.</span><span class="sxs-lookup"><span data-stu-id="8288f-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="8288f-138">L'input previsto è separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="8288f-138">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="8288f-139">-Gravità</span><span class="sxs-lookup"><span data-stu-id="8288f-139">-Severity</span></span>
<span data-ttu-id="8288f-140">Filtrare la gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="8288f-140">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="8288f-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="8288f-141">-SmartGroupId</span></span>
<span data-ttu-id="8288f-142">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="8288f-142">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="8288f-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="8288f-143">-SortBy</span></span>
<span data-ttu-id="8288f-144">Proprietà Alert da usare durante l'ordinamento</span><span class="sxs-lookup"><span data-stu-id="8288f-144">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="8288f-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="8288f-145">-SortOrder</span></span>
<span data-ttu-id="8288f-146">Ordine di ordinamento</span><span class="sxs-lookup"><span data-stu-id="8288f-146">Sort Order</span></span>

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

### <span data-ttu-id="8288f-147">-Stato</span><span class="sxs-lookup"><span data-stu-id="8288f-147">-State</span></span>
<span data-ttu-id="8288f-148">Filtrare lo stato di allerta</span><span class="sxs-lookup"><span data-stu-id="8288f-148">Filter on State of alert</span></span>

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

### <span data-ttu-id="8288f-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8288f-149">-TargetResourceGroup</span></span>
<span data-ttu-id="8288f-150">Filtrare il nome del gruppo di risorse della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="8288f-150">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="8288f-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8288f-151">-TargetResourceId</span></span>
<span data-ttu-id="8288f-152">Filtrare l'ID risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="8288f-152">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="8288f-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="8288f-153">-TargetResourceType</span></span>
<span data-ttu-id="8288f-154">Filtrare il tipo di risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="8288f-154">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="8288f-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="8288f-155">-TimeRange</span></span>
<span data-ttu-id="8288f-156">Valori di intervallo di tempo supportati-1h, 1D, 7D, 30D (il valore predefinito è 1D)</span><span class="sxs-lookup"><span data-stu-id="8288f-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="8288f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8288f-157">CommonParameters</span></span>
<span data-ttu-id="8288f-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8288f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8288f-159">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8288f-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8288f-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8288f-160">INPUTS</span></span>

### <span data-ttu-id="8288f-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8288f-161">None</span></span>

## <span data-ttu-id="8288f-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8288f-162">OUTPUTS</span></span>

### <span data-ttu-id="8288f-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="8288f-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="8288f-164">Note</span><span class="sxs-lookup"><span data-stu-id="8288f-164">NOTES</span></span>

## <span data-ttu-id="8288f-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8288f-165">RELATED LINKS</span></span>
