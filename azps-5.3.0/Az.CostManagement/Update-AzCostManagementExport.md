---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487776"
---
# <span data-ttu-id="7ff0e-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="7ff0e-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="7ff0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ff0e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff0e-103">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-103">The operation to create or update a export.</span></span>
<span data-ttu-id="7ff0e-104">L'operazione di aggiornamento richiede l'impostazione di eTag più recenti nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="7ff0e-105">Per ottenere l'eTag più recente, è possibile eseguire un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="7ff0e-106">Crea operazione non richiede eTag.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="7ff0e-107">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-107">SYNTAX</span></span>

### <span data-ttu-id="7ff0e-108">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ff0e-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ff0e-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7ff0e-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ff0e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ff0e-110">DESCRIPTION</span></span>
<span data-ttu-id="7ff0e-111">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-111">The operation to create or update a export.</span></span>
<span data-ttu-id="7ff0e-112">L'operazione di aggiornamento richiede l'impostazione di eTag più recenti nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="7ff0e-113">Per ottenere l'eTag più recente, è possibile eseguire un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="7ff0e-114">Crea operazione non richiede eTag.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="7ff0e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-115">EXAMPLES</span></span>

### <span data-ttu-id="7ff0e-116">Esempio 1: aggiornare AzCostManagementExport per ambito e nome</span><span class="sxs-lookup"><span data-stu-id="7ff0e-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="7ff0e-117">Aggiornare AzCostManagementExport per ambito e nome</span><span class="sxs-lookup"><span data-stu-id="7ff0e-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="7ff0e-118">Esempio 2: aggiornare AzCostManagementExport da InputObject</span><span class="sxs-lookup"><span data-stu-id="7ff0e-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="7ff0e-119">Aggiornare AzCostManagementExport da InputObject</span><span class="sxs-lookup"><span data-stu-id="7ff0e-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="7ff0e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-120">PARAMETERS</span></span>

