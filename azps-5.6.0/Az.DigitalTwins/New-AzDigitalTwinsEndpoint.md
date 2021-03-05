---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984940"
---
# <span data-ttu-id="ff74e-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff74e-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="ff74e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff74e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff74e-103">Creare o aggiornare l'endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="ff74e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff74e-104">SYNTAX</span></span>

### <span data-ttu-id="ff74e-105">EventHub (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff74e-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff74e-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff74e-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff74e-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff74e-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff74e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ff74e-108">DESCRIPTION</span></span>
<span data-ttu-id="ff74e-109">Creare o aggiornare l'endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="ff74e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff74e-110">EXAMPLES</span></span>

### <span data-ttu-id="ff74e-111">Esempio 1: Creare un oggetto AzDigitalTwinsEndpoint per Eventhub</span><span class="sxs-lookup"><span data-stu-id="ff74e-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ff74e-112">Creare un AzDigitalTwinsEndpoint per Eventhub tramite connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ff74e-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="ff74e-113">Esempio 2: Creare una cella AzDigitalTwinsEndpoint per EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff74e-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ff74e-114">Creare un oggetto AzDigitalTwinsEndpoint per Eventhub da TopicEndpoint e accessKey1</span><span class="sxs-lookup"><span data-stu-id="ff74e-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="ff74e-115">Esempio 3: Creare un AzDigitalTwinsEndpoint per ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff74e-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ff74e-116">Creare un AzDigitalTwinsEndpoint per ServicBus di PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="ff74e-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="ff74e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff74e-117">PARAMETERS</span></span>

### <span data-ttu-id="ff74e-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="ff74e-118">-AccessKey1</span></span>
<span data-ttu-id="ff74e-119">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff74e-120">-AsJob</span></span>
<span data-ttu-id="ff74e-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ff74e-121">Run the command as a job</span></span>

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

### <span data-ttu-id="ff74e-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ff74e-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="ff74e-123">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ff74e-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="ff74e-125">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="ff74e-126">-DeadLetterSecret</span></span>
<span data-ttu-id="ff74e-127">Segreto per lo spazio di archiviazione delle lettere erre.</span><span class="sxs-lookup"><span data-stu-id="ff74e-127">Dead letter storage secret.</span></span>
<span data-ttu-id="ff74e-128">Durante la lettura verrà offuscata.</span><span class="sxs-lookup"><span data-stu-id="ff74e-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="ff74e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff74e-129">-DefaultProfile</span></span>
<span data-ttu-id="ff74e-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff74e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff74e-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="ff74e-131">-EndpointDescription</span></span>
<span data-ttu-id="ff74e-132">Risorsa endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="ff74e-133">Per creare, vedere la sezione NOTE per le proprietà ENDPOINTDESCRIPTION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ff74e-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff74e-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ff74e-134">-EndpointName</span></span>
<span data-ttu-id="ff74e-135">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="ff74e-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="ff74e-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ff74e-136">-EndpointType</span></span>
<span data-ttu-id="ff74e-137">Il tipo di endpoint delle piattaforme digitali</span><span class="sxs-lookup"><span data-stu-id="ff74e-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="ff74e-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff74e-138">-NoWait</span></span>
<span data-ttu-id="ff74e-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ff74e-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ff74e-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="ff74e-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="ff74e-141">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff74e-142">-ResourceGroupName</span></span>
<span data-ttu-id="ff74e-143">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ff74e-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ff74e-144">-ResourceName</span></span>
<span data-ttu-id="ff74e-145">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ff74e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff74e-146">-SubscriptionId</span></span>
<span data-ttu-id="ff74e-147">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff74e-148">-TopicEndpoint</span></span>
<span data-ttu-id="ff74e-149">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ff74e-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="ff74e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff74e-150">-Confirm</span></span>
<span data-ttu-id="ff74e-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff74e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff74e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff74e-152">-WhatIf</span></span>
<span data-ttu-id="ff74e-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff74e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff74e-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff74e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff74e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff74e-155">CommonParameters</span></span>
<span data-ttu-id="ff74e-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff74e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff74e-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff74e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff74e-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="ff74e-158">INPUTS</span></span>

### <span data-ttu-id="ff74e-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="ff74e-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="ff74e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff74e-160">OUTPUTS</span></span>

### <span data-ttu-id="ff74e-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="ff74e-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="ff74e-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="ff74e-162">NOTES</span></span>

<span data-ttu-id="ff74e-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ff74e-163">ALIASES</span></span>

<span data-ttu-id="ff74e-164">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ff74e-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff74e-165">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ff74e-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff74e-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff74e-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff74e-167"><IDigitalTwinsEndpointResource>ENDPOINTDESCRIPTION: risorsa endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ff74e-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="ff74e-168">`EndpointType <EndpointType>`: il tipo di endpoint Disarriva digitali</span><span class="sxs-lookup"><span data-stu-id="ff74e-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="ff74e-169">`[DeadLetterSecret <String>]`: segreto per l'archiviazione delle lettere erre.</span><span class="sxs-lookup"><span data-stu-id="ff74e-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="ff74e-170">Durante la lettura verrà offuscata.</span><span class="sxs-lookup"><span data-stu-id="ff74e-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="ff74e-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff74e-171">RELATED LINKS</span></span>

