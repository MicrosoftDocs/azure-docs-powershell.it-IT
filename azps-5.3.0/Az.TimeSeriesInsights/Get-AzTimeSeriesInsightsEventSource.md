---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380869"
---
# <span data-ttu-id="cd865-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="cd865-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="cd865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd865-102">SYNOPSIS</span></span>
<span data-ttu-id="cd865-103">Ottiene l'origine eventi con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cd865-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="cd865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd865-104">SYNTAX</span></span>

### <span data-ttu-id="cd865-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd865-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd865-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cd865-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd865-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd865-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd865-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd865-108">DESCRIPTION</span></span>
<span data-ttu-id="cd865-109">Ottiene l'origine eventi con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cd865-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="cd865-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd865-110">EXAMPLES</span></span>

### <span data-ttu-id="cd865-111">Esempio 1: elencare tutte le origini eventi nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="cd865-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="cd865-112">Questo comando elenca tutte le origini eventi in ambienti specificati.</span><span class="sxs-lookup"><span data-stu-id="cd865-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="cd865-113">Esempio 2: ottenere un'origine eventi specificata per nome</span><span class="sxs-lookup"><span data-stu-id="cd865-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="cd865-114">Questo comando ottiene una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="cd865-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="cd865-115">Esempio 3: ottenere un'origine eventi specificata per oggetto</span><span class="sxs-lookup"><span data-stu-id="cd865-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="cd865-116">Questo comando ottiene una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="cd865-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="cd865-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd865-117">PARAMETERS</span></span>

### <span data-ttu-id="cd865-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd865-118">-DefaultProfile</span></span>
<span data-ttu-id="cd865-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd865-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd865-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="cd865-120">-EnvironmentName</span></span>
<span data-ttu-id="cd865-121">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="cd865-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="cd865-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd865-122">-InputObject</span></span>
<span data-ttu-id="cd865-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd865-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd865-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd865-124">-Name</span></span>
<span data-ttu-id="cd865-125">Nome dell'origine dell'evento Insights Series associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cd865-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd865-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd865-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd865-127">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="cd865-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="cd865-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd865-128">-SubscriptionId</span></span>
<span data-ttu-id="cd865-129">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd865-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd865-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd865-130">CommonParameters</span></span>
<span data-ttu-id="cd865-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd865-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd865-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd865-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd865-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd865-133">INPUTS</span></span>

### <span data-ttu-id="cd865-134">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="cd865-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="cd865-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd865-135">OUTPUTS</span></span>

### <span data-ttu-id="cd865-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="cd865-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="cd865-137">Note</span><span class="sxs-lookup"><span data-stu-id="cd865-137">NOTES</span></span>

<span data-ttu-id="cd865-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd865-138">ALIASES</span></span>

<span data-ttu-id="cd865-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd865-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd865-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cd865-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd865-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd865-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd865-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cd865-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd865-143">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="cd865-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="cd865-144">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="cd865-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="cd865-145">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cd865-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="cd865-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cd865-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd865-147">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="cd865-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="cd865-148">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="cd865-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="cd865-149">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="cd865-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cd865-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd865-150">RELATED LINKS</span></span>

