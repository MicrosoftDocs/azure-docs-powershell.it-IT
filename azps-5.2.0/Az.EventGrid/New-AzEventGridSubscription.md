---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363730"
---
# <span data-ttu-id="d3e05-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d3e05-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="d3e05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3e05-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e05-103">Crea una nuova sottoscrizione di eventi della griglia di eventi di Azure a un argomento, una risorsa Azure, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3e05-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="d3e05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3e05-104">SYNTAX</span></span>

### <span data-ttu-id="d3e05-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3e05-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e05-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e05-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e05-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3e05-113">DESCRIPTION</span></span>
<span data-ttu-id="d3e05-114">Creare una nuova sottoscrizione di eventi a un argomento della griglia di eventi di Azure, una risorsa Azure supportata, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3e05-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="d3e05-115">Per creare un abbonamento a un evento all'abbonamento Azure selezionato, specificare il nome della sottoscrizione dell'evento e l'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="d3e05-116">Per creare un abbonamento a un gruppo di risorse, specificare il nome del gruppo di risorse oltre al nome della sottoscrizione dell'evento e all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="d3e05-117">Per creare un abbonamento a un evento di Azure Event Grid, specificare anche il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="d3e05-118">Per creare un abbonamento a una risorsa Azure supportata, specificare l'ID risorsa completa della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3e05-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="d3e05-119">Per visualizzare l'elenco dei tipi supportati, eseguire il cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="d3e05-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="d3e05-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3e05-120">EXAMPLES</span></span>

### <span data-ttu-id="d3e05-121">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3e05-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d3e05-122">Crea un nuovo abbonamento \` a EventSubscription1 \` a un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d3e05-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d3e05-123">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d3e05-124">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d3e05-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d3e05-125">Crea un nuovo abbonamento \` \` a un evento EventSubscription1 a un gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d3e05-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d3e05-126">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d3e05-127">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d3e05-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d3e05-128">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d3e05-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d3e05-129">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d3e05-130">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d3e05-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="d3e05-131">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d3e05-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d3e05-132">Questo abbonamento agli eventi specifica i filtri aggiuntivi per i tipi di evento e l'oggetto e solo gli eventi che soddisfano tali filtri verranno recapitati all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="d3e05-133">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="d3e05-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="d3e05-134">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'hub eventi specificato come destinazione per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="d3e05-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="d3e05-135">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d3e05-136">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="d3e05-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d3e05-137">Crea un nuovo evento \` di sottoscrizione \` di EventSubscription1 in uno spazio dei nomi EventHub con l'endpoint di destinazione webhook specificato `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d3e05-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d3e05-138">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="d3e05-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3e05-139">PARAMETERS</span></span>

