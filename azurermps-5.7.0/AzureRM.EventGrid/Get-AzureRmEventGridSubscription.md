---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: a6f821f094594fb00863f5dce2134f6702cfa8e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520458"
---
# <span data-ttu-id="08bef-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="08bef-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="08bef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08bef-102">SYNOPSIS</span></span>
<span data-ttu-id="08bef-103">Ottiene i dettagli di un abbonamento a un evento o ottiene un elenco di tutti gli abbonamenti agli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="08bef-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08bef-104">SYNTAX</span></span>

### <span data-ttu-id="08bef-105">EventSubscriptionTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08bef-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08bef-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="08bef-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08bef-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08bef-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08bef-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="08bef-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08bef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08bef-109">DESCRIPTION</span></span>
<span data-ttu-id="08bef-110">Il cmdlet Get-AzureRmEventGridSubscription ottiene i dettagli di un abbonamento alla griglia di eventi specificato o un elenco di tutti gli abbonamenti alla griglia degli eventi nel gruppo di risorse o dell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="08bef-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="08bef-111">Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di un singolo abbonamento alla griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="08bef-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="08bef-112">Se il nome dell'abbonamento all'evento non è disponibile, viene restituito un elenco di tutte le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="08bef-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="08bef-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08bef-113">EXAMPLES</span></span>

### <span data-ttu-id="08bef-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08bef-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08bef-115">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08bef-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08bef-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="08bef-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="08bef-117">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` , incluso l'URL completo dell'endpoint se si tratta di un abbonamento a un evento basato su webhook.</span><span class="sxs-lookup"><span data-stu-id="08bef-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="08bef-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="08bef-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="08bef-119">Ottenere un elenco di tutti gli abbonamenti agli eventi creati per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08bef-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08bef-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="08bef-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08bef-121">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08bef-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08bef-122">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="08bef-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="08bef-123">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'abbonamento Azure attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="08bef-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="08bef-124">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="08bef-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="08bef-125">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08bef-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08bef-126">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="08bef-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="08bef-127">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create sotto l'abbonamento Azure attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="08bef-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="08bef-128">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="08bef-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="08bef-129">Ottiene l'elenco di tutte le sottoscrizioni di eventi internazionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="08bef-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="08bef-130">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="08bef-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="08bef-131">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato.</span><span class="sxs-lookup"><span data-stu-id="08bef-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="08bef-132">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="08bef-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="08bef-133">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="08bef-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="08bef-134">Esempio 11</span><span class="sxs-lookup"><span data-stu-id="08bef-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="08bef-135">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="08bef-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="08bef-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08bef-136">PARAMETERS</span></span>

### <span data-ttu-id="08bef-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bef-137">-DefaultProfile</span></span>
<span data-ttu-id="08bef-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08bef-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="08bef-139">-EventSubscriptionName</span></span>
<span data-ttu-id="08bef-140">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="08bef-140">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="08bef-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="08bef-142">Includere l'URL completo dell'endpoint della destinazione dell'abbonamento agli eventi.</span><span class="sxs-lookup"><span data-stu-id="08bef-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08bef-143">-InputObject</span></span>
<span data-ttu-id="08bef-144">Oggetto sottoscrizione dell'evento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="08bef-144">EventGrid Event Subscription object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-145">-Posizione</span><span class="sxs-lookup"><span data-stu-id="08bef-145">-Location</span></span>
<span data-ttu-id="08bef-146">Posizione</span><span class="sxs-lookup"><span data-stu-id="08bef-146">Location</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08bef-147">-ResourceGroupName</span></span>
<span data-ttu-id="08bef-148">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08bef-148">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08bef-149">-ResourceId</span></span>
<span data-ttu-id="08bef-150">Identificatore della risorsa a cui sono stati creati gli abbonamenti agli eventi.</span><span class="sxs-lookup"><span data-stu-id="08bef-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="08bef-151">-TopicName</span></span>
<span data-ttu-id="08bef-152">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="08bef-152">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="08bef-153">-TopicTypeName</span></span>
<span data-ttu-id="08bef-154">Nome TopicType</span><span class="sxs-lookup"><span data-stu-id="08bef-154">TopicType name</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bef-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bef-155">CommonParameters</span></span>
<span data-ttu-id="08bef-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bef-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bef-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bef-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bef-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08bef-158">INPUTS</span></span>

### <span data-ttu-id="08bef-159">System. String</span><span class="sxs-lookup"><span data-stu-id="08bef-159">System.String</span></span>
<span data-ttu-id="08bef-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08bef-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08bef-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08bef-161">OUTPUTS</span></span>

### <span data-ttu-id="08bef-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="08bef-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="08bef-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscriptionListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="08bef-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="08bef-164">Note</span><span class="sxs-lookup"><span data-stu-id="08bef-164">NOTES</span></span>

## <span data-ttu-id="08bef-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08bef-165">RELATED LINKS</span></span>

