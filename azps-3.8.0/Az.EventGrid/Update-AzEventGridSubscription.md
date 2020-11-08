---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: d4967dd45cc420035a4be60736389729d019fd45
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018888"
---
# <span data-ttu-id="da2de-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="da2de-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="da2de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da2de-102">SYNOPSIS</span></span>
<span data-ttu-id="da2de-103">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="da2de-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="da2de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da2de-104">SYNTAX</span></span>

### <span data-ttu-id="da2de-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da2de-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da2de-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="da2de-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da2de-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da2de-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da2de-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="da2de-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da2de-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="da2de-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da2de-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="da2de-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da2de-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da2de-111">DESCRIPTION</span></span>
<span data-ttu-id="da2de-112">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="da2de-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="da2de-113">Può essere usato per aggiornare il filtro, la destinazione o le etichette di un abbonamento a un evento esistente.</span><span class="sxs-lookup"><span data-stu-id="da2de-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="da2de-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da2de-114">EXAMPLES</span></span>

### <span data-ttu-id="da2de-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da2de-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="da2de-116">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="da2de-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="da2de-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="da2de-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="da2de-118">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="da2de-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="da2de-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="da2de-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="da2de-120">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per lo spazio dei nomi EventHub ContosoNamespace con il nuovo endpoint come \` https://requestb.in/1kxxoui1\ "e il nuovo filtro di SubjectEndsWith come \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="da2de-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="da2de-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="da2de-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="da2de-122">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per il gruppo di risorse \` MyResourceGroupName \` con le nuove etichette $labels.</span><span class="sxs-lookup"><span data-stu-id="da2de-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="da2de-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da2de-123">PARAMETERS</span></span>

### <span data-ttu-id="da2de-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="da2de-124">-AdvancedFilter</span></span>
<span data-ttu-id="da2de-125">Filtro avanzato che specifica una matrice di più valori Hashtable usati per il filtro basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="da2de-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="da2de-126">Ogni valore Hashtable contiene le chiavi seguenti: Operation, Key e value o values.</span><span class="sxs-lookup"><span data-stu-id="da2de-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="da2de-127">Operator può essere uno dei valori seguenti: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringin, StringNotIn, StringBeginsWith, StringEndsWith o StringContains.</span><span class="sxs-lookup"><span data-stu-id="da2de-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="da2de-128">Key rappresenta la proprietà payload in cui vengono applicati i criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="da2de-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="da2de-129">Infine, il valore o i valori rappresentano il valore o il set di valori da abbinare.</span><span class="sxs-lookup"><span data-stu-id="da2de-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="da2de-130">Può trattarsi di un singolo valore del tipo corrispondente o di una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="da2de-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="da2de-131">Come esempio dei parametri di filtro avanzati: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) dove $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. Key1"; Values = @ (1, 2)} e $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="da2de-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="da2de-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="da2de-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="da2de-133">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="da2de-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="da2de-134">Specificare l'ID risorsa Azure di un contenitore di BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="da2de-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="da2de-135">Ad esempio:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="da2de-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="da2de-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da2de-136">-DefaultProfile</span></span>
<span data-ttu-id="da2de-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da2de-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da2de-138">-DomainName</span><span class="sxs-lookup"><span data-stu-id="da2de-138">-DomainName</span></span>
<span data-ttu-id="da2de-139">Nome del dominio in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="da2de-140">-DomainTopicName</span></span>
<span data-ttu-id="da2de-141">Nome dell'argomento Domain in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="da2de-142">-Endpoint</span></span>
<span data-ttu-id="da2de-143">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="da2de-144">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di una coda di archiviazione EventHub, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="da2de-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="da2de-145">Ad esempio, l'ID risorsa per una connessione ibrida assume la forma seguente:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="da2de-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="da2de-146">È previsto che l'endpoint di destinazione venga creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="da2de-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="da2de-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="da2de-147">-EndpointType</span></span>
<span data-ttu-id="da2de-148">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="da2de-148">Endpoint Type.</span></span>
<span data-ttu-id="da2de-149">Può essere webhook, eventhub, storagequeue, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="da2de-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="da2de-150">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="da2de-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="da2de-151">-EventSubscriptionName</span></span>
<span data-ttu-id="da2de-152">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="da2de-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="da2de-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="da2de-153">-EventTtl</span></span>
<span data-ttu-id="da2de-154">L'ora in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="da2de-155">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="da2de-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-156">-DataScadenza</span><span class="sxs-lookup"><span data-stu-id="da2de-156">-ExpirationDate</span></span>
<span data-ttu-id="da2de-157">Determina il valore DateTime di scadenza per l'abbonamento a un evento dopo il quale l'abbonamento verrà ritirato.</span><span class="sxs-lookup"><span data-stu-id="da2de-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="da2de-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="da2de-158">-IncludedEventType</span></span>
<span data-ttu-id="da2de-159">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da2de-160">-InputObject</span></span>
<span data-ttu-id="da2de-161">Oggetto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="da2de-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-162">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="da2de-162">-Label</span></span>
<span data-ttu-id="da2de-163">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="da2de-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="da2de-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="da2de-165">Numero massimo di tentativi di recapitare l'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="da2de-166">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="da2de-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da2de-167">-ResourceGroupName</span></span>
<span data-ttu-id="da2de-168">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="da2de-168">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da2de-169">-ResourceId</span></span>
<span data-ttu-id="da2de-170">Identificatore della risorsa a cui è stato creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="da2de-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="da2de-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="da2de-172">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="da2de-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="da2de-173">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="da2de-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="da2de-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="da2de-174">-SubjectEndsWith</span></span>
<span data-ttu-id="da2de-175">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="da2de-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="da2de-176">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="da2de-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="da2de-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="da2de-177">-TopicName</span></span>
<span data-ttu-id="da2de-178">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="da2de-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2de-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da2de-179">-Confirm</span></span>
<span data-ttu-id="da2de-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da2de-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da2de-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da2de-181">-WhatIf</span></span>
<span data-ttu-id="da2de-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da2de-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da2de-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da2de-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da2de-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2de-184">CommonParameters</span></span>
<span data-ttu-id="da2de-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da2de-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2de-186">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da2de-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2de-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da2de-187">INPUTS</span></span>

### <span data-ttu-id="da2de-188">System. String</span><span class="sxs-lookup"><span data-stu-id="da2de-188">System.String</span></span>

### <span data-ttu-id="da2de-189">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="da2de-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="da2de-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da2de-190">OUTPUTS</span></span>

### <span data-ttu-id="da2de-191">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="da2de-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="da2de-192">Note</span><span class="sxs-lookup"><span data-stu-id="da2de-192">NOTES</span></span>

## <span data-ttu-id="da2de-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da2de-193">RELATED LINKS</span></span>
