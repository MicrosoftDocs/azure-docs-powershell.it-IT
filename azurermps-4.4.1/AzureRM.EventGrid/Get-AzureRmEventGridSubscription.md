---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 26e306c80f18f3e7d14ca073cfdedfbdc9e6567b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686841"
---
# <span data-ttu-id="a1b07-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a1b07-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="a1b07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1b07-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b07-103">Ottiene i dettagli di un abbonamento a un evento o ottiene un elenco di tutti gli abbonamenti agli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a1b07-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b07-104">SYNTAX</span></span>

### <span data-ttu-id="a1b07-105">EventSubscriptionTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1b07-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b07-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b07-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b07-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b07-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b07-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1b07-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b07-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b07-109">DESCRIPTION</span></span>
<span data-ttu-id="a1b07-110">Il cmdlet Get-AzureRmEventGridSubscription ottiene i dettagli di un abbonamento alla griglia di eventi specificato o un elenco di tutti gli abbonamenti alla griglia degli eventi nel gruppo di risorse o dell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a1b07-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a1b07-111">Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di un singolo abbonamento alla griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="a1b07-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a1b07-112">Se il nome dell'abbonamento all'evento non è disponibile, viene restituito un elenco di tutte le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="a1b07-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="a1b07-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b07-113">EXAMPLES</span></span>

### <span data-ttu-id="a1b07-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1b07-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a1b07-115">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a1b07-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a1b07-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a1b07-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a1b07-117">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` , incluso l'URL completo dell'endpoint se si tratta di un abbonamento a un evento basato su webhook.</span><span class="sxs-lookup"><span data-stu-id="a1b07-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a1b07-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a1b07-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a1b07-119">Ottenere un elenco di tutti gli abbonamenti agli eventi creati per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a1b07-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a1b07-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a1b07-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a1b07-121">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a1b07-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a1b07-122">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="a1b07-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a1b07-123">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'abbonamento Azure attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a1b07-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a1b07-124">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="a1b07-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a1b07-125">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a1b07-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a1b07-126">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="a1b07-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="a1b07-127">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create sotto l'abbonamento Azure attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a1b07-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a1b07-128">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="a1b07-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a1b07-129">Ottiene l'elenco di tutte le sottoscrizioni di eventi internazionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="a1b07-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="a1b07-130">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="a1b07-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a1b07-131">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato.</span><span class="sxs-lookup"><span data-stu-id="a1b07-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="a1b07-132">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="a1b07-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a1b07-133">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a1b07-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="a1b07-134">Esempio 11</span><span class="sxs-lookup"><span data-stu-id="a1b07-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a1b07-135">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="a1b07-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="a1b07-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1b07-136">PARAMETERS</span></span>

### <span data-ttu-id="a1b07-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a1b07-137">-EventSubscriptionName</span></span>
<span data-ttu-id="a1b07-138">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="a1b07-138">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-139">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a1b07-139">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a1b07-140">Includere l'URL completo dell'endpoint della destinazione dell'abbonamento agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a1b07-140">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1b07-141">-InputObject</span></span>
<span data-ttu-id="a1b07-142">Oggetto sottoscrizione dell'evento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a1b07-142">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="a1b07-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a1b07-143">-Location</span></span>
<span data-ttu-id="a1b07-144">Posizione</span><span class="sxs-lookup"><span data-stu-id="a1b07-144">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b07-145">-ResourceGroupName</span></span>
<span data-ttu-id="a1b07-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1b07-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b07-147">-ResourceId</span></span>
<span data-ttu-id="a1b07-148">Identificatore della risorsa a cui sono stati creati gli abbonamenti agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a1b07-148">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a1b07-149">-TopicName</span></span>
<span data-ttu-id="a1b07-150">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a1b07-150">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-151">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a1b07-151">-TopicTypeName</span></span>
<span data-ttu-id="a1b07-152">Nome TopicType</span><span class="sxs-lookup"><span data-stu-id="a1b07-152">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b07-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b07-153">-DefaultProfile</span></span>
<span data-ttu-id="a1b07-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b07-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b07-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b07-155">CommonParameters</span></span>
<span data-ttu-id="a1b07-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b07-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b07-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b07-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b07-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1b07-158">INPUTS</span></span>

### <span data-ttu-id="a1b07-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b07-159">System.String</span></span>
<span data-ttu-id="a1b07-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1b07-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1b07-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b07-161">OUTPUTS</span></span>

### <span data-ttu-id="a1b07-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a1b07-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="a1b07-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscriptionListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a1b07-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a1b07-164">Note</span><span class="sxs-lookup"><span data-stu-id="a1b07-164">NOTES</span></span>

## <span data-ttu-id="a1b07-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b07-165">RELATED LINKS</span></span>

