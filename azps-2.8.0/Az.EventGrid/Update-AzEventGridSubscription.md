---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674463"
---
# <span data-ttu-id="c754f-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c754f-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="c754f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c754f-102">SYNOPSIS</span></span>
<span data-ttu-id="c754f-103">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="c754f-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="c754f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c754f-104">SYNTAX</span></span>

### <span data-ttu-id="c754f-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c754f-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c754f-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c754f-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c754f-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c754f-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c754f-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c754f-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c754f-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c754f-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c754f-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c754f-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c754f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c754f-111">DESCRIPTION</span></span>
<span data-ttu-id="c754f-112">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="c754f-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="c754f-113">Può essere usato per aggiornare il filtro, la destinazione o le etichette di un abbonamento a un evento esistente.</span><span class="sxs-lookup"><span data-stu-id="c754f-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="c754f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c754f-114">EXAMPLES</span></span>

### <span data-ttu-id="c754f-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c754f-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="c754f-116">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="c754f-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="c754f-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c754f-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="c754f-118">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="c754f-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="c754f-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c754f-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="c754f-120">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per lo spazio dei nomi EventHub ContosoNamespace con il nuovo endpoint come \` https://requestb.in/1kxxoui1\ "e il nuovo filtro di SubjectEndsWith come \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="c754f-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="c754f-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c754f-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="c754f-122">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per il gruppo di risorse \` MyResourceGroupName \` con le nuove etichette $labels.</span><span class="sxs-lookup"><span data-stu-id="c754f-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="c754f-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c754f-123">PARAMETERS</span></span>

### <span data-ttu-id="c754f-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="c754f-124">-AdvancedFilter</span></span>
<span data-ttu-id="c754f-125">Filtro avanzato che specifica una matrice di più valori Hashtable usati per il filtro basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="c754f-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="c754f-126">Ogni valore Hashtable contiene le chiavi seguenti: Operation, Key e value o values.</span><span class="sxs-lookup"><span data-stu-id="c754f-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="c754f-127">Operator può essere uno dei valori seguenti: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringin, StringNotIn, StringBeginsWith, StringEndsWith o StringContains.</span><span class="sxs-lookup"><span data-stu-id="c754f-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="c754f-128">Key rappresenta la proprietà payload in cui vengono applicati i criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="c754f-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="c754f-129">Infine, il valore o i valori rappresentano il valore o il set di valori da abbinare.</span><span class="sxs-lookup"><span data-stu-id="c754f-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="c754f-130">Può trattarsi di un singolo valore del tipo corrispondente o di una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="c754f-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="c754f-131">Come esempio dei parametri di filtro avanzati: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) dove $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. Key1"; Values = @ (1, 2)} e $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="c754f-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="c754f-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="c754f-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="c754f-133">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="c754f-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="c754f-134">Specificare l'ID risorsa Azure di un contenitore di BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c754f-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="c754f-135">Ad esempio:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="c754f-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="c754f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c754f-136">-DefaultProfile</span></span>
<span data-ttu-id="c754f-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c754f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c754f-138">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c754f-138">-DomainName</span></span>
<span data-ttu-id="c754f-139">Nome del dominio in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-139">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c754f-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="c754f-140">-DomainTopicName</span></span>
<span data-ttu-id="c754f-141">Nome dell'argomento Domain in cui deve essere creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-141">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c754f-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="c754f-142">-Endpoint</span></span>
<span data-ttu-id="c754f-143">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="c754f-144">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di una coda di archiviazione EventHub, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="c754f-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="c754f-145">Ad esempio, l'ID risorsa per una connessione ibrida assume la forma seguente:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="c754f-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="c754f-146">È previsto che l'endpoint di destinazione venga creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="c754f-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="c754f-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c754f-147">-EndpointType</span></span>
<span data-ttu-id="c754f-148">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="c754f-148">Endpoint Type.</span></span>
<span data-ttu-id="c754f-149">Può essere webhook, eventhub, storagequeue, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="c754f-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="c754f-150">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="c754f-150">Default value is webhook.</span></span>

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

### <span data-ttu-id="c754f-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c754f-151">-EventSubscriptionName</span></span>
<span data-ttu-id="c754f-152">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="c754f-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="c754f-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="c754f-153">-EventTtl</span></span>
<span data-ttu-id="c754f-154">L'ora in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="c754f-155">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="c754f-155">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="c754f-156">-DataScadenza</span><span class="sxs-lookup"><span data-stu-id="c754f-156">-ExpirationDate</span></span>
<span data-ttu-id="c754f-157">Determina il valore DateTime di scadenza per l'abbonamento a un evento dopo il quale l'abbonamento verrà ritirato.</span><span class="sxs-lookup"><span data-stu-id="c754f-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="c754f-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="c754f-158">-IncludedEventType</span></span>
<span data-ttu-id="c754f-159">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="c754f-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c754f-160">-InputObject</span></span>
<span data-ttu-id="c754f-161">Oggetto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="c754f-161">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="c754f-162">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="c754f-162">-Label</span></span>
<span data-ttu-id="c754f-163">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="c754f-163">Labels for the event subscription</span></span>

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

### <span data-ttu-id="c754f-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="c754f-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="c754f-165">Numero massimo di tentativi di recapitare l'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="c754f-166">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="c754f-166">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="c754f-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c754f-167">-ResourceGroupName</span></span>
<span data-ttu-id="c754f-168">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="c754f-168">The resource group of the topic.</span></span>

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

### <span data-ttu-id="c754f-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c754f-169">-ResourceId</span></span>
<span data-ttu-id="c754f-170">Identificatore della risorsa a cui è stato creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="c754f-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="c754f-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="c754f-172">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="c754f-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="c754f-173">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="c754f-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="c754f-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="c754f-174">-SubjectEndsWith</span></span>
<span data-ttu-id="c754f-175">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="c754f-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="c754f-176">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="c754f-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="c754f-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c754f-177">-TopicName</span></span>
<span data-ttu-id="c754f-178">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c754f-178">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c754f-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c754f-179">-Confirm</span></span>
<span data-ttu-id="c754f-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c754f-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c754f-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c754f-181">-WhatIf</span></span>
<span data-ttu-id="c754f-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c754f-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c754f-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c754f-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c754f-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c754f-184">CommonParameters</span></span>
<span data-ttu-id="c754f-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c754f-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c754f-186">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c754f-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c754f-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c754f-187">INPUTS</span></span>

### <span data-ttu-id="c754f-188">System. String</span><span class="sxs-lookup"><span data-stu-id="c754f-188">System.String</span></span>

### <span data-ttu-id="c754f-189">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c754f-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c754f-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c754f-190">OUTPUTS</span></span>

### <span data-ttu-id="c754f-191">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c754f-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c754f-192">Note</span><span class="sxs-lookup"><span data-stu-id="c754f-192">NOTES</span></span>

## <span data-ttu-id="c754f-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c754f-193">RELATED LINKS</span></span>