### <span data-ttu-id="7ff0e-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="7ff0e-121">-ConfigurationColumn</span></span>
<span data-ttu-id="7ff0e-122">Matrice di nomi di colonna da includere nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="7ff0e-123">Se non viene specificato, l'esportazione includerà tutte le colonne disponibili.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="7ff0e-124">Le colonne disponibili possono variare in base al canale del cliente (Vedi esempi).</span><span class="sxs-lookup"><span data-stu-id="7ff0e-124">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="7ff0e-125">-DataSetGranularity</span></span>
<span data-ttu-id="7ff0e-126">Granularità delle righe nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="7ff0e-127">Attualmente è supportato solo "Daily".</span><span class="sxs-lookup"><span data-stu-id="7ff0e-127">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff0e-128">-DefaultProfile</span></span>
<span data-ttu-id="7ff0e-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="7ff0e-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="7ff0e-131">Intervallo di tempo per l'estrazione dei dati per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="7ff0e-132">Se personalizzato, deve essere specificato un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="7ff0e-133">-DefinitionType</span></span>
<span data-ttu-id="7ff0e-134">Tipo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-134">The type of the export.</span></span>
<span data-ttu-id="7ff0e-135">Tieni presente che "utilizzo" equivale a "ActualCost" ed è applicabile alle esportazioni che non contengono ancora dati per gli oneri o gli ammortamenti per le prenotazioni di servizi.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="7ff0e-136">-DestinationContainer</span></span>
<span data-ttu-id="7ff0e-137">Nome del contenitore in cui verranno caricati gli esportazioni.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="7ff0e-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="7ff0e-138">-DestinationResourceId</span></span>
<span data-ttu-id="7ff0e-139">ID risorsa dell'account di archiviazione in cui verranno recapitate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="7ff0e-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="7ff0e-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="7ff0e-141">Nome della directory in cui verranno caricati gli esportazioni.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="7ff0e-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="7ff0e-142">-ETag</span></span>
<span data-ttu-id="7ff0e-143">eTag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-143">eTag of the resource.</span></span>
<span data-ttu-id="7ff0e-144">Per gestire lo scenario di aggiornamento simultaneo, questo campo verrà usato per determinare se l'utente sta aggiornando la versione più recente o meno.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="7ff0e-145">-Format</span><span class="sxs-lookup"><span data-stu-id="7ff0e-145">-Format</span></span>
<span data-ttu-id="7ff0e-146">Formato dell'esportazione da consegnare.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-146">The format of the export being delivered.</span></span>
<span data-ttu-id="7ff0e-147">Attualmente è supportato solo "CSV".</span><span class="sxs-lookup"><span data-stu-id="7ff0e-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ff0e-148">-InputObject</span></span>
<span data-ttu-id="7ff0e-149">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ff0e-150">-Name</span></span>
<span data-ttu-id="7ff0e-151">Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="7ff0e-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="7ff0e-153">Data di inizio della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-153">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="7ff0e-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="7ff0e-155">Data di fine della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-155">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="7ff0e-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="7ff0e-157">La ricorrenza della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="7ff0e-158">-ScheduleStatus</span></span>
<span data-ttu-id="7ff0e-159">Stato della pianificazione dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-159">The status of the export's schedule.</span></span>
<span data-ttu-id="7ff0e-160">Se "inattivo", la pianificazione dell'esportazione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-161">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7ff0e-161">-Scope</span></span>
<span data-ttu-id="7ff0e-162">Questo parametro definisce l'ambito di Costmanagement da diverse prospettive "abbonamento", "ResourceGroup" e "Fornisci servizio".</span><span class="sxs-lookup"><span data-stu-id="7ff0e-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="7ff0e-163">-TimePeriodFrom</span></span>
<span data-ttu-id="7ff0e-164">Data di inizio per l'esportazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-164">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="7ff0e-165">-TimePeriodTo</span></span>
<span data-ttu-id="7ff0e-166">Data di fine per l'esportazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-166">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ff0e-167">-Confirm</span></span>
<span data-ttu-id="7ff0e-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff0e-169">-WhatIf</span></span>
<span data-ttu-id="7ff0e-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff0e-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff0e-172">CommonParameters</span></span>
<span data-ttu-id="7ff0e-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff0e-174">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ff0e-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff0e-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-175">INPUTS</span></span>

### <span data-ttu-id="7ff0e-176">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="7ff0e-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="7ff0e-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ff0e-177">OUTPUTS</span></span>

### <span data-ttu-id="7ff0e-178">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="7ff0e-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="7ff0e-179">Note</span><span class="sxs-lookup"><span data-stu-id="7ff0e-179">NOTES</span></span>

<span data-ttu-id="7ff0e-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7ff0e-180">ALIASES</span></span>

<span data-ttu-id="7ff0e-181">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ff0e-182">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ff0e-183">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ff0e-184">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7ff0e-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ff0e-185">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="7ff0e-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="7ff0e-186">`[ExportName <String>]`: Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="7ff0e-187">`[ExternalCloudProviderId <String>]`: Può essere "{externalSubscriptionId}" per l'account collegato o "{externalBillingAccountId}" per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="7ff0e-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Il tipo di provider cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="7ff0e-189">Questo include "externalSubscriptions" per l'account collegato e "externalBillingAccounts" per l'account consolidato.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="7ff0e-190">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7ff0e-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ff0e-191">`[Scope <String>]`: L'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="7ff0e-192">Questo include "abbonamenti/{subscriptionId}" per l'ambito di sottoscrizione, "abbonamenti/{subscriptionId}/resourceGroups/{resourceGroupName}" per resourceGroup ambito, "providers/Microsoft. Billing/billingAccounts/{billingAccountId}' per l'ambito dell'account di fatturazione,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/repartis/{IDReparto}' per l'ambito Department,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope,' Providers/Microsoft. Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione,' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito account di fatturazione esterno è Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito di sottoscrizione esterno.</span><span class="sxs-lookup"><span data-stu-id="7ff0e-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="7ff0e-193">`[ViewName <String>]`: Nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="7ff0e-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="7ff0e-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ff0e-194">RELATED LINKS</span></span>

