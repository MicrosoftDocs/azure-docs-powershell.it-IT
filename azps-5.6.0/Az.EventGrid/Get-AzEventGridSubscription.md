---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991365"
---
# <span data-ttu-id="5c9cf-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5c9cf-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="5c9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9cf-103">Recupera i dettagli di una sottoscrizione di evento o ottiene un elenco di tutte le sottoscrizioni di eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="5c9cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c9cf-104">SYNTAX</span></span>

### <span data-ttu-id="5c9cf-105">EventSubscriptionTopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c9cf-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c9cf-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9cf-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c9cf-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c9cf-113">DESCRIPTION</span></span>
<span data-ttu-id="5c9cf-114">Il cmdlet Get-AzEventGridSubscription cmdlet ottiene i dettagli di una sottoscrizione specificata di Griglia eventi oppure un elenco di tutte le sottoscrizioni della griglia eventi nella sottoscrizione o nel gruppo di risorse corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="5c9cf-115">Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di una singola sottoscrizione a Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="5c9cf-116">Se il nome della sottoscrizione dell'evento non è specificato, viene restituito un elenco di tutte le sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="5c9cf-117">Il numero di elementi restituiti in questo elenco è controllato dal parametro Top.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="5c9cf-118">Se non si specificato il valore Massimo o $null, l'elenco conterrà tutte le voci di sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="5c9cf-119">In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="5c9cf-120">Se sono ancora disponibili più abbonamenti a eventi, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva delle sottoscrizioni degli eventi.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="5c9cf-121">Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="5c9cf-122">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="5c9cf-123">Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="5c9cf-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c9cf-124">EXAMPLES</span></span>

### <span data-ttu-id="5c9cf-125">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c9cf-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5c9cf-126">Recupera i dettagli della sottoscrizione evento EventSubscription1 creata per l'argomento 1 nel gruppo \` \` di risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="5c9cf-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5c9cf-127">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5c9cf-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="5c9cf-128">Recupera i dettagli della sottoscrizione dell'evento EventSubscription1 creata per argomento1 nel gruppo di risorse \` \` \` \` MyResourceGroupName, incluso l'URL completo dell'endpoint se si tratta di una sottoscrizione a un evento basata \` \` su Webhook.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="5c9cf-129">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5c9cf-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="5c9cf-130">Ottenere un elenco di tutte le sottoscrizioni di eventi create per argomento1 nel gruppo \` \` di risorse \` MyResourceGroupName \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="5c9cf-131">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="5c9cf-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-132">Elencare le prime 10 sottoscrizioni degli eventi , se presenti, create per argomento1 nel gruppo di risorse \` \` MyResourceGroupName che soddisfa la \` \` query $odataFilter risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-133">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-134">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-135">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-136">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="5c9cf-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5c9cf-137">Recupera i dettagli della sottoscrizione evento \` EventSubscription1 \` creata per il gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="5c9cf-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5c9cf-138">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="5c9cf-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5c9cf-139">Recupera i dettagli della sottoscrizione evento \` EventSubscription1 \` creata per la sottoscrizione di Azure attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="5c9cf-140">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="5c9cf-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5c9cf-141">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="5c9cf-142">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="5c9cf-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-143">Elencare i primi cinque abbonamenti a eventi (se presenti) creati nel gruppo di risorse MyResourceGroupName che soddisfa la \` \` query $odataFilter risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-144">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-145">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo il Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-146">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-147">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="5c9cf-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="5c9cf-148">Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nella sottoscrizione di Azure attualmente selezionata senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="5c9cf-149">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="5c9cf-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-150">Elencare le prime 15 sottoscrizioni di eventi globali (se presenti) create nella sottoscrizione di Azure attualmente selezionata che soddisfa la query $odataFilter globale.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-151">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-152">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-153">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-154">Esempio 11</span><span class="sxs-lookup"><span data-stu-id="5c9cf-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="5c9cf-155">Ottiene l'elenco di tutte le sottoscrizioni di eventi locali create nel gruppo di risorse MyResourceGroupName nella posizione specificata \` \` \` westus2 \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="5c9cf-156">Esempio 12</span><span class="sxs-lookup"><span data-stu-id="5c9cf-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-157">Elencare le prime 15 sottoscrizioni di eventi locali (se presenti) create nel gruppo di risorse MyResourceGroupName nel percorso specificato westus2 che soddisfa la \` \` query $odataFilter \` \` risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-158">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-159">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-160">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-161">Esempio 13</span><span class="sxs-lookup"><span data-stu-id="5c9cf-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="5c9cf-162">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="5c9cf-163">Esempio 14</span><span class="sxs-lookup"><span data-stu-id="5c9cf-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-164">Elencare i primi 25 abbonamenti a eventi , se presenti, creati per lo spazio dei nomi EventHub specificato che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-165">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-166">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-167">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-168">Esempio 15</span><span class="sxs-lookup"><span data-stu-id="5c9cf-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="5c9cf-169">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="5c9cf-170">Esempio 16</span><span class="sxs-lookup"><span data-stu-id="5c9cf-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-171">Elencare i primi 15 abbonamenti a eventi, se presenti, creati per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata che soddisfa la query $odataFilter specificata.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-172">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-173">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-174">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5c9cf-175">Esempio 17</span><span class="sxs-lookup"><span data-stu-id="5c9cf-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5c9cf-176">Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="5c9cf-177">Esempio 18</span><span class="sxs-lookup"><span data-stu-id="5c9cf-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="5c9cf-178">Elencare i primi 100 abbonamenti a eventi, se presenti, creati per il gruppo di risorse specifico che soddisfa la query $odataFilter risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5c9cf-179">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5c9cf-180">Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5c9cf-181">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="5c9cf-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c9cf-182">PARAMETERS</span></span>

