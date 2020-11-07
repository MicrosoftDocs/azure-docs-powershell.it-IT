---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: d036ba2df289b0b2f84430f01000632a887ec20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688120"
---
# <span data-ttu-id="7c086-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7c086-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="7c086-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c086-102">SYNOPSIS</span></span>
<span data-ttu-id="7c086-103">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7c086-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c086-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c086-104">SYNTAX</span></span>

### <span data-ttu-id="7c086-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c086-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c086-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c086-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c086-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c086-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c086-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c086-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c086-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c086-109">DESCRIPTION</span></span>
<span data-ttu-id="7c086-110">Aggiornare le proprietà di un abbonamento ad eventi griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7c086-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="7c086-111">Può essere usato per aggiornare il filtro, la destinazione o le etichette di un abbonamento a un evento esistente.</span><span class="sxs-lookup"><span data-stu-id="7c086-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="7c086-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c086-112">EXAMPLES</span></span>

### <span data-ttu-id="7c086-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c086-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="7c086-114">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="7c086-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="7c086-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c086-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="7c086-116">Aggiorna l'endpoint della sottoscrizione dell'evento \` ES1 \` per l'argomento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="7c086-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="7c086-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7c086-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="7c086-118">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per lo spazio dei nomi EventHub ContosoNamespace con il nuovo endpoint come \` https://requestb.in/1kxxoui1\ "e il nuovo filtro di SubjectEndsWith come \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="7c086-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="7c086-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7c086-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="7c086-120">Aggiorna le proprietà del ES1 della sottoscrizione dell'evento \` \` per il gruppo di risorse \` MyResourceGroupName \` con le nuove etichette $labels.</span><span class="sxs-lookup"><span data-stu-id="7c086-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="7c086-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c086-121">PARAMETERS</span></span>

### <span data-ttu-id="7c086-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c086-122">-DefaultProfile</span></span>
<span data-ttu-id="7c086-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c086-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c086-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7c086-124">-Endpoint</span></span>
<span data-ttu-id="7c086-125">Endpoint di destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7c086-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="7c086-126">Può trattarsi di un URL di Webhook o dell'ID delle risorse di Azure di un EventHub.</span><span class="sxs-lookup"><span data-stu-id="7c086-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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

### <span data-ttu-id="7c086-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="7c086-127">-EndpointType</span></span>
<span data-ttu-id="7c086-128">Tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="7c086-128">Endpoint Type.</span></span>
<span data-ttu-id="7c086-129">Può essere webhook o eventhub</span><span class="sxs-lookup"><span data-stu-id="7c086-129">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c086-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7c086-130">-EventSubscriptionName</span></span>
<span data-ttu-id="7c086-131">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="7c086-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="7c086-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="7c086-132">-IncludedEventType</span></span>
<span data-ttu-id="7c086-133">Filtro che specifica un elenco di tipi di evento da includere. Se non specificato, verranno inclusi tutti i tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="7c086-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="7c086-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c086-134">-InputObject</span></span>
<span data-ttu-id="7c086-135">Oggetto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7c086-135">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c086-136">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="7c086-136">-Label</span></span>
<span data-ttu-id="7c086-137">Etichette per l'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="7c086-137">Labels for the event subscription</span></span>

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

### <span data-ttu-id="7c086-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c086-138">-ResourceGroupName</span></span>
<span data-ttu-id="7c086-139">Gruppo di risorse dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="7c086-139">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c086-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c086-140">-ResourceId</span></span>
<span data-ttu-id="7c086-141">Identificatore della risorsa a cui è stato creato l'abbonamento all'evento.</span><span class="sxs-lookup"><span data-stu-id="7c086-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="7c086-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="7c086-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="7c086-143">Filter che specifica che verranno inclusi solo gli eventi corrispondenti al prefisso dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="7c086-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="7c086-144">Se non specificato, verranno inclusi gli eventi con tutti i prefissi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="7c086-144">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="7c086-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="7c086-145">-SubjectEndsWith</span></span>
<span data-ttu-id="7c086-146">Filter che specifica che verranno inclusi solo gli eventi che corrispondono al suffisso del soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="7c086-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="7c086-147">Se non specificato, verranno inclusi gli eventi con tutti i suffissi oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c086-147">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="7c086-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7c086-148">-TopicName</span></span>
<span data-ttu-id="7c086-149">Nome dell'argomento a cui deve essere creata la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7c086-149">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7c086-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c086-150">-Confirm</span></span>
<span data-ttu-id="7c086-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c086-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c086-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c086-152">-WhatIf</span></span>
<span data-ttu-id="7c086-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c086-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c086-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c086-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c086-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c086-155">CommonParameters</span></span>
<span data-ttu-id="7c086-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c086-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c086-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c086-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c086-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c086-158">INPUTS</span></span>

### <span data-ttu-id="7c086-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7c086-159">System.String</span></span>

### <span data-ttu-id="7c086-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7c086-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="7c086-161">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c086-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7c086-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c086-162">OUTPUTS</span></span>

### <span data-ttu-id="7c086-163">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7c086-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="7c086-164">Note</span><span class="sxs-lookup"><span data-stu-id="7c086-164">NOTES</span></span>

## <span data-ttu-id="7c086-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c086-165">RELATED LINKS</span></span>
