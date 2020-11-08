---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032743"
---
# <span data-ttu-id="27126-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="27126-101">Get-AzAlert</span></span>

## <span data-ttu-id="27126-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27126-102">SYNOPSIS</span></span>
<span data-ttu-id="27126-103">Ottenere informazioni sugli avvisi</span><span class="sxs-lookup"><span data-stu-id="27126-103">Get Alerts Information</span></span>

## <span data-ttu-id="27126-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27126-104">SYNTAX</span></span>

### <span data-ttu-id="27126-105">AlertsListByFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27126-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27126-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="27126-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27126-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="27126-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27126-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27126-108">DESCRIPTION</span></span>
<span data-ttu-id="27126-109">Cmdlet **Get-AzAlert** viene generato istanze di avviso.</span><span class="sxs-lookup"><span data-stu-id="27126-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="27126-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27126-110">EXAMPLES</span></span>

### <span data-ttu-id="27126-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27126-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="27126-112">Elenca tutti gli avvisi con la gravità Sev2 e la condizione del monitor licenziato.</span><span class="sxs-lookup"><span data-stu-id="27126-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="27126-113">L'impostazione di IncludeContext su true include il payload personalizzato di Alert.</span><span class="sxs-lookup"><span data-stu-id="27126-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="27126-114">Usare Format-List per ottenere i dettagli completi di ogni avviso nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="27126-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="27126-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="27126-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="27126-116">Ottenere i dettagli degli avvisi per ID (GUID) o ID risorsa (ID ARM completo)</span><span class="sxs-lookup"><span data-stu-id="27126-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="27126-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="27126-117">Example 3</span></span>

<span data-ttu-id="27126-118">Ottenere informazioni sugli avvisi.</span><span class="sxs-lookup"><span data-stu-id="27126-118">Get Alerts Information.</span></span> <span data-ttu-id="27126-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="27126-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="27126-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27126-120">PARAMETERS</span></span>

### <span data-ttu-id="27126-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="27126-121">-AlertId</span></span>
<span data-ttu-id="27126-122">Identificatore univoco di Alert/ResourceId of Alert.</span><span class="sxs-lookup"><span data-stu-id="27126-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="27126-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="27126-123">-AlertRuleId</span></span>
<span data-ttu-id="27126-124">Filtrare l'ID della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="27126-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="27126-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="27126-125">-CustomTimeRange</span></span>
<span data-ttu-id="27126-126">Formato supportato- \<start-time\> / \<end-time\> dove il tempo è in formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="27126-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="27126-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27126-127">-DefaultProfile</span></span>
<span data-ttu-id="27126-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27126-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27126-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="27126-129">-IncludeContext</span></span>
<span data-ttu-id="27126-130">Includi contesto (payload personalizzato) di Alert</span><span class="sxs-lookup"><span data-stu-id="27126-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="27126-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="27126-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="27126-132">Includi EgressConfig</span><span class="sxs-lookup"><span data-stu-id="27126-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="27126-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="27126-133">-MonitorCondition</span></span>
<span data-ttu-id="27126-134">Filtrare le condizioni del monitor</span><span class="sxs-lookup"><span data-stu-id="27126-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="27126-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="27126-135">-MonitorService</span></span>
<span data-ttu-id="27126-136">Filtrare il servizio moniter</span><span class="sxs-lookup"><span data-stu-id="27126-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="27126-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="27126-137">-PageCount</span></span>
<span data-ttu-id="27126-138">Numero di avvisi da recuperare in una pagina.</span><span class="sxs-lookup"><span data-stu-id="27126-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="27126-139">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="27126-139">-Select</span></span>
<span data-ttu-id="27126-140">Proiettare i campi obbligatori fuori da Essentials.</span><span class="sxs-lookup"><span data-stu-id="27126-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="27126-141">L'input previsto è separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="27126-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="27126-142">-Gravità</span><span class="sxs-lookup"><span data-stu-id="27126-142">-Severity</span></span>
<span data-ttu-id="27126-143">Filtrare la gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="27126-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="27126-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="27126-144">-SmartGroupId</span></span>
<span data-ttu-id="27126-145">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="27126-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="27126-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="27126-146">-SortBy</span></span>
<span data-ttu-id="27126-147">Proprietà Alert da usare durante l'ordinamento</span><span class="sxs-lookup"><span data-stu-id="27126-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="27126-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="27126-148">-SortOrder</span></span>
<span data-ttu-id="27126-149">Ordine di ordinamento</span><span class="sxs-lookup"><span data-stu-id="27126-149">Sort Order</span></span>

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

### <span data-ttu-id="27126-150">-Stato</span><span class="sxs-lookup"><span data-stu-id="27126-150">-State</span></span>
<span data-ttu-id="27126-151">Filtrare lo stato di allerta</span><span class="sxs-lookup"><span data-stu-id="27126-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="27126-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27126-152">-TargetResourceGroup</span></span>
<span data-ttu-id="27126-153">Filtrare il nome del gruppo di risorse della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="27126-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="27126-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="27126-154">-TargetResourceId</span></span>
<span data-ttu-id="27126-155">Filtrare l'ID risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="27126-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="27126-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="27126-156">-TargetResourceType</span></span>
<span data-ttu-id="27126-157">Filtrare il tipo di risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="27126-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="27126-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="27126-158">-TimeRange</span></span>
<span data-ttu-id="27126-159">Valori di intervallo di tempo supportati-1h, 1D, 7D, 30D (il valore predefinito è 1D)</span><span class="sxs-lookup"><span data-stu-id="27126-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="27126-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27126-160">CommonParameters</span></span>
<span data-ttu-id="27126-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27126-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27126-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27126-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27126-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27126-163">INPUTS</span></span>

### <span data-ttu-id="27126-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27126-164">None</span></span>

## <span data-ttu-id="27126-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27126-165">OUTPUTS</span></span>

### <span data-ttu-id="27126-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="27126-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="27126-167">Note</span><span class="sxs-lookup"><span data-stu-id="27126-167">NOTES</span></span>

## <span data-ttu-id="27126-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27126-168">RELATED LINKS</span></span>
