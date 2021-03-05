---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3d66db0baeca0e371800c4544f2f0360c448b108
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970989"
---
# <span data-ttu-id="dbb67-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="dbb67-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="dbb67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbb67-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb67-103">Creare un oggetto PSRoutingRuleObject per la creazione in primo piano</span><span class="sxs-lookup"><span data-stu-id="dbb67-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="dbb67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbb67-104">SYNTAX</span></span>

### <span data-ttu-id="dbb67-105">ByFieldsWithForwardingParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="dbb67-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbb67-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbb67-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbb67-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbb67-107">DESCRIPTION</span></span>
<span data-ttu-id="dbb67-108">Creare un oggetto PSRoutingRuleObject per la creazione in primo piano</span><span class="sxs-lookup"><span data-stu-id="dbb67-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="dbb67-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbb67-109">EXAMPLES</span></span>

### <span data-ttu-id="dbb67-110">Esempio 1: Creare un oggetto PSRoutingRuleObject per la creazione in primo piano con una regola di inoltro</span><span class="sxs-lookup"><span data-stu-id="dbb67-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="dbb67-111">Esempio 2: Creare un oggetto PSRoutingRuleObject per la creazione in primo piano con una regola di reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="dbb67-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="dbb67-112">Creare un oggetto PSRoutingRuleObject per la creazione in primo piano</span><span class="sxs-lookup"><span data-stu-id="dbb67-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="dbb67-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbb67-113">PARAMETERS</span></span>

### <span data-ttu-id="dbb67-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="dbb67-114">-AcceptedProtocol</span></span>
<span data-ttu-id="dbb67-115">Combinazioni di protocolli corrispondenti a questa regola.</span><span class="sxs-lookup"><span data-stu-id="dbb67-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="dbb67-116">Il valore predefinito è {Https, Http}</span><span class="sxs-lookup"><span data-stu-id="dbb67-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="dbb67-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="dbb67-117">-BackendPoolName</span></span>
<span data-ttu-id="dbb67-118">ID risorsa del BackendPool a cui la regola si instrada</span><span class="sxs-lookup"><span data-stu-id="dbb67-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="dbb67-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="dbb67-119">-CustomForwardingPath</span></span>
<span data-ttu-id="dbb67-120">Percorso personalizzato usato per riscrivere i percorsi delle risorse corrispondenti a questa regola.</span><span class="sxs-lookup"><span data-stu-id="dbb67-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="dbb67-121">Lasciare vuoto per usare il percorso in arrivo.</span><span class="sxs-lookup"><span data-stu-id="dbb67-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="dbb67-122">-Custom Deframment</span><span class="sxs-lookup"><span data-stu-id="dbb67-122">-CustomFragment</span></span>
<span data-ttu-id="dbb67-123">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="dbb67-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="dbb67-124">Frammento è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="dbb67-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="dbb67-125">Non includere il valore di errore #.</span><span class="sxs-lookup"><span data-stu-id="dbb67-125">Do not include the #.</span></span>

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

### <span data-ttu-id="dbb67-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="dbb67-126">-CustomHost</span></span>
<span data-ttu-id="dbb67-127">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="dbb67-127">Host to redirect.</span></span> <span data-ttu-id="dbb67-128">Lasciare vuoto per usare l'host della posta in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dbb67-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="dbb67-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="dbb67-129">-CustomPath</span></span>
<span data-ttu-id="dbb67-130">Percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="dbb67-130">The full path to redirect.</span></span> <span data-ttu-id="dbb67-131">Il percorso non può essere vuoto e deve iniziare con /.</span><span class="sxs-lookup"><span data-stu-id="dbb67-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="dbb67-132">Lasciare vuoto per usare il percorso in ingresso come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dbb67-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="dbb67-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="dbb67-133">-CustomQueryString</span></span>
<span data-ttu-id="dbb67-134">Set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="dbb67-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="dbb67-135">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente; lasciare vuota per mantenere la stringa di query in ingresso.</span><span class="sxs-lookup"><span data-stu-id="dbb67-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="dbb67-136">La stringa di query deve essere in <key>=</span><span class="sxs-lookup"><span data-stu-id="dbb67-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="dbb67-137">.</span><span class="sxs-lookup"><span data-stu-id="dbb67-137">format.</span></span> <span data-ttu-id="dbb67-138">Il primo?</span><span class="sxs-lookup"><span data-stu-id="dbb67-138">The first ?</span></span> <span data-ttu-id="dbb67-139">e & verranno aggiunte automaticamente, quindi non includerle nella parte frontale, ma separare più stringhe di query con &.</span><span class="sxs-lookup"><span data-stu-id="dbb67-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="dbb67-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb67-140">-DefaultProfile</span></span>
<span data-ttu-id="dbb67-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb67-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbb67-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="dbb67-142">-DynamicCompression</span></span>
<span data-ttu-id="dbb67-143">Se abilitare la compressione dinamica per il contenuto memorizzato nella cache quando è abilitata la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="dbb67-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="dbb67-144">Il valore predefinito è Abilitato</span><span class="sxs-lookup"><span data-stu-id="dbb67-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="dbb67-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="dbb67-145">-EnableCaching</span></span>
<span data-ttu-id="dbb67-146">Se abilitare la memorizzazione nella cache per questa route.</span><span class="sxs-lookup"><span data-stu-id="dbb67-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="dbb67-147">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="dbb67-147">Default value is false</span></span>

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

