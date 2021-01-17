---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473924"
---
# <span data-ttu-id="09627-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="09627-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="09627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09627-102">SYNOPSIS</span></span>
<span data-ttu-id="09627-103">Ottiene i dettagli di un argomento della griglia di eventi o ottiene un elenco di tutti gli argomenti della griglia degli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="09627-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="09627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09627-104">SYNTAX</span></span>

### <span data-ttu-id="09627-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09627-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09627-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09627-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09627-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="09627-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09627-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="09627-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09627-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09627-109">DESCRIPTION</span></span>
<span data-ttu-id="09627-110">Il cmdlet Get-AzEventGridTopic ottiene i dettagli di un argomento della griglia di eventi specificato o un elenco di tutti gli argomenti della griglia eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="09627-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="09627-111">Se viene fornito il nome dell'argomento, vengono restituiti i dettagli di un singolo argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="09627-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="09627-112">Se il nome dell'argomento non è disponibile, viene restituito un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="09627-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="09627-113">Il numero di elementi restituiti in questo elenco è controllato dal parametro top.</span><span class="sxs-lookup"><span data-stu-id="09627-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="09627-114">Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="09627-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="09627-115">In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="09627-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="09627-116">Se sono ancora disponibili altri argomenti, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva di argomenti.</span><span class="sxs-lookup"><span data-stu-id="09627-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="09627-117">Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="09627-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="09627-118">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="09627-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="09627-119">Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="09627-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="09627-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09627-120">EXAMPLES</span></span>

### <span data-ttu-id="09627-121">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09627-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="09627-122">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="09627-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09627-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="09627-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="09627-124">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="09627-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09627-125">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="09627-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="09627-126">Elenca tutti gli argomenti della griglia degli eventi nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione.</span><span class="sxs-lookup"><span data-stu-id="09627-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="09627-127">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="09627-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="09627-128">Elencare i primi 10 argomenti della griglia degli eventi (se presenti) nel gruppo di risorse \` MyResourceGroupName \` che soddisfa la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="09627-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="09627-129">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="09627-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="09627-130">Per ottenere la pagina o le pagine successive degli argomenti, è previsto che l'utente richiami Get-AzEventGridTopic e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="09627-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="09627-131">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="09627-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="09627-132">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="09627-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="09627-133">Elenca tutti gli argomenti della griglia degli eventi nell'abbonamento senza paginazione.</span><span class="sxs-lookup"><span data-stu-id="09627-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="09627-134">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="09627-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="09627-135">Elencare i primi 10 argomenti della griglia degli eventi nell'abbonamento che soddisfano la query $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="09627-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="09627-136">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="09627-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="09627-137">Per ottenere la pagina o le pagine successive degli argomenti, è previsto che l'utente richiami Get-AzEventGridTopic e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="09627-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="09627-138">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="09627-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="09627-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09627-139">PARAMETERS</span></span>

### <span data-ttu-id="09627-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09627-140">-DefaultProfile</span></span>
<span data-ttu-id="09627-141">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09627-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09627-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="09627-142">-Name</span></span>
<span data-ttu-id="09627-143">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="09627-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09627-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="09627-144">-NextLink</span></span>
<span data-ttu-id="09627-145">Il collegamento per la pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="09627-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="09627-146">Questo valore viene ottenuto con la prima chiamata di cmdlet Get-AzEventGrid quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="09627-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="09627-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="09627-147">-ODataQuery</span></span>
<span data-ttu-id="09627-148">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="09627-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="09627-149">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="09627-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09627-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09627-150">-ResourceGroupName</span></span>
<span data-ttu-id="09627-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09627-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09627-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09627-152">-ResourceId</span></span>
<span data-ttu-id="09627-153">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="09627-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="09627-154">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="09627-154">-Top</span></span>
<span data-ttu-id="09627-155">Numero massimo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="09627-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="09627-156">Il valore valido è compreso tra 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="09627-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="09627-157">Se si specifica il valore superiore e sono ancora disponibili altri risultati, il risultato conterrà un collegamento alla pagina successiva in cui verrà eseguita una query in NextLink.</span><span class="sxs-lookup"><span data-stu-id="09627-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="09627-158">Se il valore superiore non è specificato, l'elenco completo delle risorse verrà restituito contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="09627-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09627-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09627-159">CommonParameters</span></span>
<span data-ttu-id="09627-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09627-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09627-161">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09627-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09627-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09627-162">INPUTS</span></span>

### <span data-ttu-id="09627-163">System. String</span><span class="sxs-lookup"><span data-stu-id="09627-163">System.String</span></span>

### <span data-ttu-id="09627-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09627-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09627-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09627-165">OUTPUTS</span></span>

### <span data-ttu-id="09627-166">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="09627-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="09627-167">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="09627-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="09627-168">Note</span><span class="sxs-lookup"><span data-stu-id="09627-168">NOTES</span></span>

## <span data-ttu-id="09627-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09627-169">RELATED LINKS</span></span>
