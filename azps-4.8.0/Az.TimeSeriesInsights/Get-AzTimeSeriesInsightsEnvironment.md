---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192631"
---
# <span data-ttu-id="cc6ce-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="cc6ce-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="cc6ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6ce-103">Ottiene l'ambiente con il nome specificato nel gruppo di risorse e dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="cc6ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-104">SYNTAX</span></span>

### <span data-ttu-id="cc6ce-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc6ce-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc6ce-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cc6ce-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc6ce-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc6ce-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc6ce-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="cc6ce-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cc6ce-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc6ce-109">DESCRIPTION</span></span>
<span data-ttu-id="cc6ce-110">Ottiene l'ambiente con il nome specificato nel gruppo di risorse e dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="cc6ce-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-111">EXAMPLES</span></span>

### <span data-ttu-id="cc6ce-112">Esempio 1: ottenere un ambiente Insights serie temporali</span><span class="sxs-lookup"><span data-stu-id="cc6ce-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="cc6ce-113">Questo comando ottiene un ambiente Insights serie temporali.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="cc6ce-114">Esempio 2: elencare tutti gli ambienti Insights serie temporali</span><span class="sxs-lookup"><span data-stu-id="cc6ce-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="cc6ce-115">Questo comando elenca tutti gli ambienti Insights serie temporali in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="cc6ce-116">Esempio 3: ottenere un ambiente per gli approfondimenti delle serie temporali per oggetto</span><span class="sxs-lookup"><span data-stu-id="cc6ce-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="cc6ce-117">Questo comando ottiene gli ambienti Insights di serie temporali.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="cc6ce-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-118">PARAMETERS</span></span>

### <span data-ttu-id="cc6ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6ce-119">-DefaultProfile</span></span>
<span data-ttu-id="cc6ce-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6ce-121">-Espandi</span><span class="sxs-lookup"><span data-stu-id="cc6ce-121">-Expand</span></span>
<span data-ttu-id="cc6ce-122">L'impostazione $expand = stato includerà lo stato dei servizi interni dell'ambiente nel servizio approfondimenti serie temporali.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc6ce-123">-InputObject</span></span>
<span data-ttu-id="cc6ce-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6ce-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc6ce-125">-Name</span></span>
<span data-ttu-id="cc6ce-126">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc6ce-128">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6ce-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc6ce-129">-SubscriptionId</span></span>
<span data-ttu-id="cc6ce-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6ce-131">CommonParameters</span></span>
<span data-ttu-id="cc6ce-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6ce-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc6ce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6ce-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-134">INPUTS</span></span>

### <span data-ttu-id="cc6ce-135">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="cc6ce-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="cc6ce-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc6ce-136">OUTPUTS</span></span>

### <span data-ttu-id="cc6ce-137">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="cc6ce-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="cc6ce-138">Note</span><span class="sxs-lookup"><span data-stu-id="cc6ce-138">NOTES</span></span>

<span data-ttu-id="cc6ce-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc6ce-139">ALIASES</span></span>

<span data-ttu-id="cc6ce-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc6ce-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc6ce-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc6ce-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cc6ce-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc6ce-144">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="cc6ce-145">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="cc6ce-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="cc6ce-146">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="cc6ce-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cc6ce-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc6ce-148">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="cc6ce-149">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="cc6ce-150">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6ce-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cc6ce-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc6ce-151">RELATED LINKS</span></span>

