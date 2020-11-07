---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: f2f3c3799ff16cdcc5f1091f8a66cb531cf46cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864497"
---
# <span data-ttu-id="38aac-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="38aac-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="38aac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38aac-102">SYNOPSIS</span></span>
<span data-ttu-id="38aac-103">Ottiene i dettagli di un dominio della griglia di eventi o ottiene un elenco di tutti i domini della griglia di eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="38aac-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="38aac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38aac-104">SYNTAX</span></span>

### <span data-ttu-id="38aac-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38aac-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38aac-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38aac-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38aac-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="38aac-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38aac-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="38aac-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38aac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38aac-109">DESCRIPTION</span></span>
<span data-ttu-id="38aac-110">Il cmdlet Get-AzEventGridDomain ottiene i dettagli di un dominio della griglia di eventi specificato o un elenco di tutti i domini della griglia di eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="38aac-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="38aac-111">Se viene fornito il nome di dominio, vengono restituiti i dettagli di un singolo dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="38aac-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="38aac-112">Se il nome di dominio non è disponibile, viene restituito un elenco di domini.</span><span class="sxs-lookup"><span data-stu-id="38aac-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="38aac-113">Il numero di elementi restituiti in questo elenco è controllato dal parametro top.</span><span class="sxs-lookup"><span data-stu-id="38aac-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="38aac-114">Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi di domini restituiti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="38aac-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="38aac-115">In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="38aac-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="38aac-116">Se sono ancora disponibili più domini, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva dei domini.</span><span class="sxs-lookup"><span data-stu-id="38aac-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="38aac-117">Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="38aac-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="38aac-118">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="38aac-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="38aac-119">Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="38aac-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="38aac-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38aac-120">EXAMPLES</span></span>

### <span data-ttu-id="38aac-121">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38aac-121">Example 1</span></span>

<span data-ttu-id="38aac-122">Ottiene i dettagli del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="38aac-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="38aac-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38aac-123">Example 2</span></span>

<span data-ttu-id="38aac-124">Ottiene i dettagli del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` usando l'opzione ResourceId.</span><span class="sxs-lookup"><span data-stu-id="38aac-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="38aac-125">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="38aac-125">Example 3</span></span>

<span data-ttu-id="38aac-126">Elenca tutti i domini della griglia degli eventi nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione (tutti i domini vengono restituiti in un solo colpo)</span><span class="sxs-lookup"><span data-stu-id="38aac-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="38aac-127">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="38aac-127">Example 4</span></span>

<span data-ttu-id="38aac-128">Elencare i domini della griglia dell'evento (se presenti) nel gruppo di risorse \` MyResourceGroupName \` che soddisfa la $odataFilter query 10 domini alla volta.</span><span class="sxs-lookup"><span data-stu-id="38aac-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="38aac-129">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="38aac-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="38aac-130">Per ottenere la pagina o le pagine successive dei domini, è previsto che l'utente richiami Get-AzEventGridDomain e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="38aac-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="38aac-131">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="38aac-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="38aac-132">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="38aac-132">Example 5</span></span>

<span data-ttu-id="38aac-133">Elenca tutti i domini griglia eventi in abbonamento a Azure senza impaginazione (tutti i domini vengono restituiti in un solo colpo)</span><span class="sxs-lookup"><span data-stu-id="38aac-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="38aac-134">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="38aac-134">Example 6</span></span>

<span data-ttu-id="38aac-135">Elencare i domini della griglia dell'evento, se presenti, in abbonamento a Azure che soddisfano la $odataFilter query di 20 domini alla volta.</span><span class="sxs-lookup"><span data-stu-id="38aac-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="38aac-136">Se sono disponibili più risultati, la $result. NextLink non sarà $null.</span><span class="sxs-lookup"><span data-stu-id="38aac-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="38aac-137">Per ottenere la pagina o le pagine successive dei domini, è previsto che l'utente richiami Get-AzEventGridDomain e usi result. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="38aac-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="38aac-138">Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="38aac-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="38aac-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38aac-139">PARAMETERS</span></span>

### <span data-ttu-id="38aac-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38aac-140">-DefaultProfile</span></span>
<span data-ttu-id="38aac-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38aac-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38aac-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="38aac-142">-Name</span></span>
<span data-ttu-id="38aac-143">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="38aac-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38aac-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="38aac-144">-NextLink</span></span>
<span data-ttu-id="38aac-145">Il collegamento per la pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="38aac-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="38aac-146">Questo valore viene ottenuto con la prima chiamata di cmdlet Get-AzEventGrid quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="38aac-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38aac-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="38aac-147">-ODataQuery</span></span>
<span data-ttu-id="38aac-148">Query OData utilizzata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="38aac-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="38aac-149">Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.</span><span class="sxs-lookup"><span data-stu-id="38aac-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38aac-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38aac-150">-ResourceGroupName</span></span>
<span data-ttu-id="38aac-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38aac-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38aac-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38aac-152">-ResourceId</span></span>
<span data-ttu-id="38aac-153">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="38aac-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="38aac-154">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="38aac-154">-Top</span></span>
<span data-ttu-id="38aac-155">Numero massimo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="38aac-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="38aac-156">Il valore valido è compreso tra 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="38aac-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="38aac-157">Se si specifica il valore superiore e sono ancora disponibili altri risultati, il risultato conterrà un collegamento alla pagina successiva in cui verrà eseguita una query in NextLink.</span><span class="sxs-lookup"><span data-stu-id="38aac-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="38aac-158">Se il valore superiore non è specificato, l'elenco completo delle risorse verrà restituito contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="38aac-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38aac-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38aac-159">CommonParameters</span></span>
<span data-ttu-id="38aac-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38aac-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38aac-161">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38aac-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38aac-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38aac-162">INPUTS</span></span>

### <span data-ttu-id="38aac-163">System. String</span><span class="sxs-lookup"><span data-stu-id="38aac-163">System.String</span></span>

## <span data-ttu-id="38aac-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38aac-164">OUTPUTS</span></span>

### <span data-ttu-id="38aac-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="38aac-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="38aac-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="38aac-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="38aac-167">Note</span><span class="sxs-lookup"><span data-stu-id="38aac-167">NOTES</span></span>

## <span data-ttu-id="38aac-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38aac-168">RELATED LINKS</span></span>
