---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 86e143455f287bef8bff4b391f7f40aa01fba99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987432"
---
# <span data-ttu-id="6d310-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="6d310-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="6d310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d310-102">SYNOPSIS</span></span>
<span data-ttu-id="6d310-103">Aggiorna l'ambiente con il nome specificato nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="6d310-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6d310-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d310-104">SYNTAX</span></span>

### <span data-ttu-id="6d310-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d310-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d310-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d310-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d310-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d310-107">DESCRIPTION</span></span>
<span data-ttu-id="6d310-108">Aggiorna l'ambiente con il nome specificato nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="6d310-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6d310-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d310-109">EXAMPLES</span></span>

### <span data-ttu-id="6d310-110">Esempio 1: Aggiornare un ambiente approfondimenti serie temporale Gen1</span><span class="sxs-lookup"><span data-stu-id="6d310-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="6d310-111">Questo comando aggiorna un ambiente approfondimenti serie temporale gen1.</span><span class="sxs-lookup"><span data-stu-id="6d310-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="6d310-112">Esempio 2: Aggiornare un ambiente approfondimenti serie temporale Gen1</span><span class="sxs-lookup"><span data-stu-id="6d310-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="6d310-113">Questo comando aggiorna un ambiente approfondimenti serie temporale gen1.</span><span class="sxs-lookup"><span data-stu-id="6d310-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="6d310-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d310-114">PARAMETERS</span></span>

### <span data-ttu-id="6d310-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d310-115">-AsJob</span></span>
<span data-ttu-id="6d310-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6d310-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d310-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d310-117">-DefaultProfile</span></span>
<span data-ttu-id="6d310-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d310-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d310-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d310-119">-InputObject</span></span>
<span data-ttu-id="6d310-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6d310-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d310-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d310-121">-Name</span></span>
<span data-ttu-id="6d310-122">Nome dell'ambiente Approfondimenti serie temporale associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6d310-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6d310-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d310-123">-NoWait</span></span>
<span data-ttu-id="6d310-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6d310-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d310-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d310-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d310-126">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d310-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6d310-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d310-127">-SubscriptionId</span></span>
<span data-ttu-id="6d310-128">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="6d310-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6d310-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d310-129">-Tag</span></span>
<span data-ttu-id="6d310-130">Coppie chiave-valore di proprietà aggiuntive per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6d310-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="6d310-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d310-131">-Confirm</span></span>
<span data-ttu-id="6d310-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d310-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d310-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d310-133">-WhatIf</span></span>
<span data-ttu-id="6d310-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d310-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d310-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d310-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d310-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d310-136">CommonParameters</span></span>
<span data-ttu-id="6d310-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d310-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d310-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d310-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d310-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d310-139">INPUTS</span></span>

### <span data-ttu-id="6d310-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6d310-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6d310-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d310-141">OUTPUTS</span></span>

### <span data-ttu-id="6d310-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="6d310-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="6d310-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d310-143">NOTES</span></span>

<span data-ttu-id="6d310-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d310-144">ALIASES</span></span>

<span data-ttu-id="6d310-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6d310-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d310-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6d310-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d310-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d310-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d310-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6d310-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d310-149">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="6d310-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6d310-150">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="6d310-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6d310-151">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6d310-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6d310-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6d310-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d310-153">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6d310-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6d310-154">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d310-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6d310-155">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="6d310-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6d310-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d310-156">RELATED LINKS</span></span>

