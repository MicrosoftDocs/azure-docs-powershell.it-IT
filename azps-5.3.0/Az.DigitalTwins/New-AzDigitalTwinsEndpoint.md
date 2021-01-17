---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473947"
---
# <span data-ttu-id="96896-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="96896-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="96896-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96896-102">SYNOPSIS</span></span>
<span data-ttu-id="96896-103">Creare o aggiornare l'endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="96896-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96896-104">SYNTAX</span></span>

### <span data-ttu-id="96896-105">EventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96896-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96896-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="96896-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96896-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96896-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96896-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96896-108">DESCRIPTION</span></span>
<span data-ttu-id="96896-109">Creare o aggiornare l'endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="96896-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96896-110">EXAMPLES</span></span>

### <span data-ttu-id="96896-111">Esempio 1: creare un AzDigitalTwinsEndpoint per Eventhub</span><span class="sxs-lookup"><span data-stu-id="96896-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96896-112">Creare un AzDigitalTwinsEndpoint per Eventhub da connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="96896-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="96896-113">Esempio 2: creare un AzDigitalTwinsEndpoint per EventGrid</span><span class="sxs-lookup"><span data-stu-id="96896-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96896-114">Creare un AzDigitalTwinsEndpoint per Eventhub da TopicEndpoint e accessKey1</span><span class="sxs-lookup"><span data-stu-id="96896-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="96896-115">Esempio 3: creare un AzDigitalTwinsEndpoint per ServiceBus</span><span class="sxs-lookup"><span data-stu-id="96896-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="96896-116">Creare un AzDigitalTwinsEndpoint per ServicBus da PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="96896-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="96896-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96896-117">PARAMETERS</span></span>

### <span data-ttu-id="96896-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="96896-118">-AccessKey1</span></span>
<span data-ttu-id="96896-119">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96896-120">-AsJob</span></span>
<span data-ttu-id="96896-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="96896-121">Run the command as a job</span></span>

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

### <span data-ttu-id="96896-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="96896-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="96896-123">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="96896-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="96896-125">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="96896-126">-DeadLetterSecret</span></span>
<span data-ttu-id="96896-127">Segreto di archiviazione con lettere morte.</span><span class="sxs-lookup"><span data-stu-id="96896-127">Dead letter storage secret.</span></span>
<span data-ttu-id="96896-128">Verranno offuscati durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="96896-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="96896-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96896-129">-DefaultProfile</span></span>
<span data-ttu-id="96896-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96896-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96896-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="96896-131">-EndpointDescription</span></span>
<span data-ttu-id="96896-132">Risorsa endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="96896-133">Per costruire, vedere la sezione Note per le proprietà di ENDPOINTDESCRIPTION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="96896-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96896-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="96896-134">-EndpointName</span></span>
<span data-ttu-id="96896-135">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="96896-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="96896-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="96896-136">-EndpointType</span></span>
<span data-ttu-id="96896-137">Tipo di endpoint Digital Twins</span><span class="sxs-lookup"><span data-stu-id="96896-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-138">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="96896-138">-NoWait</span></span>
<span data-ttu-id="96896-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="96896-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96896-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="96896-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="96896-141">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96896-142">-ResourceGroupName</span></span>
<span data-ttu-id="96896-143">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="96896-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="96896-144">-ResourceName</span></span>
<span data-ttu-id="96896-145">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="96896-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96896-146">-SubscriptionId</span></span>
<span data-ttu-id="96896-147">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="96896-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="96896-148">-TopicEndpoint</span></span>
<span data-ttu-id="96896-149">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="96896-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96896-150">-Confirm</span></span>
<span data-ttu-id="96896-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96896-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96896-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96896-152">-WhatIf</span></span>
<span data-ttu-id="96896-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96896-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96896-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96896-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96896-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96896-155">CommonParameters</span></span>
<span data-ttu-id="96896-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96896-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96896-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96896-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96896-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96896-158">INPUTS</span></span>

### <span data-ttu-id="96896-159">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="96896-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="96896-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96896-160">OUTPUTS</span></span>

### <span data-ttu-id="96896-161">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="96896-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="96896-162">Note</span><span class="sxs-lookup"><span data-stu-id="96896-162">NOTES</span></span>

<span data-ttu-id="96896-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="96896-163">ALIASES</span></span>

<span data-ttu-id="96896-164">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96896-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96896-165">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="96896-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96896-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96896-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96896-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : risorsa endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="96896-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="96896-168">`EndpointType <EndpointType>`: Il tipo di endpoint Digital Twins</span><span class="sxs-lookup"><span data-stu-id="96896-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="96896-169">`[DeadLetterSecret <String>]`: Segreto archiviazione lettere morte.</span><span class="sxs-lookup"><span data-stu-id="96896-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="96896-170">Verranno offuscati durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="96896-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="96896-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96896-171">RELATED LINKS</span></span>

