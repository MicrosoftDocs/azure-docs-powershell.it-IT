---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: a2b8ba54a812f405d634066881c32b6b0467eeab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864250"
---
# <span data-ttu-id="381f6-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="381f6-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="381f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="381f6-102">SYNOPSIS</span></span>
<span data-ttu-id="381f6-103">Crea una nuova sottoscrizione di eventi della griglia di eventi di Azure a un argomento, una risorsa Azure, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="381f6-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="381f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="381f6-104">SYNTAX</span></span>

### <span data-ttu-id="381f6-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="381f6-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="381f6-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381f6-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="381f6-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381f6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="381f6-113">DESCRIPTION</span></span>
<span data-ttu-id="381f6-114">Creare una nuova sottoscrizione di eventi a un argomento della griglia di eventi di Azure, una risorsa Azure supportata, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="381f6-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="381f6-115">Per creare un abbonamento a un evento all'abbonamento Azure selezionato, specificare il nome della sottoscrizione dell'evento e l'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="381f6-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="381f6-116">Per creare un abbonamento a un gruppo di risorse, specificare il nome del gruppo di risorse oltre al nome della sottoscrizione dell'evento e all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="381f6-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="381f6-117">Per creare un abbonamento a un evento di Azure Event Grid, specificare anche il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="381f6-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="381f6-118">Per creare un abbonamento a una risorsa Azure supportata, specificare l'ID risorsa completa della risorsa.</span><span class="sxs-lookup"><span data-stu-id="381f6-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="381f6-119">Per visualizzare l'elenco dei tipi supportati, eseguire il cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="381f6-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="381f6-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="381f6-120">EXAMPLES</span></span>

### <span data-ttu-id="381f6-121">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="381f6-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="381f6-122">Crea un nuovo abbonamento \` a EventSubscription1 \` a un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="381f6-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="381f6-123">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="381f6-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="381f6-124">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="381f6-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="381f6-125">Crea un nuovo abbonamento \` \` a un evento EventSubscription1 a un gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="381f6-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="381f6-126">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="381f6-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="381f6-127">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="381f6-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="381f6-128">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="381f6-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="381f6-129">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="381f6-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="381f6-130">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="381f6-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="381f6-131">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="381f6-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="381f6-132">Questo abbonamento agli eventi specifica i filtri aggiuntivi per i tipi di evento e l'oggetto e solo gli eventi che soddisfano tali filtri verranno recapitati all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="381f6-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="381f6-133">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="381f6-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="381f6-134">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'hub eventi specificato come destinazione per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="381f6-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="381f6-135">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="381f6-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="381f6-136">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="381f6-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="381f6-137">Crea un nuovo evento \` di sottoscrizione \` di EventSubscription1 in uno spazio dei nomi EventHub con l'endpoint di destinazione webhook specificato https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="381f6-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="381f6-138">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="381f6-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="381f6-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="381f6-139">PARAMETERS</span></span>