### <span data-ttu-id="5c9cf-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9cf-183">-DefaultProfile</span></span>
<span data-ttu-id="5c9cf-184">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5c9cf-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c9cf-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="5c9cf-185">-DomainInputObject</span></span>
<span data-ttu-id="5c9cf-186">Oggetto Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="5c9cf-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-187">-DomainName</span></span>
<span data-ttu-id="5c9cf-188">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="5c9cf-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="5c9cf-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="5c9cf-190">Oggetto Domain Topic di EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="5c9cf-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-191">-DomainTopicName</span></span>
<span data-ttu-id="5c9cf-192">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="5c9cf-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-193">-EventSubscriptionName</span></span>
<span data-ttu-id="5c9cf-194">Nome della sottoscrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="5c9cf-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="5c9cf-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5c9cf-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="5c9cf-196">Includere l'URL completo dell'endpoint della destinazione della sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="5c9cf-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c9cf-197">-InputObject</span></span>
<span data-ttu-id="5c9cf-198">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5c9cf-199">-Location</span><span class="sxs-lookup"><span data-stu-id="5c9cf-199">-Location</span></span>
<span data-ttu-id="5c9cf-200">Posizione</span><span class="sxs-lookup"><span data-stu-id="5c9cf-200">Location</span></span>

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

### <span data-ttu-id="5c9cf-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="5c9cf-201">-NextLink</span></span>
<span data-ttu-id="5c9cf-202">Collegamento alla pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="5c9cf-203">Questo valore viene ottenuto con la prima chiamata Get-AzEventGrid cmdlet quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="5c9cf-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5c9cf-204">-ODataQuery</span></span>
<span data-ttu-id="5c9cf-205">Query OData usata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="5c9cf-206">L'applicazione di filtri è attualmente consentita solo per la proprietà Nome. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="5c9cf-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-207">-ResourceGroupName</span></span>
<span data-ttu-id="5c9cf-208">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c9cf-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c9cf-209">-ResourceId</span></span>
<span data-ttu-id="5c9cf-210">Identificatore della risorsa per cui sono state create le sottoscrizioni degli eventi.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="5c9cf-211">-In alto</span><span class="sxs-lookup"><span data-stu-id="5c9cf-211">-Top</span></span>
<span data-ttu-id="5c9cf-212">Query OData usata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="5c9cf-213">L'applicazione di filtri è attualmente consentita solo per la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="5c9cf-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-214">-TopicName</span></span>
<span data-ttu-id="5c9cf-215">Nome dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="5c9cf-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="5c9cf-216">-TopicTypeName</span></span>
<span data-ttu-id="5c9cf-217">Nome TopicType</span><span class="sxs-lookup"><span data-stu-id="5c9cf-217">TopicType name</span></span>

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

### <span data-ttu-id="5c9cf-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9cf-218">CommonParameters</span></span>
<span data-ttu-id="5c9cf-219">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9cf-220">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c9cf-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9cf-221">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c9cf-221">INPUTS</span></span>

### <span data-ttu-id="5c9cf-222">System.String</span><span class="sxs-lookup"><span data-stu-id="5c9cf-222">System.String</span></span>

### <span data-ttu-id="5c9cf-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="5c9cf-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="5c9cf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="5c9cf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="5c9cf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5c9cf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="5c9cf-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5c9cf-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5c9cf-227">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c9cf-227">OUTPUTS</span></span>

### <span data-ttu-id="5c9cf-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="5c9cf-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="5c9cf-229">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c9cf-229">NOTES</span></span>

## <span data-ttu-id="5c9cf-230">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c9cf-230">RELATED LINKS</span></span>
