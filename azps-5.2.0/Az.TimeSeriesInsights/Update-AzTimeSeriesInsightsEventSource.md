---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345691"
---
# <span data-ttu-id="ee2fe-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="ee2fe-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="ee2fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2fe-103">Aggiorna l'origine eventi con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="ee2fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-104">SYNTAX</span></span>

### <span data-ttu-id="ee2fe-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee2fe-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ee2fe-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ee2fe-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee2fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee2fe-107">DESCRIPTION</span></span>
<span data-ttu-id="ee2fe-108">Aggiorna l'origine eventi con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="ee2fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-109">EXAMPLES</span></span>

### <span data-ttu-id="ee2fe-110">Esempio 1: aggiornare un'origine eventi specificata per nome</span><span class="sxs-lookup"><span data-stu-id="ee2fe-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="ee2fe-111">Questo comando aggiorna una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="ee2fe-112">Esempio 3: aggiornare un'origine eventi specificata per oggetto</span><span class="sxs-lookup"><span data-stu-id="ee2fe-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="ee2fe-113">Questo comando aggiorna una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="ee2fe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-114">PARAMETERS</span></span>

### <span data-ttu-id="ee2fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2fe-115">-DefaultProfile</span></span>
<span data-ttu-id="ee2fe-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2fe-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ee2fe-117">-EnvironmentName</span></span>
<span data-ttu-id="ee2fe-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ee2fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee2fe-119">-InputObject</span></span>
<span data-ttu-id="ee2fe-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee2fe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee2fe-121">-Name</span></span>
<span data-ttu-id="ee2fe-122">Nome dell'origine dell'evento Insights Series associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee2fe-124">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ee2fe-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee2fe-125">-SubscriptionId</span></span>
<span data-ttu-id="ee2fe-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ee2fe-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee2fe-127">-Tag</span></span>
<span data-ttu-id="ee2fe-128">Coppie chiave-valore di proprietà aggiuntive per l'origine eventi.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="ee2fe-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee2fe-129">-Confirm</span></span>
<span data-ttu-id="ee2fe-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2fe-131">-WhatIf</span></span>
<span data-ttu-id="ee2fe-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2fe-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2fe-134">CommonParameters</span></span>
<span data-ttu-id="ee2fe-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2fe-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee2fe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2fe-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-137">INPUTS</span></span>

### <span data-ttu-id="ee2fe-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="ee2fe-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ee2fe-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee2fe-139">OUTPUTS</span></span>

### <span data-ttu-id="ee2fe-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="ee2fe-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="ee2fe-141">Note</span><span class="sxs-lookup"><span data-stu-id="ee2fe-141">NOTES</span></span>

<span data-ttu-id="ee2fe-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ee2fe-142">ALIASES</span></span>

<span data-ttu-id="ee2fe-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee2fe-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee2fe-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee2fe-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ee2fe-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee2fe-147">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ee2fe-148">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="ee2fe-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ee2fe-149">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ee2fe-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ee2fe-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee2fe-151">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ee2fe-152">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ee2fe-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2fe-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ee2fe-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee2fe-154">RELATED LINKS</span></span>

