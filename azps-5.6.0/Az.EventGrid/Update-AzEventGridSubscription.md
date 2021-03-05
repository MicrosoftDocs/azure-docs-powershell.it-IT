---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: dc8515cb37d18a36fa00c6803fda06a1e4d1f1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001566"
---
# <span data-ttu-id="3e8e8-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3e8e8-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="3e8e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8e8-103">Aggiornare le proprietà di una sottoscrizione a un evento della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="3e8e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e8e8-104">SYNTAX</span></span>

### <span data-ttu-id="3e8e8-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8e8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8e8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8e8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8e8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e8e8-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8e8-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8e8-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8e8-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8e8-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e8e8-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8e8-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e8e8-111">DESCRIPTION</span></span>
<span data-ttu-id="3e8e8-112">Aggiornare le proprietà di una sottoscrizione a un evento della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="3e8e8-113">Può essere usato per aggiornare il filtro, la destinazione o le etichette di una sottoscrizione di evento esistente.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="3e8e8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e8e8-114">EXAMPLES</span></span>

### <span data-ttu-id="3e8e8-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e8e8-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3e8e8-116">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 per l'argomento Argomento1 nel gruppo di \` \` risorse \` \` MyResourceGroupName \` a \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3e8e8-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3e8e8-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e8e8-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3e8e8-118">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 per l'argomento Argomento1 nel gruppo di \` \` risorse \` \` MyResourceGroupName \` a \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3e8e8-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3e8e8-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3e8e8-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="3e8e8-120">Aggiorna le proprietà dell'abbonamento all'evento ES1 per lo spazio dei nomi EventHub ContosoWith con il nuovo endpoint come ' e il nuovo \` \` filtro \` https://requestb.in/1kxxoui1\ SubjectEndsWith come \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="3e8e8-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="3e8e8-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3e8e8-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="3e8e8-122">Aggiorna le proprietà della sottoscrizione evento ES1 per il gruppo di risorse \` \` \` MyResourceGroupName \` con le nuove etichette $labels.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="3e8e8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e8e8-123">PARAMETERS</span></span>

