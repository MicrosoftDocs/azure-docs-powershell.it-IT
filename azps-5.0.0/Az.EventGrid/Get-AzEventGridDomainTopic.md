---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193433"
---
# <span data-ttu-id="fc6b2-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fc6b2-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="fc6b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6b2-103">Ottiene i dettagli di un argomento relativo al dominio della griglia di eventi oppure ottiene un elenco di tutti gli argomenti relativi al dominio della griglia eventi in un dominio specifico della griglia di eventi nell'abbonamento a Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="fc6b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc6b2-104">SYNTAX</span></span>

### <span data-ttu-id="fc6b2-105">DomainTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc6b2-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc6b2-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc6b2-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc6b2-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc6b2-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc6b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc6b2-108">DESCRIPTION</span></span>
<span data-ttu-id="fc6b2-109">Il cmdlet Get-AzEventGridDomainTopic ottiene i dettagli di un argomento del dominio della griglia di eventi specificato o un elenco di tutti gli argomenti relativi al dominio della griglia di eventi in un dominio specifico dell'abbonamento a Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="fc6b2-110">Se viene fornito il nome dell'argomento di dominio, vengono restituiti i dettagli di un singolo argomento relativo al dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="fc6b2-111">Se il nome dell'argomento del dominio non è disponibile, viene restituito un elenco di argomenti del dominio con il nome di dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="fc6b2-112">Il numero di elementi restituiti in questo elenco è controllato dal parametro top.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="fc6b2-113">Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi del dominio.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="fc6b2-114">In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="fc6b2-115">Se sono ancora disponibili altri argomenti di dominio, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva di argomenti di dominio.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="fc6b2-116">Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="fc6b2-117">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="fc6b2-118">Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="fc6b2-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc6b2-119">EXAMPLES</span></span>

### <span data-ttu-id="fc6b2-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc6b2-120">Example 1</span></span>

<span data-ttu-id="fc6b2-121">Ottiene i dettagli dell'argomento relativo al dominio della griglia dell'evento \` DomainTopic1 \` in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fc6b2-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="fc6b2-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fc6b2-122">Example 2</span></span>

<span data-ttu-id="fc6b2-123">Ottiene i dettagli dell'argomento relativo al dominio della griglia dell'evento \` DomainTopic1 in \` Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` usando l'opzione ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="fc6b2-124">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fc6b2-124">Example 3</span></span>

<span data-ttu-id="fc6b2-125">Elenca tutti gli argomenti relativi al dominio della griglia eventi in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione (tutti i risultati vengono restituiti in un solo colpo).</span><span class="sxs-lookup"><span data-stu-id="fc6b2-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="fc6b2-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="fc6b2-126">Example 4</span></span>

<span data-ttu-id="fc6b2-127">Elenca tutti gli argomenti relativi al dominio della griglia eventi in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione (tutti i risultati vengono restituiti in un solo colpo) usando l'opzione ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6b2-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="fc6b2-128">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="fc6b2-128">Example 5</span></span>

<span data-ttu-id="fc6b2-129">Elencare gli argomenti relativi al dominio della griglia degli eventi in Domain \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` che soddisfano gli argomenti di $odataFilter query 10 Domain alla volta.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="fc6b2-130">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="fc6b2-131">Per ottenere la pagina o le pagine successive degli argomenti di dominio, si prevede che l'utente richiami Get-AzEventGridDomainTopic e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="fc6b2-132">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="fc6b2-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc6b2-133">PARAMETERS</span></span>

### <span data-ttu-id="fc6b2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6b2-134">-DefaultProfile</span></span>
<span data-ttu-id="fc6b2-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc6b2-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fc6b2-136">-DomainName</span></span>
<span data-ttu-id="fc6b2-137">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc6b2-138">-Name</span></span>
<span data-ttu-id="fc6b2-139">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="fc6b2-140">-NextLink</span></span>
<span data-ttu-id="fc6b2-141">Il collegamento per la pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="fc6b2-142">Questo valore viene ottenuto con la prima chiamata di cmdlet Get-AzEventGrid quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="fc6b2-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fc6b2-143">-ODataQuery</span></span>
<span data-ttu-id="fc6b2-144">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="fc6b2-145">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc6b2-146">-ResourceGroupName</span></span>
<span data-ttu-id="fc6b2-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6b2-148">-ResourceId</span></span>
<span data-ttu-id="fc6b2-149">Identificatore delle risorse che rappresenta il dominio dell'evento Grid o Domain Grid.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-150">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="fc6b2-150">-Top</span></span>
<span data-ttu-id="fc6b2-151">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="fc6b2-152">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6b2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6b2-153">CommonParameters</span></span>
<span data-ttu-id="fc6b2-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6b2-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc6b2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6b2-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc6b2-156">INPUTS</span></span>

### <span data-ttu-id="fc6b2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="fc6b2-157">System.String</span></span>

### <span data-ttu-id="fc6b2-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fc6b2-158">System.Int32</span></span>

## <span data-ttu-id="fc6b2-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc6b2-159">OUTPUTS</span></span>

### <span data-ttu-id="fc6b2-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fc6b2-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="fc6b2-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="fc6b2-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="fc6b2-162">Note</span><span class="sxs-lookup"><span data-stu-id="fc6b2-162">NOTES</span></span>

## <span data-ttu-id="fc6b2-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc6b2-163">RELATED LINKS</span></span>