### <span data-ttu-id="381f6-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="381f6-140">-AdvancedFilter</span></span>
<span data-ttu-id="381f6-141">Filtro avanzato che specifica una matrice di più valori Hashtable usati per il filtro basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="381f6-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="381f6-142">Ogni valore Hashtable contiene le chiavi seguenti: Operation, Key e value o values.</span><span class="sxs-lookup"><span data-stu-id="381f6-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="381f6-143">Operator può essere uno dei valori seguenti: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringin, StringNotIn, StringBeginsWith, StringEndsWith o StringContains.</span><span class="sxs-lookup"><span data-stu-id="381f6-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="381f6-144">Key rappresenta la proprietà payload in cui vengono applicati i criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="381f6-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="381f6-145">Infine, il valore o i valori rappresentano il valore o il set di valori da abbinare.</span><span class="sxs-lookup"><span data-stu-id="381f6-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="381f6-146">Può trattarsi di un singolo valore del tipo corrispondente o di una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="381f6-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="381f6-147">Come esempio dei parametri di filtro avanzati: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) dove $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. Key1"; Values = @ (1, 2)} e $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="381f6-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="381f6-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="381f6-149">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="381f6-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="381f6-150">Specificare l'ID risorsa Azure di un contenitore di BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="381f6-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="381f6-151">Ad esempio:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="381f6-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381f6-152">-DefaultProfile</span></span>
<span data-ttu-id="381f6-153">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="381f6-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="381f6-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="381f6-154">-DomainInputObject</span></span>
<span data-ttu-id="381f6-155">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="381f6-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-156">-DomainName</span><span class="sxs-lookup"><span data-stu-id="381f6-156">-DomainName</span></span>
<span data-ttu-id="381f6-157">Nome del dominio della griglia dell'evento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="381f6-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="381f6-159">Oggetto argomento del dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="381f6-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="381f6-160">-DomainTopicName</span></span>
<span data-ttu-id="381f6-161">Nome dell'argomento Domain in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-162">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="381f6-162">-Endpoint</span></span>
<span data-ttu-id="381f6-163">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="381f6-164">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di una coda di archiviazione EventHub, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="381f6-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="381f6-165">Ad esempio, l'ID risorsa per una connessione ibrida assume la forma seguente:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="381f6-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="381f6-166">È previsto che l'endpoint di destinazione venga creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="381f6-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="381f6-167">-EndpointType</span></span>
<span data-ttu-id="381f6-168">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="381f6-168">Endpoint Type.</span></span>
<span data-ttu-id="381f6-169">Può essere webhook, eventhub, storagequeue, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="381f6-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="381f6-170">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="381f6-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="381f6-171">-EventSubscriptionName</span></span>
<span data-ttu-id="381f6-172">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="381f6-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="381f6-173">-EventTtl</span></span>
<span data-ttu-id="381f6-174">L'ora in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="381f6-175">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="381f6-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-176">-DataScadenza</span><span class="sxs-lookup"><span data-stu-id="381f6-176">-ExpirationDate</span></span>
<span data-ttu-id="381f6-177">Determina il valore DateTime di scadenza per l'abbonamento a un evento dopo il quale l'abbonamento verrà ritirato.</span><span class="sxs-lookup"><span data-stu-id="381f6-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="381f6-178">-IncludedEventType</span></span>
<span data-ttu-id="381f6-179">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="381f6-180">-InputObject</span></span>
<span data-ttu-id="381f6-181">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="381f6-181">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="381f6-182">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="381f6-182">-Label</span></span>
<span data-ttu-id="381f6-183">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="381f6-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="381f6-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="381f6-185">Numero massimo di tentativi di recapitare l'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="381f6-186">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="381f6-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="381f6-187">-ResourceGroupName</span></span>
<span data-ttu-id="381f6-188">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="381f6-188">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-189">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="381f6-189">-ResourceId</span></span>
<span data-ttu-id="381f6-190">Identificatore della risorsa a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-190">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="381f6-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="381f6-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="381f6-192">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="381f6-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="381f6-193">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="381f6-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="381f6-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="381f6-195">Filter che specifica che il campo Subject deve essere confrontato in modo sensibile al caso.</span><span class="sxs-lookup"><span data-stu-id="381f6-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="381f6-196">Se non specificato, l'oggetto verrà confrontato in modo senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="381f6-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="381f6-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="381f6-197">-SubjectEndsWith</span></span>
<span data-ttu-id="381f6-198">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="381f6-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="381f6-199">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="381f6-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381f6-200">-TopicName</span><span class="sxs-lookup"><span data-stu-id="381f6-200">-TopicName</span></span>
<span data-ttu-id="381f6-201">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="381f6-201">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="381f6-202">-Confermare</span><span class="sxs-lookup"><span data-stu-id="381f6-202">-Confirm</span></span>
<span data-ttu-id="381f6-203">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381f6-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="381f6-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381f6-204">-WhatIf</span></span>
<span data-ttu-id="381f6-205">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="381f6-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381f6-206">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="381f6-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="381f6-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381f6-207">CommonParameters</span></span>
<span data-ttu-id="381f6-208">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381f6-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381f6-209">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381f6-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381f6-210">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="381f6-210">INPUTS</span></span>

### <span data-ttu-id="381f6-211">System. String</span><span class="sxs-lookup"><span data-stu-id="381f6-211">System.String</span></span>

### <span data-ttu-id="381f6-212">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="381f6-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="381f6-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="381f6-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="381f6-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="381f6-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="381f6-215">System. String []</span><span class="sxs-lookup"><span data-stu-id="381f6-215">System.String[]</span></span>

### <span data-ttu-id="381f6-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="381f6-216">System.Int32</span></span>

## <span data-ttu-id="381f6-217">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="381f6-217">OUTPUTS</span></span>

### <span data-ttu-id="381f6-218">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="381f6-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="381f6-219">Note</span><span class="sxs-lookup"><span data-stu-id="381f6-219">NOTES</span></span>

## <span data-ttu-id="381f6-220">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="381f6-220">RELATED LINKS</span></span>
