---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336664"
---
# <span data-ttu-id="b7bbc-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="b7bbc-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="b7bbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bbc-103">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-103">The operation to create or update a export.</span></span>
<span data-ttu-id="b7bbc-104">L'operazione di aggiornamento richiede l'impostazione di eTag più recenti nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="b7bbc-105">Per ottenere l'eTag più recente, è possibile eseguire un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="b7bbc-106">Crea operazione non richiede eTag.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="b7bbc-107">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7bbc-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7bbc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7bbc-108">DESCRIPTION</span></span>
<span data-ttu-id="b7bbc-109">Operazione per creare o aggiornare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-109">The operation to create or update a export.</span></span>
<span data-ttu-id="b7bbc-110">L'operazione di aggiornamento richiede l'impostazione di eTag più recenti nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="b7bbc-111">Per ottenere l'eTag più recente, è possibile eseguire un'operazione get.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="b7bbc-112">Crea operazione non richiede eTag.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="b7bbc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7bbc-113">EXAMPLES</span></span>

### <span data-ttu-id="b7bbc-114">Esempio 1: creare un AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="b7bbc-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="b7bbc-115">Creare un AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="b7bbc-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="b7bbc-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7bbc-116">PARAMETERS</span></span>

### <span data-ttu-id="b7bbc-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="b7bbc-117">-ConfigurationColumn</span></span>
<span data-ttu-id="b7bbc-118">Matrice di nomi di colonna da includere nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="b7bbc-119">Se non viene specificato, l'esportazione includerà tutte le colonne disponibili.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="b7bbc-120">Le colonne disponibili possono variare in base al canale del cliente (Vedi esempi).</span><span class="sxs-lookup"><span data-stu-id="b7bbc-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="b7bbc-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="b7bbc-121">-DataSetGranularity</span></span>
<span data-ttu-id="b7bbc-122">Granularità delle righe nell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="b7bbc-123">Attualmente è supportato solo "Daily".</span><span class="sxs-lookup"><span data-stu-id="b7bbc-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="b7bbc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bbc-124">-DefaultProfile</span></span>
<span data-ttu-id="b7bbc-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7bbc-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="b7bbc-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="b7bbc-127">Intervallo di tempo per l'estrazione dei dati per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="b7bbc-128">Se personalizzato, deve essere specificato un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="b7bbc-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="b7bbc-129">-DefinitionType</span></span>
<span data-ttu-id="b7bbc-130">Tipo di esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-130">The type of the export.</span></span>
<span data-ttu-id="b7bbc-131">Tieni presente che "utilizzo" equivale a "ActualCost" ed è applicabile alle esportazioni che non contengono ancora dati per gli oneri o gli ammortamenti per le prenotazioni di servizi.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="b7bbc-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="b7bbc-132">-DestinationContainer</span></span>
<span data-ttu-id="b7bbc-133">Nome del contenitore in cui verranno caricati gli esportazioni.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="b7bbc-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b7bbc-134">-DestinationResourceId</span></span>
<span data-ttu-id="b7bbc-135">ID risorsa dell'account di archiviazione in cui verranno recapitate le esportazioni.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="b7bbc-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="b7bbc-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="b7bbc-137">Nome della directory in cui verranno caricati gli esportazioni.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="b7bbc-138">-Format</span><span class="sxs-lookup"><span data-stu-id="b7bbc-138">-Format</span></span>
<span data-ttu-id="b7bbc-139">Formato dell'esportazione da consegnare.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-139">The format of the export being delivered.</span></span>
<span data-ttu-id="b7bbc-140">Attualmente è supportato solo "CSV".</span><span class="sxs-lookup"><span data-stu-id="b7bbc-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="b7bbc-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7bbc-141">-Name</span></span>
<span data-ttu-id="b7bbc-142">Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-142">Export Name.</span></span>

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

### <span data-ttu-id="b7bbc-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="b7bbc-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="b7bbc-144">Data di inizio della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="b7bbc-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="b7bbc-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="b7bbc-146">Data di fine della ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="b7bbc-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="b7bbc-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="b7bbc-148">La ricorrenza della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="b7bbc-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="b7bbc-149">-ScheduleStatus</span></span>
<span data-ttu-id="b7bbc-150">Stato della pianificazione dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-150">The status of the export's schedule.</span></span>
<span data-ttu-id="b7bbc-151">Se "inattivo", la pianificazione dell'esportazione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="b7bbc-152">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b7bbc-152">-Scope</span></span>
<span data-ttu-id="b7bbc-153">Questo parametro definisce l'ambito di Costmanagement da diverse prospettive "abbonamento", "ResourceGroup" e "Fornisci servizio".</span><span class="sxs-lookup"><span data-stu-id="b7bbc-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="b7bbc-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="b7bbc-154">-TimePeriodFrom</span></span>
<span data-ttu-id="b7bbc-155">Data di inizio per l'esportazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-155">The start date for export data.</span></span>

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

### <span data-ttu-id="b7bbc-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="b7bbc-156">-TimePeriodTo</span></span>
<span data-ttu-id="b7bbc-157">Data di fine per l'esportazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-157">The end date for export data.</span></span>

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

### <span data-ttu-id="b7bbc-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7bbc-158">-Confirm</span></span>
<span data-ttu-id="b7bbc-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7bbc-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7bbc-160">-WhatIf</span></span>
<span data-ttu-id="b7bbc-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7bbc-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7bbc-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bbc-163">CommonParameters</span></span>
<span data-ttu-id="b7bbc-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bbc-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7bbc-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bbc-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7bbc-166">INPUTS</span></span>

## <span data-ttu-id="b7bbc-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7bbc-167">OUTPUTS</span></span>

### <span data-ttu-id="b7bbc-168">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="b7bbc-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="b7bbc-169">Note</span><span class="sxs-lookup"><span data-stu-id="b7bbc-169">NOTES</span></span>

<span data-ttu-id="b7bbc-170">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b7bbc-170">ALIASES</span></span>

## <span data-ttu-id="b7bbc-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7bbc-171">RELATED LINKS</span></span>

