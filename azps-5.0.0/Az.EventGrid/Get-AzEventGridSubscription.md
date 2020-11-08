---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193430"
---
# <span data-ttu-id="a9629-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="a9629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9629-102">SYNOPSIS</span></span>
<span data-ttu-id="a9629-103">Ottiene i dettagli di un abbonamento a un evento o ottiene un elenco di tutti gli abbonamenti agli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a9629-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="a9629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9629-104">SYNTAX</span></span>

### <span data-ttu-id="a9629-105">EventSubscriptionTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9629-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9629-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9629-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9629-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9629-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9629-113">DESCRIPTION</span></span>
<span data-ttu-id="a9629-114">Il cmdlet Get-AzEventGridSubscription ottiene i dettagli di un abbonamento alla griglia di eventi specificato o un elenco di tutti gli abbonamenti alla griglia degli eventi nel gruppo di risorse o dell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a9629-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a9629-115">Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di un singolo abbonamento alla griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a9629-116">Se il nome dell'abbonamento all'evento non è disponibile, viene restituito un elenco di tutte le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="a9629-117">Il numero di elementi restituiti in questo elenco è controllato dal parametro top.</span><span class="sxs-lookup"><span data-stu-id="a9629-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="a9629-118">Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi dell'abbonamento agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="a9629-119">In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a9629-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="a9629-120">Se altre sottoscrizioni di eventi sono ancora disponibili, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva di abbonamenti a eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="a9629-121">Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="a9629-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="a9629-122">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="a9629-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="a9629-123">Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="a9629-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="a9629-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9629-124">EXAMPLES</span></span>

### <span data-ttu-id="a9629-125">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9629-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9629-126">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9629-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9629-127">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a9629-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a9629-128">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` , incluso l'URL completo dell'endpoint se si tratta di un abbonamento a un evento basato su webhook.</span><span class="sxs-lookup"><span data-stu-id="a9629-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a9629-129">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a9629-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a9629-130">Ottenere un elenco di tutti gli abbonamenti agli eventi creati per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a9629-131">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a9629-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-132">Elencare le prime 10 sottoscrizioni di eventi (se presenti) create per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-133">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-134">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-135">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-136">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="a9629-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9629-137">Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9629-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9629-138">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="a9629-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9629-139">Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'abbonamento Azure attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a9629-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a9629-140">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="a9629-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a9629-141">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a9629-142">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="a9629-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-143">Elencare le prime 5 sottoscrizioni di eventi (se presenti) create in MyResourceGroupName gruppo risorse \` \` che soddisfano la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-144">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-145">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-146">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-147">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="a9629-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="a9629-148">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nell'ambito dell'abbonamento Azure attualmente selezionato senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="a9629-149">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="a9629-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-150">Elencare le prime 15 sottoscrizioni di eventi globali create sotto l'abbonamento Azure attualmente selezionato che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-151">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-152">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-153">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-154">Esempio 11</span><span class="sxs-lookup"><span data-stu-id="a9629-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a9629-155">Ottiene l'elenco di tutte le sottoscrizioni di eventi internazionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="a9629-156">Esempio 12</span><span class="sxs-lookup"><span data-stu-id="a9629-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-157">Elencare le prime 15 sottoscrizioni di eventi regionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-158">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-159">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-160">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-161">Esempio 13</span><span class="sxs-lookup"><span data-stu-id="a9629-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a9629-162">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="a9629-163">Esempio 14</span><span class="sxs-lookup"><span data-stu-id="a9629-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-164">Elencare le prime 25 sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-165">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-166">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-167">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-168">Esempio 15</span><span class="sxs-lookup"><span data-stu-id="a9629-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a9629-169">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="a9629-170">Esempio 16</span><span class="sxs-lookup"><span data-stu-id="a9629-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-171">Elencare le prime 15 sottoscrizioni di eventi (se presenti) create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-172">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-173">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-174">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a9629-175">Esempio 17</span><span class="sxs-lookup"><span data-stu-id="a9629-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a9629-176">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="a9629-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="a9629-177">Esempio 18</span><span class="sxs-lookup"><span data-stu-id="a9629-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a9629-178">Elencare le prime sottoscrizioni di eventi di 100 (se presenti) create per il gruppo di risorse specifico che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="a9629-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a9629-179">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a9629-180">Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="a9629-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a9629-181">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="a9629-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="a9629-182">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9629-182">PARAMETERS</span></span>

### <span data-ttu-id="a9629-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9629-183">-DefaultProfile</span></span>
<span data-ttu-id="a9629-184">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a9629-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9629-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a9629-185">-DomainInputObject</span></span>
<span data-ttu-id="a9629-186">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a9629-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a9629-187">-DomainName</span></span>
<span data-ttu-id="a9629-188">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a9629-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="a9629-190">Oggetto argomento del dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="a9629-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a9629-191">-DomainTopicName</span></span>
<span data-ttu-id="a9629-192">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a9629-193">-EventSubscriptionName</span></span>
<span data-ttu-id="a9629-194">Nome dell'abbonamento a un evento</span><span class="sxs-lookup"><span data-stu-id="a9629-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a9629-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a9629-196">Includere l'URL completo dell'endpoint della destinazione dell'abbonamento agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9629-197">-InputObject</span></span>
<span data-ttu-id="a9629-198">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a9629-199">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a9629-199">-Location</span></span>
<span data-ttu-id="a9629-200">Posizione</span><span class="sxs-lookup"><span data-stu-id="a9629-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a9629-201">-NextLink</span></span>
<span data-ttu-id="a9629-202">Il collegamento per la pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a9629-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="a9629-203">Questo valore viene ottenuto con la prima chiamata di cmdlet Get-AzEventGrid quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="a9629-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a9629-204">-ODataQuery</span></span>
<span data-ttu-id="a9629-205">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a9629-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a9629-206">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="a9629-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9629-207">-ResourceGroupName</span></span>
<span data-ttu-id="a9629-208">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9629-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9629-209">-ResourceId</span></span>
<span data-ttu-id="a9629-210">Identificatore della risorsa a cui sono stati creati gli abbonamenti agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a9629-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="a9629-211">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="a9629-211">-Top</span></span>
<span data-ttu-id="a9629-212">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a9629-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a9629-213">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="a9629-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a9629-214">-TopicName</span></span>
<span data-ttu-id="a9629-215">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9629-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a9629-216">-TopicTypeName</span></span>
<span data-ttu-id="a9629-217">Nome TopicType</span><span class="sxs-lookup"><span data-stu-id="a9629-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9629-218">CommonParameters</span></span>
<span data-ttu-id="a9629-219">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9629-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9629-220">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9629-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9629-221">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9629-221">INPUTS</span></span>

### <span data-ttu-id="a9629-222">System. String</span><span class="sxs-lookup"><span data-stu-id="a9629-222">System.String</span></span>

### <span data-ttu-id="a9629-223">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a9629-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a9629-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="a9629-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a9629-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a9629-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="a9629-226">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9629-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a9629-227">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9629-227">OUTPUTS</span></span>

### <span data-ttu-id="a9629-228">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a9629-229">Note</span><span class="sxs-lookup"><span data-stu-id="a9629-229">NOTES</span></span>

## <span data-ttu-id="a9629-230">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9629-230">RELATED LINKS</span></span>
