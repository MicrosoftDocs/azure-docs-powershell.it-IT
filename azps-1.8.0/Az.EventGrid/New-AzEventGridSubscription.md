---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395187"
---
# <span data-ttu-id="0c6b3-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0c6b3-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="0c6b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6b3-103">Crea una nuova sottoscrizione di eventi della griglia di eventi di Azure a un argomento, una risorsa Azure, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="0c6b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c6b3-104">SYNTAX</span></span>

### <span data-ttu-id="0c6b3-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c6b3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6b3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6b3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6b3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6b3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6b3-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6b3-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6b3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c6b3-109">DESCRIPTION</span></span>
<span data-ttu-id="0c6b3-110">Creare una nuova sottoscrizione di eventi a un argomento della griglia di eventi di Azure, una risorsa Azure supportata, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="0c6b3-111">Per creare un abbonamento a un evento all'abbonamento Azure selezionato, specificare il nome della sottoscrizione dell'evento e l'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0c6b3-112">Per creare un abbonamento a un gruppo di risorse, specificare il nome del gruppo di risorse oltre al nome della sottoscrizione dell'evento e all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0c6b3-113">Per creare un abbonamento a un evento di Azure Event Grid, specificare anche il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="0c6b3-114">Per creare un abbonamento a una risorsa Azure supportata, specificare l'ID risorsa completa della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="0c6b3-115">Per visualizzare l'elenco dei tipi supportati, eseguire il cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="0c6b3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c6b3-116">EXAMPLES</span></span>

### <span data-ttu-id="0c6b3-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c6b3-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c6b3-118">Crea un nuovo abbonamento \` a EventSubscription1 \` a un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0c6b3-119">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c6b3-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c6b3-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c6b3-121">Crea un nuovo abbonamento \` \` a un evento EventSubscription1 a un gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0c6b3-122">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c6b3-123">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0c6b3-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c6b3-124">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0c6b3-125">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c6b3-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="0c6b3-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="0c6b3-127">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0c6b3-128">Questo abbonamento agli eventi specifica i filtri aggiuntivi per i tipi di evento e l'oggetto e solo gli eventi che soddisfano tali filtri verranno recapitati all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="0c6b3-129">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="0c6b3-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="0c6b3-130">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'hub eventi specificato come destinazione per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="0c6b3-131">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c6b3-132">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="0c6b3-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c6b3-133">Crea un nuovo evento \` di sottoscrizione \` di EventSubscription1 in uno spazio dei nomi EventHub con l'endpoint di destinazione webhook specificato `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0c6b3-134">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="0c6b3-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c6b3-135">PARAMETERS</span></span>

### <span data-ttu-id="0c6b3-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c6b3-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="0c6b3-137">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="0c6b3-138">Specificare l'ID risorsa Azure di un contenitore di BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="0c6b3-139">Ad esempio:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="0c6b3-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6b3-140">-DefaultProfile</span></span>
<span data-ttu-id="0c6b3-141">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c6b3-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="0c6b3-142">-Endpoint</span></span>
<span data-ttu-id="0c6b3-143">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="0c6b3-144">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di una coda di archiviazione EventHub o hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="0c6b3-145">Ad esempio, l'ID risorsa per una connessione ibrida assume la forma seguente:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="0c6b3-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="0c6b3-146">È previsto che l'endpoint di destinazione venga creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0c6b3-147">-EndpointType</span></span>
<span data-ttu-id="0c6b3-148">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-148">Endpoint Type.</span></span>
<span data-ttu-id="0c6b3-149">Può essere webhook, eventhub, storagequeue o hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="0c6b3-150">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0c6b3-151">-EventSubscriptionName</span></span>
<span data-ttu-id="0c6b3-152">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="0c6b3-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="0c6b3-153">-EventTtl</span></span>
<span data-ttu-id="0c6b3-154">L'ora in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="0c6b3-155">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="0c6b3-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="0c6b3-156">-IncludedEventType</span></span>
<span data-ttu-id="0c6b3-157">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c6b3-158">-InputObject</span></span>
<span data-ttu-id="0c6b3-159">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-160">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="0c6b3-160">-Label</span></span>
<span data-ttu-id="0c6b3-161">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="0c6b3-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="0c6b3-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="0c6b3-163">Numero massimo di tentativi di recapitare l'evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="0c6b3-164">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="0c6b3-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6b3-165">-ResourceGroupName</span></span>
<span data-ttu-id="0c6b3-166">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-166">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c6b3-167">-ResourceId</span></span>
<span data-ttu-id="0c6b3-168">Identificatore della risorsa a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-168">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0c6b3-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="0c6b3-170">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="0c6b3-171">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="0c6b3-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="0c6b3-173">Filter che specifica che il campo Subject deve essere confrontato in modo sensibile al caso.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="0c6b3-174">Se non specificato, l'oggetto verrà confrontato in modo senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="0c6b3-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="0c6b3-175">-SubjectEndsWith</span></span>
<span data-ttu-id="0c6b3-176">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="0c6b3-177">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0c6b3-178">-TopicName</span></span>
<span data-ttu-id="0c6b3-179">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-179">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b3-180">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c6b3-180">-Confirm</span></span>
<span data-ttu-id="0c6b3-181">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6b3-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6b3-182">-WhatIf</span></span>
<span data-ttu-id="0c6b3-183">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6b3-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6b3-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6b3-185">CommonParameters</span></span>
<span data-ttu-id="0c6b3-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6b3-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6b3-187">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6b3-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6b3-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c6b3-188">INPUTS</span></span>

### <span data-ttu-id="0c6b3-189">System. String</span><span class="sxs-lookup"><span data-stu-id="0c6b3-189">System.String</span></span>

### <span data-ttu-id="0c6b3-190">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0c6b3-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="0c6b3-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="0c6b3-191">System.String[]</span></span>

## <span data-ttu-id="0c6b3-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c6b3-192">OUTPUTS</span></span>

### <span data-ttu-id="0c6b3-193">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0c6b3-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0c6b3-194">Note</span><span class="sxs-lookup"><span data-stu-id="0c6b3-194">NOTES</span></span>

## <span data-ttu-id="0c6b3-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c6b3-195">RELATED LINKS</span></span>
