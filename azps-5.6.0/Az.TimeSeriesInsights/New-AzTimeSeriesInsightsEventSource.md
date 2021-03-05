---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995845"
---
# <span data-ttu-id="eca89-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="eca89-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="eca89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca89-102">SYNOPSIS</span></span>
<span data-ttu-id="eca89-103">Creare un'origine evento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="eca89-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="eca89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eca89-104">SYNTAX</span></span>

### <span data-ttu-id="eca89-105">eventhub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eca89-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eca89-106">iothub</span><span class="sxs-lookup"><span data-stu-id="eca89-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eca89-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eca89-107">DESCRIPTION</span></span>
<span data-ttu-id="eca89-108">Creare un'origine evento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="eca89-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="eca89-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eca89-109">EXAMPLES</span></span>

### <span data-ttu-id="eca89-110">Esempio 1: Creare un'origine evento eventhub nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="eca89-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="eca89-111">Questo comando crea un'origine evento eventhub nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="eca89-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="eca89-112">Esempio 2: Creare un'origine evento iothub nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="eca89-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="eca89-113">Questo comando crea un'origine evento iothub nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="eca89-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="eca89-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eca89-114">PARAMETERS</span></span>

### <span data-ttu-id="eca89-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="eca89-115">-ConsumerGroupName</span></span>
<span data-ttu-id="eca89-116">Nome del gruppo consumer dell'hub evento/iot che contiene le partizioni da cui verranno letti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="eca89-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="eca89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca89-117">-DefaultProfile</span></span>
<span data-ttu-id="eca89-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eca89-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca89-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="eca89-119">-EnvironmentName</span></span>
<span data-ttu-id="eca89-120">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="eca89-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="eca89-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="eca89-121">-EventHubName</span></span>
<span data-ttu-id="eca89-122">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="eca89-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="eca89-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="eca89-123">-EventSourceResourceId</span></span>
<span data-ttu-id="eca89-124">ID risorsa dell'origine evento in Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="eca89-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="eca89-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="eca89-125">-IoTHubName</span></span>
<span data-ttu-id="eca89-126">Nome dell'hub iot.</span><span class="sxs-lookup"><span data-stu-id="eca89-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="eca89-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eca89-127">-KeyName</span></span>
<span data-ttu-id="eca89-128">Nome della chiave di firma di accesso condiviso che concede al servizio Time Series Insights l'accesso all'hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="eca89-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="eca89-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="eca89-129">-Kind</span></span>
<span data-ttu-id="eca89-130">Il tipo di origine dell'evento.</span><span class="sxs-lookup"><span data-stu-id="eca89-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="eca89-131">-Location</span><span class="sxs-lookup"><span data-stu-id="eca89-131">-Location</span></span>
<span data-ttu-id="eca89-132">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eca89-132">The location of the resource.</span></span>

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

### <span data-ttu-id="eca89-133">-Name</span><span class="sxs-lookup"><span data-stu-id="eca89-133">-Name</span></span>
<span data-ttu-id="eca89-134">Nome dell'origine dell'evento.</span><span class="sxs-lookup"><span data-stu-id="eca89-134">Name of the event source.</span></span>

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

### <span data-ttu-id="eca89-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca89-135">-ResourceGroupName</span></span>
<span data-ttu-id="eca89-136">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="eca89-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="eca89-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="eca89-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="eca89-138">Nome del bus di servizio che contiene l'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="eca89-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="eca89-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="eca89-139">-SharedAccessKey</span></span>
<span data-ttu-id="eca89-140">Valore della chiave di accesso condivisa che concede al servizio Time Series Insights l'accesso in lettura all'hub evento/iot.</span><span class="sxs-lookup"><span data-stu-id="eca89-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="eca89-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eca89-141">-SubscriptionId</span></span>
<span data-ttu-id="eca89-142">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="eca89-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="eca89-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="eca89-143">-Tag</span></span>
<span data-ttu-id="eca89-144">Coppie chiave-valore di proprietà aggiuntive per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="eca89-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="eca89-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="eca89-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="eca89-146">Proprietà evento che verrà usata come timestamp dell'origine evento.</span><span class="sxs-lookup"><span data-stu-id="eca89-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="eca89-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eca89-147">-Confirm</span></span>
<span data-ttu-id="eca89-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca89-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca89-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca89-149">-WhatIf</span></span>
<span data-ttu-id="eca89-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eca89-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca89-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eca89-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca89-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca89-152">CommonParameters</span></span>
<span data-ttu-id="eca89-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca89-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca89-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eca89-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca89-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="eca89-155">INPUTS</span></span>

## <span data-ttu-id="eca89-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eca89-156">OUTPUTS</span></span>

### <span data-ttu-id="eca89-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="eca89-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="eca89-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="eca89-158">NOTES</span></span>

<span data-ttu-id="eca89-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eca89-159">ALIASES</span></span>

## <span data-ttu-id="eca89-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eca89-160">RELATED LINKS</span></span>

