---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010670"
---
# <span data-ttu-id="63576-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="63576-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="63576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63576-102">SYNOPSIS</span></span>
<span data-ttu-id="63576-103">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-103">The operation to create or update a export.</span></span>
<span data-ttu-id="63576-104">Per l'operazione di aggiornamento è necessario impostare l'eTag più recente nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="63576-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="63576-105">È possibile ottenere l'eTag più recente eseguendo un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="63576-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="63576-106">L'operazione di creazione non richiede un eTag.</span><span class="sxs-lookup"><span data-stu-id="63576-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="63576-107">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63576-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63576-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63576-108">DESCRIPTION</span></span>
<span data-ttu-id="63576-109">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-109">The operation to create or update a export.</span></span>
<span data-ttu-id="63576-110">Per l'operazione di aggiornamento è necessario impostare l'eTag più recente nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="63576-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="63576-111">È possibile ottenere l'eTag più recente eseguendo un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="63576-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="63576-112">L'operazione di creazione non richiede un eTag.</span><span class="sxs-lookup"><span data-stu-id="63576-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="63576-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63576-113">EXAMPLES</span></span>

### <span data-ttu-id="63576-114">Esempio 1: Creare un'istanza di AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="63576-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="63576-115">Creare un'istanza di AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="63576-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="63576-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63576-116">PARAMETERS</span></span>

### <span data-ttu-id="63576-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="63576-117">-ConfigurationColumn</span></span>
<span data-ttu-id="63576-118">Matrice dei nomi di colonna da includere nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="63576-119">Se non viene specificato, l'esportazione includerà tutte le colonne disponibili.</span><span class="sxs-lookup"><span data-stu-id="63576-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="63576-120">Le colonne disponibili possono variare in base al canale del cliente (vedere gli esempi).</span><span class="sxs-lookup"><span data-stu-id="63576-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="63576-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="63576-121">-DataSetGranularity</span></span>
<span data-ttu-id="63576-122">Granularità delle righe nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="63576-123">Attualmente è supportato solo "Giornaliera".</span><span class="sxs-lookup"><span data-stu-id="63576-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="63576-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63576-124">-DefaultProfile</span></span>
<span data-ttu-id="63576-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63576-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63576-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="63576-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="63576-127">Intervallo di tempo per il pull dei dati per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="63576-128">Se personalizzato, è necessario specificare un periodo di tempo specifico.</span><span class="sxs-lookup"><span data-stu-id="63576-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="63576-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="63576-129">-DefinitionType</span></span>
<span data-ttu-id="63576-130">Tipo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-130">The type of the export.</span></span>
<span data-ttu-id="63576-131">Si noti che "Utilizzo" è equivalente a "CostoEsterno" ed è applicabile alle esportazioni che non forniscono ancora dati per gli addebiti o gli ammortamenti per le prenotazioni di servizi.</span><span class="sxs-lookup"><span data-stu-id="63576-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="63576-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="63576-132">-DestinationContainer</span></span>
<span data-ttu-id="63576-133">Nome del contenitore in cui verranno caricate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="63576-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="63576-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="63576-134">-DestinationResourceId</span></span>
<span data-ttu-id="63576-135">ID risorsa dell'account di archiviazione in cui verranno recapitate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="63576-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="63576-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="63576-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="63576-137">Nome della directory in cui verranno caricate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="63576-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="63576-138">-Format</span><span class="sxs-lookup"><span data-stu-id="63576-138">-Format</span></span>
<span data-ttu-id="63576-139">Formato dell'esportazione da recapitare.</span><span class="sxs-lookup"><span data-stu-id="63576-139">The format of the export being delivered.</span></span>
<span data-ttu-id="63576-140">Attualmente è supportato solo il formato "Csv".</span><span class="sxs-lookup"><span data-stu-id="63576-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="63576-141">-Name</span><span class="sxs-lookup"><span data-stu-id="63576-141">-Name</span></span>
<span data-ttu-id="63576-142">Nome esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63576-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="63576-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="63576-144">Data di inizio della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="63576-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="63576-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="63576-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="63576-146">Data di fine della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="63576-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="63576-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="63576-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="63576-148">Ricorrenza della programmazione.</span><span class="sxs-lookup"><span data-stu-id="63576-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="63576-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="63576-149">-ScheduleStatus</span></span>
<span data-ttu-id="63576-150">Stato della pianificazione dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-150">The status of the export's schedule.</span></span>
<span data-ttu-id="63576-151">Se "Inattivo", la pianificazione dell'esportazione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="63576-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="63576-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="63576-152">-Scope</span></span>
<span data-ttu-id="63576-153">Questo parametro definisce l'ambito di costmanagement da prospettive diverse, "Sottoscrizione", "GruppoSociezione" e "Fornire servizio".</span><span class="sxs-lookup"><span data-stu-id="63576-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="63576-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="63576-154">-TimePeriodFrom</span></span>
<span data-ttu-id="63576-155">Data di inizio per i dati di esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-155">The start date for export data.</span></span>

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

### <span data-ttu-id="63576-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="63576-156">-TimePeriodTo</span></span>
<span data-ttu-id="63576-157">Data di fine per i dati di esportazione.</span><span class="sxs-lookup"><span data-stu-id="63576-157">The end date for export data.</span></span>

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

### <span data-ttu-id="63576-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63576-158">-Confirm</span></span>
<span data-ttu-id="63576-159">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63576-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63576-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63576-160">-WhatIf</span></span>
<span data-ttu-id="63576-161">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63576-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63576-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63576-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63576-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63576-163">CommonParameters</span></span>
<span data-ttu-id="63576-164">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63576-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63576-165">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63576-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63576-166">INPUT</span><span class="sxs-lookup"><span data-stu-id="63576-166">INPUTS</span></span>

## <span data-ttu-id="63576-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63576-167">OUTPUTS</span></span>

### <span data-ttu-id="63576-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="63576-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="63576-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="63576-169">NOTES</span></span>

<span data-ttu-id="63576-170">ALIAS</span><span class="sxs-lookup"><span data-stu-id="63576-170">ALIASES</span></span>

## <span data-ttu-id="63576-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63576-171">RELATED LINKS</span></span>

