---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473869"
---
# <span data-ttu-id="b9c50-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="b9c50-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="b9c50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9c50-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c50-103">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="b9c50-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b9c50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9c50-104">SYNTAX</span></span>

### <span data-ttu-id="b9c50-105">ByFieldsWithForwardingParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9c50-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c50-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c50-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c50-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9c50-107">DESCRIPTION</span></span>
<span data-ttu-id="b9c50-108">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="b9c50-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b9c50-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9c50-109">EXAMPLES</span></span>

### <span data-ttu-id="b9c50-110">Esempio 1: creare una PSRoutingRuleObject per la creazione di porte anteriori con una regola di inoltro</span><span class="sxs-lookup"><span data-stu-id="b9c50-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="b9c50-111">Esempio 2: creare una PSRoutingRuleObject per la creazione di porte anteriori con una regola di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b9c50-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="b9c50-112">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="b9c50-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b9c50-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9c50-113">PARAMETERS</span></span>

### <span data-ttu-id="b9c50-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="b9c50-114">-AcceptedProtocol</span></span>
<span data-ttu-id="b9c50-115">Schemi di protocollo da corrispondere per la regola.</span><span class="sxs-lookup"><span data-stu-id="b9c50-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="b9c50-116">Il valore predefinito è {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="b9c50-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="b9c50-117">-BackendPoolName</span></span>
<span data-ttu-id="b9c50-118">ID risorsa della BackendPool a cui questa regola viene indirizzata</span><span class="sxs-lookup"><span data-stu-id="b9c50-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="b9c50-119">-CustomForwardingPath</span></span>
<span data-ttu-id="b9c50-120">Percorso personalizzato usato per riscrivere i percorsi delle risorse corrispondenti alla regola.</span><span class="sxs-lookup"><span data-stu-id="b9c50-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="b9c50-121">Lascia vuoto per usare il percorso in arrivo.</span><span class="sxs-lookup"><span data-stu-id="b9c50-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="b9c50-122">-CustomFragment</span></span>
<span data-ttu-id="b9c50-123">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="b9c50-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="b9c50-124">Fragment è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="b9c50-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="b9c50-125">Non includere #.</span><span class="sxs-lookup"><span data-stu-id="b9c50-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="b9c50-126">-CustomHost</span></span>
<span data-ttu-id="b9c50-127">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="b9c50-127">Host to redirect.</span></span> <span data-ttu-id="b9c50-128">Lascia vuoto per usare l'host in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b9c50-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="b9c50-129">-CustomPath</span></span>
<span data-ttu-id="b9c50-130">Il percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="b9c50-130">The full path to redirect.</span></span> <span data-ttu-id="b9c50-131">Il percorso non può essere vuoto e deve iniziare con/.</span><span class="sxs-lookup"><span data-stu-id="b9c50-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="b9c50-132">Lascia vuoto per usare il percorso in arrivo come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b9c50-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="b9c50-133">-CustomQueryString</span></span>
<span data-ttu-id="b9c50-134">Il set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="b9c50-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="b9c50-135">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente. lascia vuoto per mantenere la stringa di query in arrivo.</span><span class="sxs-lookup"><span data-stu-id="b9c50-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="b9c50-136">La stringa di query deve essere in <key>=</span><span class="sxs-lookup"><span data-stu-id="b9c50-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="b9c50-137">formato.</span><span class="sxs-lookup"><span data-stu-id="b9c50-137">format.</span></span> <span data-ttu-id="b9c50-138">La prima?</span><span class="sxs-lookup"><span data-stu-id="b9c50-138">The first ?</span></span> <span data-ttu-id="b9c50-139">e & verranno aggiunti automaticamente in modo da non includerli in primo piano, ma separare più stringhe di query con &.</span><span class="sxs-lookup"><span data-stu-id="b9c50-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c50-140">-DefaultProfile</span></span>
<span data-ttu-id="b9c50-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c50-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c50-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="b9c50-142">-DynamicCompression</span></span>
<span data-ttu-id="b9c50-143">Se abilitare la compressione dinamica per il contenuto memorizzato nella cache quando è abilitata la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="b9c50-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="b9c50-144">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="b9c50-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="b9c50-145">-EnableCaching</span></span>
<span data-ttu-id="b9c50-146">Se abilitare la memorizzazione nella cache per questa route.</span><span class="sxs-lookup"><span data-stu-id="b9c50-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="b9c50-147">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="b9c50-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b9c50-148">-EnabledState</span></span>
<span data-ttu-id="b9c50-149">Se abilitare l'uso di questa regola.</span><span class="sxs-lookup"><span data-stu-id="b9c50-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="b9c50-150">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="b9c50-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="b9c50-151">-ForwardingProtocol</span></span>
<span data-ttu-id="b9c50-152">Il protocollo che questa regola userà quando si inoltra il traffico al valore predefinito di backend è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="b9c50-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b9c50-153">-FrontDoorName</span></span>
<span data-ttu-id="b9c50-154">Nome dello sportello anteriore a cui appartiene la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="b9c50-154">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b9c50-155">-FrontendEndpointName</span></span>
<span data-ttu-id="b9c50-156">Nomi degli endpoint frontend associati a questa regola</span><span class="sxs-lookup"><span data-stu-id="b9c50-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c50-157">-Name</span></span>
<span data-ttu-id="b9c50-158">Nome RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="b9c50-158">RoutingRule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="b9c50-159">-PatternToMatch</span></span>
<span data-ttu-id="b9c50-160">I modelli di route della regola non devono avere \* eccetto eventualmente dopo la finale/alla fine del percorso.</span><span class="sxs-lookup"><span data-stu-id="b9c50-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="b9c50-161">Il valore predefinito è/\*</span><span class="sxs-lookup"><span data-stu-id="b9c50-161">Default value is /\*</span></span>

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