### <span data-ttu-id="d3e05-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="d3e05-140">-AdvancedFilter</span></span>
<span data-ttu-id="d3e05-141">Filtro avanzato che specifica una matrice di più valori Hashtable usati per il filtro basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="d3e05-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="d3e05-142">Ogni valore Hashtable contiene le chiavi seguenti: Operation, Key e value o values.</span><span class="sxs-lookup"><span data-stu-id="d3e05-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="d3e05-143">Operator può essere uno dei valori seguenti: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringin, StringNotIn, StringBeginsWith, StringEndsWith o StringContains.</span><span class="sxs-lookup"><span data-stu-id="d3e05-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="d3e05-144">Key rappresenta la proprietà payload in cui vengono applicati i criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="d3e05-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="d3e05-145">Infine, il valore o i valori rappresentano il valore o il set di valori da abbinare.</span><span class="sxs-lookup"><span data-stu-id="d3e05-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="d3e05-146">Può trattarsi di un singolo valore del tipo corrispondente o di una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="d3e05-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="d3e05-147">Come esempio dei parametri di filtro avanzati: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) dove $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. Key1"; Values = @ (1, 2)} e $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="d3e05-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="d3e05-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="d3e05-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="d3e05-149">ID applicazione o URI di Azure Active Directory (AAD) per ottenere il token di accesso che verrà incluso come token del portatore nelle richieste di recapito. Applicabile solo per webhook come destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="d3e05-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="d3e05-151">ID tenant di Azure Active Directory (AAD) per ottenere il token di accesso che verrà incluso come token del portatore nelle richieste di recapito. Applicabile solo per webhook come destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3e05-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="d3e05-153">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="d3e05-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="d3e05-154">Specificare l'ID risorsa Azure di un contenitore di BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="d3e05-155">Ad esempio:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="d3e05-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="d3e05-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e05-156">-DefaultProfile</span></span>
<span data-ttu-id="d3e05-157">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d3e05-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3e05-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="d3e05-158">-DeliverySchema</span></span>
<span data-ttu-id="d3e05-159">Schema da usare per la distribuzione di eventi alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3e05-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="d3e05-160">I valori possibili sono: eventgridschema, CustomInputSchema o cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="d3e05-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="d3e05-161">Il valore predefinito è CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="d3e05-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="d3e05-162">-DomainInputObject</span></span>
<span data-ttu-id="d3e05-163">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d3e05-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="d3e05-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d3e05-164">-DomainName</span></span>
<span data-ttu-id="d3e05-165">Nome del dominio della griglia dell'evento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d3e05-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="d3e05-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="d3e05-167">Oggetto argomento del dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d3e05-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="d3e05-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="d3e05-168">-DomainTopicName</span></span>
<span data-ttu-id="d3e05-169">Nome dell'argomento Domain in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d3e05-170">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d3e05-170">-Endpoint</span></span>
<span data-ttu-id="d3e05-171">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="d3e05-172">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di una coda di archiviazione EventHub, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="d3e05-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="d3e05-173">Ad esempio, l'ID risorsa per una connessione ibrida assume la forma seguente:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="d3e05-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="d3e05-174">È previsto che l'endpoint di destinazione venga creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="d3e05-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="d3e05-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d3e05-175">-EndpointType</span></span>
<span data-ttu-id="d3e05-176">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="d3e05-176">Endpoint Type.</span></span>
<span data-ttu-id="d3e05-177">Può essere webhook, eventhub, storagequeue, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="d3e05-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="d3e05-178">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="d3e05-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d3e05-179">-EventSubscriptionName</span></span>
<span data-ttu-id="d3e05-180">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="d3e05-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="d3e05-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="d3e05-181">-EventTtl</span></span>
<span data-ttu-id="d3e05-182">L'ora in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="d3e05-183">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="d3e05-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="d3e05-184">-DataScadenza</span><span class="sxs-lookup"><span data-stu-id="d3e05-184">-ExpirationDate</span></span>
<span data-ttu-id="d3e05-185">Determina il valore DateTime di scadenza per l'abbonamento a un evento dopo il quale l'abbonamento verrà ritirato.</span><span class="sxs-lookup"><span data-stu-id="d3e05-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="d3e05-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="d3e05-186">-IncludedEventType</span></span>
<span data-ttu-id="d3e05-187">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e05-188">-InputObject</span></span>
<span data-ttu-id="d3e05-189">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d3e05-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d3e05-190">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="d3e05-190">-Label</span></span>
<span data-ttu-id="d3e05-191">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="d3e05-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e05-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="d3e05-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="d3e05-193">Numero massimo di tentativi di recapitare l'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="d3e05-194">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="d3e05-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="d3e05-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="d3e05-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="d3e05-196">Numero massimo di eventi in un batch.</span><span class="sxs-lookup"><span data-stu-id="d3e05-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="d3e05-197">Questo valore deve essere compreso tra 1 e 5000.</span><span class="sxs-lookup"><span data-stu-id="d3e05-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="d3e05-198">Questo parametro è valido quando il tipo di Endpint è solo webhook.</span><span class="sxs-lookup"><span data-stu-id="d3e05-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="d3e05-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="d3e05-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="d3e05-200">Dimensioni del batch preferite in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="d3e05-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="d3e05-201">Questo valore deve essere compreso tra 1 e 1024.</span><span class="sxs-lookup"><span data-stu-id="d3e05-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="d3e05-202">Questo parametro è valido quando il tipo di Endpint è solo webhook.</span><span class="sxs-lookup"><span data-stu-id="d3e05-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="d3e05-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e05-203">-ResourceGroupName</span></span>
<span data-ttu-id="d3e05-204">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="d3e05-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e05-205">-ResourceId</span></span>
<span data-ttu-id="d3e05-206">Identificatore della risorsa a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d3e05-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d3e05-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="d3e05-208">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="d3e05-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="d3e05-209">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="d3e05-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="d3e05-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="d3e05-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="d3e05-211">Filter che specifica che il campo Subject deve essere confrontato in modo sensibile al caso.</span><span class="sxs-lookup"><span data-stu-id="d3e05-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="d3e05-212">Se non specificato, l'oggetto verrà confrontato in modo senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d3e05-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="d3e05-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="d3e05-213">-SubjectEndsWith</span></span>
<span data-ttu-id="d3e05-214">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="d3e05-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="d3e05-215">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3e05-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="d3e05-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d3e05-216">-TopicName</span></span>
<span data-ttu-id="d3e05-217">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d3e05-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d3e05-218">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3e05-218">-Confirm</span></span>
<span data-ttu-id="d3e05-219">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e05-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e05-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e05-220">-WhatIf</span></span>
<span data-ttu-id="d3e05-221">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e05-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e05-222">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e05-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e05-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e05-223">CommonParameters</span></span>
<span data-ttu-id="d3e05-224">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e05-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e05-225">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3e05-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e05-226">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3e05-226">INPUTS</span></span>

### <span data-ttu-id="d3e05-227">System. String</span><span class="sxs-lookup"><span data-stu-id="d3e05-227">System.String</span></span>

### <span data-ttu-id="d3e05-228">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d3e05-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="d3e05-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="d3e05-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="d3e05-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d3e05-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="d3e05-231">System. String []</span><span class="sxs-lookup"><span data-stu-id="d3e05-231">System.String[]</span></span>

### <span data-ttu-id="d3e05-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3e05-232">System.Int32</span></span>

## <span data-ttu-id="d3e05-233">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3e05-233">OUTPUTS</span></span>

### <span data-ttu-id="d3e05-234">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d3e05-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d3e05-235">Note</span><span class="sxs-lookup"><span data-stu-id="d3e05-235">NOTES</span></span>

## <span data-ttu-id="d3e05-236">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3e05-236">RELATED LINKS</span></span>
