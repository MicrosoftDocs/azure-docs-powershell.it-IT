---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952749"
---
# <span data-ttu-id="e7c3e-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="e7c3e-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="e7c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c3e-103">Operazione di creazione o aggiornamento di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-103">The operation to create or update a export.</span></span>
<span data-ttu-id="e7c3e-104">Per l'operazione di aggiornamento è necessario impostare l'eTag più recente nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="e7c3e-105">È possibile ottenere l'eTag più recente eseguendo un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="e7c3e-106">L'operazione di creazione non richiede un eTag.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="e7c3e-107">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7c3e-107">SYNTAX</span></span>

### <span data-ttu-id="e7c3e-108">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7c3e-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e7c3e-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e7c3e-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7c3e-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7c3e-110">DESCRIPTION</span></span>
<span data-ttu-id="e7c3e-111">Operazione di creazione o aggiornamento di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-111">The operation to create or update a export.</span></span>
<span data-ttu-id="e7c3e-112">Per l'operazione di aggiornamento è necessario impostare l'eTag più recente nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="e7c3e-113">È possibile ottenere l'eTag più recente eseguendo un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="e7c3e-114">L'operazione di creazione non richiede un eTag.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="e7c3e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7c3e-115">EXAMPLES</span></span>

### <span data-ttu-id="e7c3e-116">Esempio 1: Aggiornare AzCostManagementExport in base all'ambito e al nome</span><span class="sxs-lookup"><span data-stu-id="e7c3e-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="e7c3e-117">Aggiornare AzCostManagementExport in base all'ambito e al nome</span><span class="sxs-lookup"><span data-stu-id="e7c3e-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="e7c3e-118">Esempio 2: Aggiornare AzCostManagementExport per InputObject</span><span class="sxs-lookup"><span data-stu-id="e7c3e-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="e7c3e-119">Aggiornare AzCostManagementExport per InputObject</span><span class="sxs-lookup"><span data-stu-id="e7c3e-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="e7c3e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7c3e-120">PARAMETERS</span></span>

### <span data-ttu-id="e7c3e-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="e7c3e-121">-ConfigurationColumn</span></span>
<span data-ttu-id="e7c3e-122">Matrice dei nomi di colonna da includere nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="e7c3e-123">Se non viene specificato, l'esportazione includerà tutte le colonne disponibili.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="e7c3e-124">Le colonne disponibili possono variare in base al canale del cliente (vedere gli esempi).</span><span class="sxs-lookup"><span data-stu-id="e7c3e-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="e7c3e-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="e7c3e-125">-DataSetGranularity</span></span>
<span data-ttu-id="e7c3e-126">Granularità delle righe nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="e7c3e-127">Attualmente è supportato solo "Giornaliera".</span><span class="sxs-lookup"><span data-stu-id="e7c3e-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="e7c3e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c3e-128">-DefaultProfile</span></span>
<span data-ttu-id="e7c3e-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7c3e-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="e7c3e-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="e7c3e-131">Intervallo di tempo per il pull dei dati per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="e7c3e-132">Se personalizzato, è necessario specificare un periodo di tempo specifico.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="e7c3e-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="e7c3e-133">-DefinitionType</span></span>
<span data-ttu-id="e7c3e-134">Tipo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-134">The type of the export.</span></span>
<span data-ttu-id="e7c3e-135">Si noti che "Utilizzo" è equivalente a "CostoEsterno" ed è applicabile alle esportazioni che non forniscono ancora dati per gli addebiti o gli ammortamenti per le prenotazioni di servizi.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="e7c3e-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="e7c3e-136">-DestinationContainer</span></span>
<span data-ttu-id="e7c3e-137">Nome del contenitore in cui verranno caricate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="e7c3e-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c3e-138">-DestinationResourceId</span></span>
<span data-ttu-id="e7c3e-139">ID risorsa dell'account di archiviazione in cui verranno recapitate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="e7c3e-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="e7c3e-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="e7c3e-141">Nome della directory in cui verranno caricate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="e7c3e-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="e7c3e-142">-ETag</span></span>
<span data-ttu-id="e7c3e-143">eTag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-143">eTag of the resource.</span></span>
<span data-ttu-id="e7c3e-144">Per gestire lo scenario di aggiornamento simultaneo, questo campo verrà usato per determinare se l'utente sta aggiornando la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="e7c3e-145">-Format</span><span class="sxs-lookup"><span data-stu-id="e7c3e-145">-Format</span></span>
<span data-ttu-id="e7c3e-146">Formato dell'esportazione da recapitare.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-146">The format of the export being delivered.</span></span>
<span data-ttu-id="e7c3e-147">Attualmente è supportato solo il formato "Csv".</span><span class="sxs-lookup"><span data-stu-id="e7c3e-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="e7c3e-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7c3e-148">-InputObject</span></span>
<span data-ttu-id="e7c3e-149">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7c3e-150">-Name</span><span class="sxs-lookup"><span data-stu-id="e7c3e-150">-Name</span></span>
<span data-ttu-id="e7c3e-151">Nome esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-151">Export Name.</span></span>

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

