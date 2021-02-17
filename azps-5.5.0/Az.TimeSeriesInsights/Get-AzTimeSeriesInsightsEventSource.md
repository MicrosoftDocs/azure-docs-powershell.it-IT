---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198326"
---
# <span data-ttu-id="3185b-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="3185b-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="3185b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3185b-102">SYNOPSIS</span></span>
<span data-ttu-id="3185b-103">Ottiene l'origine evento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="3185b-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3185b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3185b-104">SYNTAX</span></span>

### <span data-ttu-id="3185b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3185b-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3185b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3185b-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3185b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3185b-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3185b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3185b-108">DESCRIPTION</span></span>
<span data-ttu-id="3185b-109">Ottiene l'origine evento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="3185b-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3185b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3185b-110">EXAMPLES</span></span>

### <span data-ttu-id="3185b-111">Esempio 1: Elencare tutte le origini evento nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="3185b-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="3185b-112">Questo comando elenca tutte le origini evento negli ambienti specificati.</span><span class="sxs-lookup"><span data-stu-id="3185b-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="3185b-113">Esempio 2: Ottenere un'origine evento specificata in base al nome</span><span class="sxs-lookup"><span data-stu-id="3185b-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="3185b-114">Questo comando ottiene un'origine evento specifica.</span><span class="sxs-lookup"><span data-stu-id="3185b-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="3185b-115">Esempio 3: Ottenere un'origine evento specificata in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="3185b-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="3185b-116">Questo comando ottiene un'origine evento specifica.</span><span class="sxs-lookup"><span data-stu-id="3185b-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="3185b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3185b-117">PARAMETERS</span></span>

### <span data-ttu-id="3185b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3185b-118">-DefaultProfile</span></span>
<span data-ttu-id="3185b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3185b-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="3185b-120">-EnvironmentName</span></span>
<span data-ttu-id="3185b-121">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3185b-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="3185b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3185b-122">-InputObject</span></span>
<span data-ttu-id="3185b-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3185b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3185b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3185b-124">-Name</span></span>
<span data-ttu-id="3185b-125">Nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="3185b-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="3185b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3185b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3185b-127">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3185b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3185b-128">-SubscriptionId</span></span>
<span data-ttu-id="3185b-129">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3185b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3185b-130">CommonParameters</span></span>
<span data-ttu-id="3185b-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3185b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3185b-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3185b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3185b-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3185b-133">INPUTS</span></span>

### <span data-ttu-id="3185b-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="3185b-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="3185b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3185b-135">OUTPUTS</span></span>

### <span data-ttu-id="3185b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="3185b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="3185b-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="3185b-137">NOTES</span></span>

<span data-ttu-id="3185b-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3185b-138">ALIASES</span></span>

<span data-ttu-id="3185b-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3185b-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3185b-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3185b-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3185b-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3185b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3185b-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="3185b-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3185b-143">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="3185b-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="3185b-144">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="3185b-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="3185b-145">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="3185b-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="3185b-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3185b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3185b-147">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="3185b-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="3185b-148">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="3185b-149">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="3185b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3185b-150">RELATED LINKS</span></span>