### <span data-ttu-id="dbb67-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="dbb67-148">-EnabledState</span></span>
<span data-ttu-id="dbb67-149">Se abilitare o meno l'uso di questa regola.</span><span class="sxs-lookup"><span data-stu-id="dbb67-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="dbb67-150">Il valore predefinito è Abilitato</span><span class="sxs-lookup"><span data-stu-id="dbb67-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="dbb67-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="dbb67-151">-ForwardingProtocol</span></span>
<span data-ttu-id="dbb67-152">Il protocollo che verrà utilizzato da questa regola per l'inoltro del traffico al valore predefinito back-end è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="dbb67-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="dbb67-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="dbb67-153">-FrontDoorName</span></span>
<span data-ttu-id="dbb67-154">Nome della porta a cui appartiene questa regola di routing.</span><span class="sxs-lookup"><span data-stu-id="dbb67-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="dbb67-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="dbb67-155">-FrontendEndpointName</span></span>
<span data-ttu-id="dbb67-156">Nomi degli endpoint frontend associati a questa regola</span><span class="sxs-lookup"><span data-stu-id="dbb67-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="dbb67-157">-Name</span><span class="sxs-lookup"><span data-stu-id="dbb67-157">-Name</span></span>
<span data-ttu-id="dbb67-158">RoutingRule name.</span><span class="sxs-lookup"><span data-stu-id="dbb67-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="dbb67-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="dbb67-159">-PatternToMatch</span></span>
<span data-ttu-id="dbb67-160">I modelli di percorso della regola, Non devono avere \* tranne eventualmente dopo il finale / alla fine del percorso.</span><span class="sxs-lookup"><span data-stu-id="dbb67-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="dbb67-161">Il valore predefinito è /\*</span><span class="sxs-lookup"><span data-stu-id="dbb67-161">Default value is /\*</span></span>

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

### <span data-ttu-id="dbb67-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="dbb67-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="dbb67-163">Il trattamento dei termini di query URL durante la creazione della chiave cache.</span><span class="sxs-lookup"><span data-stu-id="dbb67-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="dbb67-164">Il valore predefinito è StripAll</span><span class="sxs-lookup"><span data-stu-id="dbb67-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="dbb67-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="dbb67-165">-RedirectProtocol</span></span>
<span data-ttu-id="dbb67-166">Protocollo della destinazione a cui viene reindirizzato il traffico.</span><span class="sxs-lookup"><span data-stu-id="dbb67-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="dbb67-167">Il valore predefinito è MatchRequest</span><span class="sxs-lookup"><span data-stu-id="dbb67-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="dbb67-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="dbb67-168">-RedirectType</span></span>
<span data-ttu-id="dbb67-169">Tipo di reindirizzamento che la regola userà per il reindirizzamento del traffico.</span><span class="sxs-lookup"><span data-stu-id="dbb67-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="dbb67-170">Il valore predefinito viene spostato</span><span class="sxs-lookup"><span data-stu-id="dbb67-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="dbb67-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb67-171">-ResourceGroupName</span></span>
<span data-ttu-id="dbb67-172">Nome del gruppo di risorse con cui verrà creata la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="dbb67-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="dbb67-173">-RulesToolName</span><span class="sxs-lookup"><span data-stu-id="dbb67-173">-RulesEngineName</span></span>
<span data-ttu-id="dbb67-174">Riferimento a una specifica configurazione del motore di regole da applicare a questa route.</span><span class="sxs-lookup"><span data-stu-id="dbb67-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="dbb67-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb67-175">CommonParameters</span></span>
<span data-ttu-id="dbb67-176">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb67-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb67-177">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbb67-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb67-178">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbb67-178">INPUTS</span></span>

### <span data-ttu-id="dbb67-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dbb67-179">None</span></span>

## <span data-ttu-id="dbb67-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbb67-180">OUTPUTS</span></span>

### <span data-ttu-id="dbb67-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dbb67-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="dbb67-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbb67-182">NOTES</span></span>

## <span data-ttu-id="dbb67-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbb67-183">RELATED LINKS</span></span>

<span data-ttu-id="dbb67-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="dbb67-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