### <span data-ttu-id="b9c50-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="b9c50-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="b9c50-163">Il trattamento dei termini di query URL quando si forma la chiave di cache.</span><span class="sxs-lookup"><span data-stu-id="b9c50-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="b9c50-164">Il valore predefinito è StripAll</span><span class="sxs-lookup"><span data-stu-id="b9c50-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="b9c50-165">-RedirectProtocol</span></span>
<span data-ttu-id="b9c50-166">Il protocollo della destinazione in cui viene reindirizzato il traffico.</span><span class="sxs-lookup"><span data-stu-id="b9c50-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="b9c50-167">Il valore predefinito è MatchRequest</span><span class="sxs-lookup"><span data-stu-id="b9c50-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b9c50-168">-RedirectType</span></span>
<span data-ttu-id="b9c50-169">Il tipo di reindirizzamento che verrà usato dalla regola per reindirizzare il traffico.</span><span class="sxs-lookup"><span data-stu-id="b9c50-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="b9c50-170">Il valore predefinito viene spostato</span><span class="sxs-lookup"><span data-stu-id="b9c50-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c50-171">-ResourceGroupName</span></span>
<span data-ttu-id="b9c50-172">Nome del gruppo di risorse in cui verrà creato il RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="b9c50-172">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c50-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="b9c50-173">-RulesEngineName</span></span>
<span data-ttu-id="b9c50-174">Riferimento a una configurazione specifica del motore di regole da applicare alla route.</span><span class="sxs-lookup"><span data-stu-id="b9c50-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="b9c50-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c50-175">CommonParameters</span></span>
<span data-ttu-id="b9c50-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c50-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c50-177">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9c50-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c50-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9c50-178">INPUTS</span></span>

### <span data-ttu-id="b9c50-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b9c50-179">None</span></span>

## <span data-ttu-id="b9c50-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9c50-180">OUTPUTS</span></span>

### <span data-ttu-id="b9c50-181">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b9c50-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="b9c50-182">Note</span><span class="sxs-lookup"><span data-stu-id="b9c50-182">NOTES</span></span>

## <span data-ttu-id="b9c50-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9c50-183">RELATED LINKS</span></span>

<span data-ttu-id="b9c50-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b9c50-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
