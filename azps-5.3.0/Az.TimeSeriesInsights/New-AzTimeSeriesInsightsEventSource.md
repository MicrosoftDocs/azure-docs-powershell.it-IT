---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474817"
---
# <span data-ttu-id="72163-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="72163-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="72163-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72163-102">SYNOPSIS</span></span>
<span data-ttu-id="72163-103">Creare un'origine eventi nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="72163-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="72163-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72163-104">SYNTAX</span></span>

### <span data-ttu-id="72163-105">eventhub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72163-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72163-106">iothub</span><span class="sxs-lookup"><span data-stu-id="72163-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72163-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72163-107">DESCRIPTION</span></span>
<span data-ttu-id="72163-108">Creare un'origine eventi nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="72163-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="72163-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72163-109">EXAMPLES</span></span>

### <span data-ttu-id="72163-110">Esempio 1: creare un'origine eventi eventhub nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="72163-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="72163-111">Questo comando crea un'origine eventi eventhub nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="72163-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="72163-112">Esempio 2: creare un'origine eventi iothub nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="72163-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="72163-113">Questo comando crea un'origine eventi iothub nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="72163-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="72163-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72163-114">PARAMETERS</span></span>

### <span data-ttu-id="72163-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="72163-115">-ConsumerGroupName</span></span>
<span data-ttu-id="72163-116">Nome del gruppo di utenti dell'hub per l'evento/sacco che contiene le partizioni da cui verranno letti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="72163-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="72163-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72163-117">-DefaultProfile</span></span>
<span data-ttu-id="72163-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72163-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72163-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="72163-119">-EnvironmentName</span></span>
<span data-ttu-id="72163-120">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="72163-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="72163-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="72163-121">-EventHubName</span></span>
<span data-ttu-id="72163-122">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="72163-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72163-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="72163-123">-EventSourceResourceId</span></span>
<span data-ttu-id="72163-124">ID risorsa dell'origine eventi in Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="72163-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="72163-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="72163-125">-IoTHubName</span></span>
<span data-ttu-id="72163-126">Il nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="72163-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72163-127">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="72163-127">-KeyName</span></span>
<span data-ttu-id="72163-128">Nome della chiave SAS che concede l'accesso al servizio Insights Series per l'intervallo di tempo per l'hub eventi/disponibilità.</span><span class="sxs-lookup"><span data-stu-id="72163-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="72163-129">-Tipo</span><span class="sxs-lookup"><span data-stu-id="72163-129">-Kind</span></span>
<span data-ttu-id="72163-130">Tipo dell'origine dell'evento.</span><span class="sxs-lookup"><span data-stu-id="72163-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="72163-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="72163-131">-Location</span></span>
<span data-ttu-id="72163-132">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="72163-132">The location of the resource.</span></span>

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

### <span data-ttu-id="72163-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="72163-133">-Name</span></span>
<span data-ttu-id="72163-134">Nome dell'origine eventi.</span><span class="sxs-lookup"><span data-stu-id="72163-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72163-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72163-135">-ResourceGroupName</span></span>
<span data-ttu-id="72163-136">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="72163-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="72163-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="72163-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="72163-138">Nome del bus di servizio che contiene l'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="72163-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72163-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="72163-139">-SharedAccessKey</span></span>
<span data-ttu-id="72163-140">Il valore del tasto di scelta condiviso che concede al servizio Insights serie temporali l'accesso in lettura all'hub eventi/disponibilità.</span><span class="sxs-lookup"><span data-stu-id="72163-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72163-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72163-141">-SubscriptionId</span></span>
<span data-ttu-id="72163-142">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="72163-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="72163-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="72163-143">-Tag</span></span>
<span data-ttu-id="72163-144">Coppie chiave-valore di proprietà aggiuntive per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="72163-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="72163-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="72163-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="72163-146">Proprietà dell'evento che verrà usata come timestamp dell'origine eventi.</span><span class="sxs-lookup"><span data-stu-id="72163-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="72163-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72163-147">-Confirm</span></span>
<span data-ttu-id="72163-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72163-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72163-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72163-149">-WhatIf</span></span>
<span data-ttu-id="72163-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72163-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72163-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72163-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72163-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72163-152">CommonParameters</span></span>
<span data-ttu-id="72163-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72163-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72163-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72163-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72163-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72163-155">INPUTS</span></span>

## <span data-ttu-id="72163-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72163-156">OUTPUTS</span></span>

### <span data-ttu-id="72163-157">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="72163-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="72163-158">Note</span><span class="sxs-lookup"><span data-stu-id="72163-158">NOTES</span></span>

<span data-ttu-id="72163-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72163-159">ALIASES</span></span>

## <span data-ttu-id="72163-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72163-160">RELATED LINKS</span></span>

