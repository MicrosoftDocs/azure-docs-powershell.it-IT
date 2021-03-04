---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955053"
---
# <span data-ttu-id="1306e-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="1306e-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="1306e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1306e-102">SYNOPSIS</span></span>
<span data-ttu-id="1306e-103">Creare un ambiente nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="1306e-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="1306e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1306e-104">SYNTAX</span></span>

### <span data-ttu-id="1306e-105">Gen1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1306e-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1306e-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="1306e-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1306e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1306e-107">DESCRIPTION</span></span>
<span data-ttu-id="1306e-108">Creare un ambiente nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="1306e-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="1306e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1306e-109">EXAMPLES</span></span>

### <span data-ttu-id="1306e-110">Esempio 1: Creare un ambiente approfondimenti serie temporale Gen1</span><span class="sxs-lookup"><span data-stu-id="1306e-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="1306e-111">Questo comando crea un ambiente approfondimenti serie temporale Gen1.</span><span class="sxs-lookup"><span data-stu-id="1306e-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="1306e-112">Esempio 2: Creare un ambiente approfondimenti serie temporale Gen2</span><span class="sxs-lookup"><span data-stu-id="1306e-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="1306e-113">Questo comando crea un ambiente approfondimenti serie temporale Gen2.</span><span class="sxs-lookup"><span data-stu-id="1306e-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="1306e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1306e-114">PARAMETERS</span></span>

### <span data-ttu-id="1306e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1306e-115">-AsJob</span></span>
<span data-ttu-id="1306e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1306e-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="1306e-117">-Capacity</span></span>
<span data-ttu-id="1306e-118">Capacità della SKU.</span><span class="sxs-lookup"><span data-stu-id="1306e-118">The capacity of the sku.</span></span>
<span data-ttu-id="1306e-119">Per gli ambienti gen1, questo valore può essere modificato per supportare la scalabilità orizzontale degli ambienti dopo la loro creazione.</span><span class="sxs-lookup"><span data-stu-id="1306e-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="1306e-120">-DataRetentionTime</span></span>
<span data-ttu-id="1306e-121">Il tempo di conservazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1306e-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1306e-122">-DefaultProfile</span></span>
<span data-ttu-id="1306e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1306e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1306e-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="1306e-124">-Kind</span></span>
<span data-ttu-id="1306e-125">Tipo di ambiente.</span><span class="sxs-lookup"><span data-stu-id="1306e-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-126">-Location</span><span class="sxs-lookup"><span data-stu-id="1306e-126">-Location</span></span>
<span data-ttu-id="1306e-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1306e-127">The location of the resource.</span></span>

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

### <span data-ttu-id="1306e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1306e-128">-Name</span></span>
<span data-ttu-id="1306e-129">Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="1306e-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1306e-130">-NoWait</span></span>
<span data-ttu-id="1306e-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1306e-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="1306e-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="1306e-133">Elenco delle proprietà evento che verranno usate per partizionare i dati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="1306e-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="1306e-134">Per creare, vedere la sezione NOTE per le proprietà PARTITIONKEYPROPERTY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1306e-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1306e-135">-ResourceGroupName</span></span>
<span data-ttu-id="1306e-136">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1306e-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1306e-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="1306e-137">-Sku</span></span>
<span data-ttu-id="1306e-138">Nome di questo SKU.</span><span class="sxs-lookup"><span data-stu-id="1306e-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1306e-139">-StorageAccountKey</span></span>
<span data-ttu-id="1306e-140">Valore della chiave di gestione che concede al servizio Time Series Insights l'accesso in scrittura all'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1306e-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1306e-141">-StorageAccountName</span></span>
<span data-ttu-id="1306e-142">Nome dell'account di archiviazione che contenerà i dati a lungo termine dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="1306e-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="1306e-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="1306e-144">Il comportamento che il servizio Time Series Insights dovrebbe adottare quando la capacità dell'ambiente è stata superata</span><span class="sxs-lookup"><span data-stu-id="1306e-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1306e-145">-SubscriptionId</span></span>
<span data-ttu-id="1306e-146">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="1306e-146">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="1306e-147">-Tag</span></span>
<span data-ttu-id="1306e-148">Coppie chiave-valore di proprietà aggiuntive per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1306e-148">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="1306e-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="1306e-150">Elenco delle proprietà evento che verranno usate per definire l'ID serie temporale dell'ambiente. Per creare, vedere la sezione NOTES per le proprietà TIMESERIESIDPROPERTY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1306e-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="1306e-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="1306e-152">Intervallo di tempo ISO8601 che specifica il numero di giorni per cui gli eventi dell'ambiente saranno disponibili per la query dal warm store.</span><span class="sxs-lookup"><span data-stu-id="1306e-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1306e-153">-Confirm</span></span>
<span data-ttu-id="1306e-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1306e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1306e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1306e-155">-WhatIf</span></span>
<span data-ttu-id="1306e-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1306e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1306e-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1306e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1306e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1306e-158">CommonParameters</span></span>
<span data-ttu-id="1306e-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1306e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1306e-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1306e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1306e-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="1306e-161">INPUTS</span></span>

## <span data-ttu-id="1306e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1306e-162">OUTPUTS</span></span>

### <span data-ttu-id="1306e-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="1306e-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="1306e-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="1306e-164">NOTES</span></span>

<span data-ttu-id="1306e-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1306e-165">ALIASES</span></span>

<span data-ttu-id="1306e-166">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1306e-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1306e-167">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1306e-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1306e-168">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1306e-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1306e-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: elenco delle proprietà evento che verranno usate per partizionare i dati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="1306e-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="1306e-170">`[Name <String>]`: nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1306e-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="1306e-171">`[Type <PropertyType?>]`: tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1306e-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="1306e-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: elenco delle proprietà evento che verranno usate per definire l'ID serie temporale dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="1306e-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="1306e-173">`[Name <String>]`: nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1306e-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="1306e-174">`[Type <PropertyType?>]`: tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1306e-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="1306e-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1306e-175">RELATED LINKS</span></span>

