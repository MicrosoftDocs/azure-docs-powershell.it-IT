---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383039"
---
# <span data-ttu-id="53cb9-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="53cb9-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="53cb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="53cb9-103">Aggiorna l'ambiente con il nome specificato nel gruppo di risorse e dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="53cb9-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="53cb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53cb9-104">SYNTAX</span></span>

### <span data-ttu-id="53cb9-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53cb9-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53cb9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53cb9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53cb9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53cb9-107">DESCRIPTION</span></span>
<span data-ttu-id="53cb9-108">Aggiorna l'ambiente con il nome specificato nel gruppo di risorse e dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="53cb9-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="53cb9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="53cb9-110">Esempio 1: aggiornare un ambiente per gli approfondimenti delle serie temporali di Gen1</span><span class="sxs-lookup"><span data-stu-id="53cb9-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="53cb9-111">Questo comando aggiorna un ambiente per gli approfondimenti delle serie temporali di Gen1.</span><span class="sxs-lookup"><span data-stu-id="53cb9-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="53cb9-112">Esempio 2: aggiornare un ambiente per gli approfondimenti delle serie temporali di Gen1</span><span class="sxs-lookup"><span data-stu-id="53cb9-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="53cb9-113">Questo comando aggiorna un ambiente per gli approfondimenti delle serie temporali di Gen1.</span><span class="sxs-lookup"><span data-stu-id="53cb9-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="53cb9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53cb9-114">PARAMETERS</span></span>

### <span data-ttu-id="53cb9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53cb9-115">-AsJob</span></span>
<span data-ttu-id="53cb9-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="53cb9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="53cb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53cb9-117">-DefaultProfile</span></span>
<span data-ttu-id="53cb9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53cb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53cb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53cb9-119">-InputObject</span></span>
<span data-ttu-id="53cb9-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="53cb9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53cb9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="53cb9-121">-Name</span></span>
<span data-ttu-id="53cb9-122">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="53cb9-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53cb9-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="53cb9-123">-NoWait</span></span>
<span data-ttu-id="53cb9-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="53cb9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53cb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53cb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="53cb9-126">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="53cb9-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="53cb9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53cb9-127">-SubscriptionId</span></span>
<span data-ttu-id="53cb9-128">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="53cb9-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53cb9-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="53cb9-129">-Tag</span></span>
<span data-ttu-id="53cb9-130">Coppie chiave-valore di proprietà aggiuntive per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="53cb9-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="53cb9-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53cb9-131">-Confirm</span></span>
<span data-ttu-id="53cb9-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53cb9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53cb9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53cb9-133">-WhatIf</span></span>
<span data-ttu-id="53cb9-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53cb9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53cb9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53cb9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53cb9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cb9-136">CommonParameters</span></span>
<span data-ttu-id="53cb9-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53cb9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cb9-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53cb9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cb9-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53cb9-139">INPUTS</span></span>

### <span data-ttu-id="53cb9-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="53cb9-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="53cb9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53cb9-141">OUTPUTS</span></span>

### <span data-ttu-id="53cb9-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="53cb9-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="53cb9-143">Note</span><span class="sxs-lookup"><span data-stu-id="53cb9-143">NOTES</span></span>

<span data-ttu-id="53cb9-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="53cb9-144">ALIASES</span></span>

<span data-ttu-id="53cb9-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53cb9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53cb9-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="53cb9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53cb9-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53cb9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53cb9-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="53cb9-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53cb9-149">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="53cb9-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="53cb9-150">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="53cb9-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="53cb9-151">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="53cb9-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="53cb9-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="53cb9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53cb9-153">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="53cb9-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="53cb9-154">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="53cb9-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="53cb9-155">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="53cb9-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="53cb9-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53cb9-156">RELATED LINKS</span></span>

