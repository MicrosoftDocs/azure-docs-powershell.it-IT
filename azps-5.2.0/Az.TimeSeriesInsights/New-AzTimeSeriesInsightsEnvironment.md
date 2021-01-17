---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371486"
---
# <span data-ttu-id="363fc-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="363fc-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="363fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="363fc-102">SYNOPSIS</span></span>
<span data-ttu-id="363fc-103">Creare un ambiente nel gruppo di risorse e sottoscrizioni specificato.</span><span class="sxs-lookup"><span data-stu-id="363fc-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="363fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="363fc-104">SYNTAX</span></span>

### <span data-ttu-id="363fc-105">Gen1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="363fc-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="363fc-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="363fc-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="363fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="363fc-107">DESCRIPTION</span></span>
<span data-ttu-id="363fc-108">Creare un ambiente nel gruppo di risorse e sottoscrizioni specificato.</span><span class="sxs-lookup"><span data-stu-id="363fc-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="363fc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="363fc-109">EXAMPLES</span></span>

### <span data-ttu-id="363fc-110">Esempio 1: creare un ambiente per gli approfondimenti delle serie temporali di Gen1</span><span class="sxs-lookup"><span data-stu-id="363fc-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="363fc-111">Questo comando crea un ambiente per gli approfondimenti delle serie temporali di Gen1.</span><span class="sxs-lookup"><span data-stu-id="363fc-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="363fc-112">Esempio 2: creare un ambiente per gli approfondimenti delle serie temporali di Gen2</span><span class="sxs-lookup"><span data-stu-id="363fc-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="363fc-113">Questo comando crea un ambiente per gli approfondimenti delle serie temporali di Gen2.</span><span class="sxs-lookup"><span data-stu-id="363fc-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="363fc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="363fc-114">PARAMETERS</span></span>

### <span data-ttu-id="363fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="363fc-115">-AsJob</span></span>
<span data-ttu-id="363fc-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="363fc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="363fc-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="363fc-117">-Capacity</span></span>
<span data-ttu-id="363fc-118">Capacità dell'USK.</span><span class="sxs-lookup"><span data-stu-id="363fc-118">The capacity of the sku.</span></span>
<span data-ttu-id="363fc-119">Per gli ambienti Gen1, questo valore può essere modificato per supportare la scalabilità fuori dagli ambienti dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="363fc-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="363fc-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="363fc-120">-DataRetentionTime</span></span>
<span data-ttu-id="363fc-121">Periodo di conservazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="363fc-121">The data retention time.</span></span>

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

### <span data-ttu-id="363fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363fc-122">-DefaultProfile</span></span>
<span data-ttu-id="363fc-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="363fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="363fc-124">-Tipo</span><span class="sxs-lookup"><span data-stu-id="363fc-124">-Kind</span></span>
<span data-ttu-id="363fc-125">Il tipo di ambiente.</span><span class="sxs-lookup"><span data-stu-id="363fc-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="363fc-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="363fc-126">-Location</span></span>
<span data-ttu-id="363fc-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="363fc-127">The location of the resource.</span></span>

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

### <span data-ttu-id="363fc-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="363fc-128">-Name</span></span>
<span data-ttu-id="363fc-129">Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="363fc-129">Name of the environment</span></span>

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

### <span data-ttu-id="363fc-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="363fc-130">-NoWait</span></span>
<span data-ttu-id="363fc-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="363fc-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="363fc-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="363fc-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="363fc-133">Elenco delle proprietà dell'evento che verranno usate per partizionare i dati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="363fc-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="363fc-134">Per costruire, vedere la sezione Note per le proprietà di PARTITIONKEYPROPERTY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="363fc-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="363fc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="363fc-135">-ResourceGroupName</span></span>
<span data-ttu-id="363fc-136">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="363fc-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="363fc-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="363fc-137">-Sku</span></span>
<span data-ttu-id="363fc-138">Il nome di questo SKU.</span><span class="sxs-lookup"><span data-stu-id="363fc-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="363fc-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="363fc-139">-StorageAccountKey</span></span>
<span data-ttu-id="363fc-140">Il valore della chiave di gestione che concede l'accesso in scrittura del servizio Insights serie temporali all'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="363fc-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="363fc-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="363fc-141">-StorageAccountName</span></span>
<span data-ttu-id="363fc-142">Nome dell'account di archiviazione che conterrà i dati a lungo termine dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="363fc-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="363fc-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="363fc-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="363fc-144">Comportamento che il servizio approfondimenti della serie temporale deve eseguire quando la capacità dell'ambiente è stata superata</span><span class="sxs-lookup"><span data-stu-id="363fc-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="363fc-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="363fc-145">-SubscriptionId</span></span>
<span data-ttu-id="363fc-146">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="363fc-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="363fc-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="363fc-147">-Tag</span></span>
<span data-ttu-id="363fc-148">Coppie chiave-valore di proprietà aggiuntive per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="363fc-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="363fc-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="363fc-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="363fc-150">L'elenco delle proprietà dell'evento che verranno usate per definire l'ID della serie temporali dell'ambiente. Per costruire, vedere la sezione Note per le proprietà di TIMESERIESIDPROPERTY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="363fc-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="363fc-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="363fc-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="363fc-152">ISO8601 TimeSpan che specifica il numero di giorni in cui gli eventi dell'ambiente saranno disponibili per la query dall'archivio caldo.</span><span class="sxs-lookup"><span data-stu-id="363fc-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="363fc-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="363fc-153">-Confirm</span></span>
<span data-ttu-id="363fc-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="363fc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="363fc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="363fc-155">-WhatIf</span></span>
<span data-ttu-id="363fc-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363fc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="363fc-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363fc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="363fc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363fc-158">CommonParameters</span></span>
<span data-ttu-id="363fc-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="363fc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363fc-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="363fc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363fc-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="363fc-161">INPUTS</span></span>

## <span data-ttu-id="363fc-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="363fc-162">OUTPUTS</span></span>

### <span data-ttu-id="363fc-163">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="363fc-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="363fc-164">Note</span><span class="sxs-lookup"><span data-stu-id="363fc-164">NOTES</span></span>

<span data-ttu-id="363fc-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="363fc-165">ALIASES</span></span>

<span data-ttu-id="363fc-166">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="363fc-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="363fc-167">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="363fc-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="363fc-168">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="363fc-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="363fc-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: elenco delle proprietà dell'evento che verranno usate per partizionare i dati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="363fc-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="363fc-170">`[Name <String>]`: Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="363fc-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="363fc-171">`[Type <PropertyType?>]`: Il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="363fc-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="363fc-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: l'elenco delle proprietà dell'evento che verranno usate per definire l'ID della serie temporale dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="363fc-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="363fc-173">`[Name <String>]`: Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="363fc-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="363fc-174">`[Type <PropertyType?>]`: Il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="363fc-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="363fc-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="363fc-175">RELATED LINKS</span></span>