### <span data-ttu-id="e7c3e-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="e7c3e-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="e7c3e-153">Data di inizio della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="e7c3e-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="e7c3e-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="e7c3e-155">Data di fine della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="e7c3e-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="e7c3e-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="e7c3e-157">Ricorrenza della programmazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="e7c3e-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="e7c3e-158">-ScheduleStatus</span></span>
<span data-ttu-id="e7c3e-159">Stato della pianificazione dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-159">The status of the export's schedule.</span></span>
<span data-ttu-id="e7c3e-160">Se "Inattivo", la pianificazione dell'esportazione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="e7c3e-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="e7c3e-161">-Scope</span></span>
<span data-ttu-id="e7c3e-162">Questo parametro definisce l'ambito di costmanagement da prospettive diverse, "Sottoscrizione", "GruppoSociezione" e "Fornire servizio".</span><span class="sxs-lookup"><span data-stu-id="e7c3e-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="e7c3e-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="e7c3e-163">-TimePeriodFrom</span></span>
<span data-ttu-id="e7c3e-164">Data di inizio per i dati di esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-164">The start date for export data.</span></span>

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

### <span data-ttu-id="e7c3e-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="e7c3e-165">-TimePeriodTo</span></span>
<span data-ttu-id="e7c3e-166">Data di fine per i dati di esportazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-166">The end date for export data.</span></span>

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

### <span data-ttu-id="e7c3e-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7c3e-167">-Confirm</span></span>
<span data-ttu-id="e7c3e-168">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7c3e-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c3e-169">-WhatIf</span></span>
<span data-ttu-id="e7c3e-170">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c3e-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7c3e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c3e-172">CommonParameters</span></span>
<span data-ttu-id="e7c3e-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c3e-174">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c3e-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7c3e-175">INPUTS</span></span>

### <span data-ttu-id="e7c3e-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="e7c3e-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="e7c3e-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7c3e-177">OUTPUTS</span></span>

### <span data-ttu-id="e7c3e-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="e7c3e-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="e7c3e-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7c3e-179">NOTES</span></span>

<span data-ttu-id="e7c3e-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e7c3e-180">ALIASES</span></span>

<span data-ttu-id="e7c3e-181">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e7c3e-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7c3e-182">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7c3e-183">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7c3e-184">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e7c3e-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7c3e-185">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="e7c3e-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="e7c3e-186">`[ExportName <String>]`: consente di esportare il nome.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="e7c3e-187">`[ExternalCloudProviderId <String>]`: può essere '{externalSubscriptionId}' per l'account collegato o '{externalBillingAccountId}' per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="e7c3e-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: tipo di provider di cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="e7c3e-189">Sono incluse le 'externalSubscriptions' per gli account collegati e 'externalBillingAccounts' per gli account consolidati.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="e7c3e-190">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e7c3e-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7c3e-191">`[Scope <String>]`: ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="e7c3e-192">Ciò include 'subscriptions/{subscriptionId}' per l'ambito della sottoscrizione, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' per l'ambito resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' per l'ambito Account di fatturazione, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' per l'ambito Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' per ambito EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' per l'ambito BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' per l'ambito InvoiceSection, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito Account di fatturazione esterna e 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito Sottoscrizione esterna.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="e7c3e-193">`[ViewName <String>]`: nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e7c3e-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="e7c3e-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7c3e-194">RELATED LINKS</span></span>

