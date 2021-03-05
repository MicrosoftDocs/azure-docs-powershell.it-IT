---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 053c9a503b6cb7d3833d214208ae7fe6bd60fe45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984659"
---
# <span data-ttu-id="62d73-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="62d73-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="62d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62d73-102">SYNOPSIS</span></span>
<span data-ttu-id="62d73-103">Recupera i dettagli di un argomento relativo al dominio della griglia eventi o ottiene un elenco di tutti gli argomenti di dominio della griglia eventi in uno specifico dominio della griglia eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="62d73-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="62d73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62d73-104">SYNTAX</span></span>

### <span data-ttu-id="62d73-105">DomainTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62d73-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62d73-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d73-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62d73-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d73-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62d73-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62d73-108">DESCRIPTION</span></span>
<span data-ttu-id="62d73-109">Il cmdlet Get-AzEventGridDomainTopic ottiene i dettagli di un argomento di dominio della griglia eventi specificato oppure un elenco di tutti gli argomenti di dominio della griglia eventi per un dominio specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="62d73-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="62d73-110">Se si fornisce il nome dell'argomento dominio, vengono restituiti i dettagli di un singolo argomento Dominio griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="62d73-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="62d73-111">Se non viene fornito il nome dell'argomento relativo al dominio, viene restituito un elenco di argomenti di dominio sotto il nome di dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="62d73-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="62d73-112">Il numero di elementi restituiti in questo elenco è controllato dal parametro Top.</span><span class="sxs-lookup"><span data-stu-id="62d73-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="62d73-113">Se non si specificato il valore Massimo o $null, l'elenco conterrà tutti gli elementi degli argomenti di dominio.</span><span class="sxs-lookup"><span data-stu-id="62d73-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="62d73-114">In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="62d73-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="62d73-115">Se sono ancora disponibili altri argomenti sul dominio, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva di argomenti sul dominio.</span><span class="sxs-lookup"><span data-stu-id="62d73-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="62d73-116">Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="62d73-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="62d73-117">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="62d73-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="62d73-118">Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="62d73-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="62d73-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62d73-119">EXAMPLES</span></span>

### <span data-ttu-id="62d73-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62d73-120">Example 1</span></span>

<span data-ttu-id="62d73-121">Recupera i dettagli dell'argomento dominio Griglia eventi DomainTopic1 in Domain1 della griglia eventi nel gruppo di \` \` risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="62d73-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="62d73-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="62d73-122">Example 2</span></span>

<span data-ttu-id="62d73-123">Recupera i dettagli dell'argomento dominio Griglia eventi DomainTopic1 in Domain1 della griglia eventi nel gruppo di risorse \` \` \` MyResourceGroupName usando \` \` l'opzione \` ResourceId.</span><span class="sxs-lookup"><span data-stu-id="62d73-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="62d73-124">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="62d73-124">Example 3</span></span>

<span data-ttu-id="62d73-125">Elencare tutti gli argomenti di dominio della griglia eventi in Domain1 della griglia eventi nel gruppo di risorse MyResourceGroupName senza impaginazione (tutti i risultati vengono restituiti \` \` in \` \` un'unica schermata).</span><span class="sxs-lookup"><span data-stu-id="62d73-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="62d73-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="62d73-126">Example 4</span></span>

<span data-ttu-id="62d73-127">Elencare tutti gli argomenti sui domini della griglia eventi in Dominio griglia eventi1 nel gruppo di risorse \` \` MyResourceGroupName senza impaginazione (tutti i risultati vengono restituiti in un'unica schermata) usando l'opzione \` \` ResourceId</span><span class="sxs-lookup"><span data-stu-id="62d73-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="62d73-128">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="62d73-128">Example 5</span></span>

<span data-ttu-id="62d73-129">Elencare gli eventuali argomenti sui domini della griglia eventi in Dominio1 nel gruppo di risorse MyResourceGroupName che soddisfano gli argomenti di dominio \` \` della query $odataFilter \` \` 10 per volta.</span><span class="sxs-lookup"><span data-stu-id="62d73-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="62d73-130">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="62d73-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="62d73-131">Per ottenere le pagine seguenti di argomenti sul dominio, è previsto che l'utente chiami di nuovo il Get-AzEventGridDomainTopic e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="62d73-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="62d73-132">Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="62d73-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="62d73-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62d73-133">PARAMETERS</span></span>

### <span data-ttu-id="62d73-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d73-134">-DefaultProfile</span></span>
<span data-ttu-id="62d73-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62d73-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d73-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="62d73-136">-DomainName</span></span>
<span data-ttu-id="62d73-137">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="62d73-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="62d73-138">-Name</span><span class="sxs-lookup"><span data-stu-id="62d73-138">-Name</span></span>
<span data-ttu-id="62d73-139">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="62d73-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="62d73-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="62d73-140">-NextLink</span></span>
<span data-ttu-id="62d73-141">Collegamento alla pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="62d73-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="62d73-142">Questo valore viene ottenuto con la prima chiamata Get-AzEventGrid cmdlet quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="62d73-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="62d73-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="62d73-143">-ODataQuery</span></span>
<span data-ttu-id="62d73-144">Query OData usata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="62d73-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="62d73-145">L'applicazione di filtri è attualmente consentita solo per la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="62d73-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="62d73-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d73-146">-ResourceGroupName</span></span>
<span data-ttu-id="62d73-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62d73-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="62d73-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62d73-148">-ResourceId</span></span>
<span data-ttu-id="62d73-149">Identificatore di risorsa che rappresenta l'argomento Dominio griglia eventi o Dominio griglia.</span><span class="sxs-lookup"><span data-stu-id="62d73-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="62d73-150">-In alto</span><span class="sxs-lookup"><span data-stu-id="62d73-150">-Top</span></span>
<span data-ttu-id="62d73-151">Query OData usata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="62d73-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="62d73-152">L'applicazione di filtri è attualmente consentita solo per la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="62d73-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="62d73-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d73-153">CommonParameters</span></span>
<span data-ttu-id="62d73-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d73-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d73-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62d73-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d73-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="62d73-156">INPUTS</span></span>

### <span data-ttu-id="62d73-157">System.String</span><span class="sxs-lookup"><span data-stu-id="62d73-157">System.String</span></span>

### <span data-ttu-id="62d73-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="62d73-158">System.Int32</span></span>

## <span data-ttu-id="62d73-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62d73-159">OUTPUTS</span></span>

### <span data-ttu-id="62d73-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="62d73-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="62d73-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="62d73-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="62d73-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="62d73-162">NOTES</span></span>

## <span data-ttu-id="62d73-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62d73-163">RELATED LINKS</span></span>
