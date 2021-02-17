---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185959"
---
# <span data-ttu-id="af1b6-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="af1b6-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="af1b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="af1b6-103">Recupera i dettagli di un dominio Griglia eventi o ottiene un elenco di tutti i domini Griglia eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="af1b6-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="af1b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af1b6-104">SYNTAX</span></span>

### <span data-ttu-id="af1b6-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af1b6-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af1b6-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af1b6-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af1b6-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="af1b6-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af1b6-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="af1b6-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af1b6-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af1b6-109">DESCRIPTION</span></span>
<span data-ttu-id="af1b6-110">Il Get-AzEventGridDomain cmdlet ottiene i dettagli di un dominio della griglia eventi specificato oppure un elenco di tutti i domini Griglia eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="af1b6-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="af1b6-111">Se viene fornito il nome di dominio, vengono restituiti i dettagli di un singolo dominio Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="af1b6-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="af1b6-112">Se il nome di dominio non viene fornito, viene restituito un elenco di domini.</span><span class="sxs-lookup"><span data-stu-id="af1b6-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="af1b6-113">Il numero di elementi restituiti in questo elenco è controllato dal parametro Top.</span><span class="sxs-lookup"><span data-stu-id="af1b6-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="af1b6-114">Se non viene specificato il valore Top o $null, l'elenco conterrà tutti gli elementi dei domini restituiti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="af1b6-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="af1b6-115">In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="af1b6-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="af1b6-116">Se sono ancora disponibili più domini, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva dei domini.</span><span class="sxs-lookup"><span data-stu-id="af1b6-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="af1b6-117">Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="af1b6-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="af1b6-118">La query di filtro segue la sintassi OData usando solo la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="af1b6-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="af1b6-119">Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="af1b6-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="af1b6-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af1b6-120">EXAMPLES</span></span>

### <span data-ttu-id="af1b6-121">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af1b6-121">Example 1</span></span>

<span data-ttu-id="af1b6-122">Ottiene i dettagli del dominio Griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="af1b6-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="af1b6-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="af1b6-123">Example 2</span></span>

<span data-ttu-id="af1b6-124">Ottiene i dettagli del dominio Griglia eventi Domain1 nel gruppo \` \` di risorse \` MyResourceGroupName \` usando l'opzione ResourceId.</span><span class="sxs-lookup"><span data-stu-id="af1b6-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="af1b6-125">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="af1b6-125">Example 3</span></span>

<span data-ttu-id="af1b6-126">Elencare tutti i domini della griglia eventi nel gruppo di risorse \` MyResourceGroupName senza \` impaginazione (tutti i domini vengono restituiti in un'unica schermata)</span><span class="sxs-lookup"><span data-stu-id="af1b6-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="af1b6-127">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="af1b6-127">Example 4</span></span>

<span data-ttu-id="af1b6-128">Elencare i domini della griglia degli eventi (se presenti) nel gruppo di risorse MyResourceGroupName che soddisfa i domini della \` \` query $odataFilter 10 alla volta.</span><span class="sxs-lookup"><span data-stu-id="af1b6-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="af1b6-129">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="af1b6-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="af1b6-130">Per ottenere le pagine dei domini successivi, è previsto che l'utente chiami di nuovo Get-AzEventGridDomain e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="af1b6-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="af1b6-131">Caller should stop when result. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="af1b6-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="af1b6-132">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="af1b6-132">Example 5</span></span>

<span data-ttu-id="af1b6-133">Elencare tutti i domini Griglia eventi nella sottoscrizione di Azure senza impaginazione (tutti i domini vengono restituiti in un'unica schermata)</span><span class="sxs-lookup"><span data-stu-id="af1b6-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="af1b6-134">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="af1b6-134">Example 6</span></span>

<span data-ttu-id="af1b6-135">Elencare gli eventuali domini della griglia degli eventi nella sottoscrizione di Azure che soddisfano i $odataFilter della query 20 per volta.</span><span class="sxs-lookup"><span data-stu-id="af1b6-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="af1b6-136">Se sono disponibili altri risultati, la $result. NextLink non verrà $null.</span><span class="sxs-lookup"><span data-stu-id="af1b6-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="af1b6-137">Per ottenere le pagine dei domini successivi, è previsto che l'utente chiami di nuovo Get-AzEventGridDomain e usi il risultato. NextLink ottenuto dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="af1b6-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="af1b6-138">Caller should stop when result. NextLink diventa $null.</span><span class="sxs-lookup"><span data-stu-id="af1b6-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="af1b6-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af1b6-139">PARAMETERS</span></span>

### <span data-ttu-id="af1b6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1b6-140">-DefaultProfile</span></span>
<span data-ttu-id="af1b6-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af1b6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af1b6-142">-Name</span><span class="sxs-lookup"><span data-stu-id="af1b6-142">-Name</span></span>
<span data-ttu-id="af1b6-143">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="af1b6-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af1b6-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="af1b6-144">-NextLink</span></span>
<span data-ttu-id="af1b6-145">Collegamento alla pagina successiva delle risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="af1b6-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="af1b6-146">Questo valore viene ottenuto con la prima chiamata Get-AzEventGrid cmdlet quando sono ancora disponibili altre risorse per la query.</span><span class="sxs-lookup"><span data-stu-id="af1b6-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="af1b6-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="af1b6-147">-ODataQuery</span></span>
<span data-ttu-id="af1b6-148">Query OData usata per filtrare i risultati dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="af1b6-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="af1b6-149">L'applicazione di filtri è attualmente consentita solo per la proprietà Nome. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="af1b6-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af1b6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1b6-150">-ResourceGroupName</span></span>
<span data-ttu-id="af1b6-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af1b6-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af1b6-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af1b6-152">-ResourceId</span></span>
<span data-ttu-id="af1b6-153">Identificatore di risorsa che rappresenta il dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="af1b6-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="af1b6-154">-In alto</span><span class="sxs-lookup"><span data-stu-id="af1b6-154">-Top</span></span>
<span data-ttu-id="af1b6-155">Numero massimo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="af1b6-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="af1b6-156">Il valore valido è compreso tra 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="af1b6-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="af1b6-157">Se viene specificato il valore superiore e sono ancora disponibili altri risultati, il risultato conterrà un collegamento alla pagina successiva in cui eseguire la query in NextLink.</span><span class="sxs-lookup"><span data-stu-id="af1b6-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="af1b6-158">Se non si specificato il valore Massimo, verrà restituito contemporaneamente l'elenco completo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="af1b6-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af1b6-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1b6-159">CommonParameters</span></span>
<span data-ttu-id="af1b6-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af1b6-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1b6-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af1b6-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1b6-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="af1b6-162">INPUTS</span></span>

### <span data-ttu-id="af1b6-163">System.String</span><span class="sxs-lookup"><span data-stu-id="af1b6-163">System.String</span></span>

## <span data-ttu-id="af1b6-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af1b6-164">OUTPUTS</span></span>

### <span data-ttu-id="af1b6-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="af1b6-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="af1b6-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="af1b6-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="af1b6-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="af1b6-167">NOTES</span></span>

## <span data-ttu-id="af1b6-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af1b6-168">RELATED LINKS</span></span>