### <span data-ttu-id="3e8e8-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="3e8e8-124">-AdvancedFilter</span></span>
<span data-ttu-id="3e8e8-125">Filtro avanzato che specifica una matrice di più valori Hashtable usati per il filtro basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="3e8e8-126">Ogni valore Hashtable contiene le informazioni chiave-valore seguenti: Operazione, Chiave, Valore o Valori.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="3e8e8-127">L'operatore può essere uno dei valori seguenti: NumberIn, NumberNotIn, NumberLessWith, NumberGreaterWith, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith o StringContains.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="3e8e8-128">La chiave rappresenta la proprietà payload in cui vengono applicati i criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="3e8e8-129">Infine, Valore o Valori rappresenta il valore o il set di valori per cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="3e8e8-130">Può trattarsi di un singolo valore del tipo corrispondente o di una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="3e8e8-131">Come esempio dei parametri di filtro avanzati: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2) dove $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} e $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="3e8e8-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="3e8e8-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="3e8e8-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="3e8e8-133">L'ID applicazione di Azure Active Directory (AAD) o l'URI per ottenere il token di accesso che verrà incluso come token di orso nelle richieste di recapito. Applicabile solo per webhook come destinazione.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8e8-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="3e8e8-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="3e8e8-135">L'ID tenant di Azure Active Directory (AAD) per ottenere il token di accesso che verrà incluso come token del orso nelle richieste di recapito. Applicabile solo per webhook come destinazione.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8e8-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e8e8-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="3e8e8-137">Endpoint usato per archiviare gli eventi non recapitati.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="3e8e8-138">Specificare l'ID della risorsa Azure di un contenitore BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="3e8e8-139">Ad esempio: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="3e8e8-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="3e8e8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8e8-140">-DefaultProfile</span></span>
<span data-ttu-id="3e8e8-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e8e8-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="3e8e8-142">-DomainName</span></span>
<span data-ttu-id="3e8e8-143">Nome del dominio in cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3e8e8-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="3e8e8-144">-DomainTopicName</span></span>
<span data-ttu-id="3e8e8-145">Nome dell'argomento del dominio in cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3e8e8-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="3e8e8-146">-Endpoint</span></span>
<span data-ttu-id="3e8e8-147">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="3e8e8-148">Può trattarsi di un URL di una webhook o dell'ID della risorsa Azure di una coda di archiviazione, di EventHub, di connessione ibrida o di servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3e8e8-149">Ad esempio, l'ID risorsa per una connessione ibrida ha il formato seguente: /subscriptions/[ID sottoscrizione azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="3e8e8-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="3e8e8-150">È previsto che l'endpoint di destinazione sia creato e disponibile per l'uso prima di eseguire qualsiasi cmdlet della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="3e8e8-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3e8e8-151">-EndpointType</span></span>
<span data-ttu-id="3e8e8-152">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-152">Endpoint Type.</span></span>
<span data-ttu-id="3e8e8-153">Può trattarsi di webhook, eventhub, storagequeue, hybridconnection o servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3e8e8-154">Il valore predefinito è webhook.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8e8-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3e8e8-155">-EventSubscriptionName</span></span>
<span data-ttu-id="3e8e8-156">Nome della sottoscrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="3e8e8-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="3e8e8-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="3e8e8-157">-EventTtl</span></span>
<span data-ttu-id="3e8e8-158">Il tempo in minuti per il recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="3e8e8-159">Questo valore deve essere compreso tra 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="3e8e8-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="3e8e8-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="3e8e8-160">-ExpirationDate</span></span>
<span data-ttu-id="3e8e8-161">Determina la scadenza DateTime per la sottoscrizione dell'evento dopo la quale la sottoscrizione dell'evento verrà ritirata.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="3e8e8-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="3e8e8-162">-IncludedEventType</span></span>
<span data-ttu-id="3e8e8-163">Filtro che specifica un elenco di tipi di evento da includere. Se non viene specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="3e8e8-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e8e8-164">-InputObject</span></span>
<span data-ttu-id="3e8e8-165">Oggetto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="3e8e8-166">-Label</span><span class="sxs-lookup"><span data-stu-id="3e8e8-166">-Label</span></span>
<span data-ttu-id="3e8e8-167">Etichette per la sottoscrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="3e8e8-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="3e8e8-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="3e8e8-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="3e8e8-169">Numero massimo di tentativi di recapito dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="3e8e8-170">Questo valore deve essere compreso tra 1 e 30</span><span class="sxs-lookup"><span data-stu-id="3e8e8-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="3e8e8-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="3e8e8-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="3e8e8-172">Numero massimo di eventi in un batch.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="3e8e8-173">Questo valore deve essere compreso tra 1 e 5000.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="3e8e8-174">Questo parametro è valido quando Endpint Type è solo webhook.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="3e8e8-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="3e8e8-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="3e8e8-176">Dimensioni del batch preferite in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="3e8e8-177">Questo valore deve essere compreso tra 1 e 1024.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="3e8e8-178">Questo parametro è valido quando Endpint Type è solo webhook.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="3e8e8-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8e8-179">-ResourceGroupName</span></span>
<span data-ttu-id="3e8e8-180">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="3e8e8-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e8e8-181">-ResourceId</span></span>
<span data-ttu-id="3e8e8-182">Identificatore della risorsa a cui è stata creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="3e8e8-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="3e8e8-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="3e8e8-184">Filtro che specifica che verranno inclusi solo gli eventi che corrispondono al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="3e8e8-185">Se non viene specificato, verranno inclusi gli eventi con tutti i prefissi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="3e8e8-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="3e8e8-186">-SubjectEndsWith</span></span>
<span data-ttu-id="3e8e8-187">Filtro che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="3e8e8-188">Se non viene specificato, verranno inclusi gli eventi con tutti i suffissi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="3e8e8-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3e8e8-189">-TopicName</span></span>
<span data-ttu-id="3e8e8-190">Nome dell'argomento in cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3e8e8-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e8e8-191">-Confirm</span></span>
<span data-ttu-id="3e8e8-192">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8e8-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8e8-193">-WhatIf</span></span>
<span data-ttu-id="3e8e8-194">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8e8-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8e8-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8e8-196">CommonParameters</span></span>
<span data-ttu-id="3e8e8-197">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8e8-198">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8e8-199">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e8e8-199">INPUTS</span></span>

### <span data-ttu-id="3e8e8-200">System.String</span><span class="sxs-lookup"><span data-stu-id="3e8e8-200">System.String</span></span>

### <span data-ttu-id="3e8e8-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3e8e8-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3e8e8-202">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e8e8-202">OUTPUTS</span></span>

### <span data-ttu-id="3e8e8-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3e8e8-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3e8e8-204">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e8e8-204">NOTES</span></span>

## <span data-ttu-id="3e8e8-205">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e8e8-205">RELATED LINKS</span></span>
