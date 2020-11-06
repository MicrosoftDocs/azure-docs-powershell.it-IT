---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: bb21a7d69d6e2afa810b9df1bb2fa676b6568782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516640"
---
# <span data-ttu-id="0c2f7-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0c2f7-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="0c2f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2f7-103">Crea una nuova sottoscrizione di eventi della griglia di eventi di Azure a un argomento, una risorsa Azure, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c2f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c2f7-104">SYNTAX</span></span>

### <span data-ttu-id="0c2f7-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c2f7-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2f7-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c2f7-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2f7-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c2f7-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2f7-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c2f7-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2f7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2f7-109">DESCRIPTION</span></span>
<span data-ttu-id="0c2f7-110">Creare una nuova sottoscrizione di eventi a un argomento della griglia di eventi di Azure, una risorsa Azure supportata, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="0c2f7-111">Per creare un abbonamento a un evento all'abbonamento Azure selezionato, specificare il nome della sottoscrizione dell'evento e l'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0c2f7-112">Per creare un abbonamento a un gruppo di risorse, specificare il nome del gruppo di risorse oltre al nome della sottoscrizione dell'evento e all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0c2f7-113">Per creare un abbonamento a un evento di Azure Event Grid, specificare anche il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="0c2f7-114">Per creare un abbonamento a una risorsa Azure supportata, specificare l'ID risorsa completa della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="0c2f7-115">Per visualizzare l'elenco dei tipi supportati, eseguire il cmdlet Get-AzureRmEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="0c2f7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c2f7-116">EXAMPLES</span></span>

### <span data-ttu-id="0c2f7-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c2f7-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c2f7-118">Crea un nuovo abbonamento \` a EventSubscription1 \` a un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0c2f7-119">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c2f7-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c2f7-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c2f7-121">Crea un nuovo abbonamento \` \` a un evento EventSubscription1 a un gruppo di risorse \` MyResourceGroupName \` con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0c2f7-122">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c2f7-123">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0c2f7-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c2f7-124">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0c2f7-125">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c2f7-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="0c2f7-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="0c2f7-127">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'endpoint di destinazione webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0c2f7-128">Questo abbonamento agli eventi specifica i filtri aggiuntivi per i tipi di evento e l'oggetto e solo gli eventi che soddisfano tali filtri verranno recapitati all'endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="0c2f7-129">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="0c2f7-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="0c2f7-130">Crea un nuovo abbonamento \` a EventSubscription1 \` all'abbonamento Azure attualmente selezionato con l'hub eventi specificato come destinazione per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="0c2f7-131">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0c2f7-132">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="0c2f7-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0c2f7-133">Crea un nuovo evento \` di sottoscrizione \` di EventSubscription1 in uno spazio dei nomi EventHub con l'endpoint di destinazione webhhok specificato https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="0c2f7-134">Questo abbonamento agli eventi usa filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="0c2f7-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c2f7-135">PARAMETERS</span></span>

### <span data-ttu-id="0c2f7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2f7-136">-DefaultProfile</span></span>
<span data-ttu-id="0c2f7-137">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c2f7-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-138">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="0c2f7-138">-Endpoint</span></span>
<span data-ttu-id="0c2f7-139">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-139">Event subscription destination endpoint.</span></span>
<span data-ttu-id="0c2f7-140">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di un EventHub.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-140">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-141">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0c2f7-141">-EndpointType</span></span>
<span data-ttu-id="0c2f7-142">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-142">Endpoint Type.</span></span>
<span data-ttu-id="0c2f7-143">Può essere webhook o eventhub</span><span class="sxs-lookup"><span data-stu-id="0c2f7-143">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-144">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0c2f7-144">-EventSubscriptionName</span></span>
<span data-ttu-id="0c2f7-145">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="0c2f7-145">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-146">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="0c2f7-146">-IncludedEventType</span></span>
<span data-ttu-id="0c2f7-147">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-147">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2f7-148">-InputObject</span></span>
<span data-ttu-id="0c2f7-149">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-149">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-150">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="0c2f7-150">-Label</span></span>
<span data-ttu-id="0c2f7-151">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="0c2f7-151">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c2f7-152">-ResourceGroupName</span></span>
<span data-ttu-id="0c2f7-153">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-153">The resource group of the topic.</span></span>

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

### <span data-ttu-id="0c2f7-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c2f7-154">-ResourceId</span></span>
<span data-ttu-id="0c2f7-155">Identificatore della risorsa a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-155">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="0c2f7-156">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0c2f7-156">-SubjectBeginsWith</span></span>
<span data-ttu-id="0c2f7-157">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-157">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="0c2f7-158">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-158">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-159">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="0c2f7-159">-SubjectCaseSensitive</span></span>
<span data-ttu-id="0c2f7-160">Filter che specifica che il campo Subject deve essere confrontato in modo sensibile al caso.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-160">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="0c2f7-161">Se non specificato, l'oggetto verrà confrontato in modo senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-161">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="0c2f7-162">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="0c2f7-162">-SubjectEndsWith</span></span>
<span data-ttu-id="0c2f7-163">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-163">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="0c2f7-164">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-164">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f7-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0c2f7-165">-TopicName</span></span>
<span data-ttu-id="0c2f7-166">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-166">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="0c2f7-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c2f7-167">-Confirm</span></span>
<span data-ttu-id="0c2f7-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2f7-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2f7-169">-WhatIf</span></span>
<span data-ttu-id="0c2f7-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2f7-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2f7-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2f7-172">CommonParameters</span></span>
<span data-ttu-id="0c2f7-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2f7-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2f7-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2f7-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2f7-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c2f7-175">INPUTS</span></span>

### <span data-ttu-id="0c2f7-176">System. String</span><span class="sxs-lookup"><span data-stu-id="0c2f7-176">System.String</span></span>

### <span data-ttu-id="0c2f7-177">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0c2f7-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="0c2f7-178">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c2f7-178">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0c2f7-179">System. String []</span><span class="sxs-lookup"><span data-stu-id="0c2f7-179">System.String[]</span></span>

## <span data-ttu-id="0c2f7-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c2f7-180">OUTPUTS</span></span>

### <span data-ttu-id="0c2f7-181">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0c2f7-181">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0c2f7-182">Note</span><span class="sxs-lookup"><span data-stu-id="0c2f7-182">NOTES</span></span>

## <span data-ttu-id="0c2f7-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c2f7-183">RELATED LINKS</span></span>
