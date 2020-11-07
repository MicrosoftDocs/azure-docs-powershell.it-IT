---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836135"
---
# <span data-ttu-id="43e55-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="43e55-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="43e55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43e55-102">SYNOPSIS</span></span>
<span data-ttu-id="43e55-103">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="43e55-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="43e55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43e55-104">SYNTAX</span></span>

### <span data-ttu-id="43e55-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e55-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43e55-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e55-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43e55-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e55-107">DESCRIPTION</span></span>
<span data-ttu-id="43e55-108">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="43e55-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="43e55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43e55-109">EXAMPLES</span></span>

### <span data-ttu-id="43e55-110">Esempio 1: creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="43e55-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="43e55-111">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="43e55-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="43e55-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43e55-112">PARAMETERS</span></span>

### <span data-ttu-id="43e55-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="43e55-113">-AcceptedProtocol</span></span>
<span data-ttu-id="43e55-114">Schemi di protocollo da corrispondere per la regola.</span><span class="sxs-lookup"><span data-stu-id="43e55-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="43e55-115">Il valore predefinito è {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="43e55-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="43e55-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="43e55-116">-BackendPoolName</span></span>
<span data-ttu-id="43e55-117">ID risorsa della BackendPool a cui questa regola viene indirizzata</span><span class="sxs-lookup"><span data-stu-id="43e55-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="43e55-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="43e55-118">-CustomForwardingPath</span></span>
<span data-ttu-id="43e55-119">Percorso personalizzato usato per riscrivere i percorsi delle risorse corrispondenti alla regola.</span><span class="sxs-lookup"><span data-stu-id="43e55-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="43e55-120">Lascia vuoto per usare il percorso in arrivo.</span><span class="sxs-lookup"><span data-stu-id="43e55-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="43e55-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="43e55-121">-CustomFragment</span></span>
<span data-ttu-id="43e55-122">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="43e55-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="43e55-123">Fragment è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="43e55-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="43e55-124">Non includere #.</span><span class="sxs-lookup"><span data-stu-id="43e55-124">Do not include the #.</span></span>

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

### <span data-ttu-id="43e55-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="43e55-125">-CustomHost</span></span>
<span data-ttu-id="43e55-126">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="43e55-126">Host to redirect.</span></span> <span data-ttu-id="43e55-127">Lascia vuoto per usare l'host in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43e55-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="43e55-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="43e55-128">-CustomPath</span></span>
<span data-ttu-id="43e55-129">Il percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="43e55-129">The full path to redirect.</span></span> <span data-ttu-id="43e55-130">Il percorso non può essere vuoto e deve iniziare con/.</span><span class="sxs-lookup"><span data-stu-id="43e55-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="43e55-131">Lascia vuoto per usare il percorso in arrivo come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43e55-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="43e55-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="43e55-132">-CustomQueryString</span></span>
<span data-ttu-id="43e55-133">Il set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="43e55-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="43e55-134">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente. lascia vuoto per mantenere la stringa di query in arrivo.</span><span class="sxs-lookup"><span data-stu-id="43e55-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="43e55-135">La stringa di query deve essere in <key>=</span><span class="sxs-lookup"><span data-stu-id="43e55-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="43e55-136">formato.</span><span class="sxs-lookup"><span data-stu-id="43e55-136">format.</span></span> <span data-ttu-id="43e55-137">La prima?</span><span class="sxs-lookup"><span data-stu-id="43e55-137">The first ?</span></span> <span data-ttu-id="43e55-138">e & verranno aggiunti automaticamente in modo da non includerli in primo piano, ma separare più stringhe di query con &.</span><span class="sxs-lookup"><span data-stu-id="43e55-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="43e55-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e55-139">-DefaultProfile</span></span>
<span data-ttu-id="43e55-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43e55-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e55-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="43e55-141">-DynamicCompression</span></span>
<span data-ttu-id="43e55-142">Se abilitare la compressione dinamica per il contenuto memorizzato nella cache quando è abilitata la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="43e55-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="43e55-143">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="43e55-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="43e55-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="43e55-144">-EnableCaching</span></span>
<span data-ttu-id="43e55-145">Se abilitare la memorizzazione nella cache per questa route.</span><span class="sxs-lookup"><span data-stu-id="43e55-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="43e55-146">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="43e55-146">Default value is false</span></span>

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

### <span data-ttu-id="43e55-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="43e55-147">-EnabledState</span></span>
<span data-ttu-id="43e55-148">Se abilitare l'uso di questa regola.</span><span class="sxs-lookup"><span data-stu-id="43e55-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="43e55-149">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="43e55-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="43e55-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="43e55-150">-ForwardingProtocol</span></span>
<span data-ttu-id="43e55-151">Il protocollo che questa regola userà quando si inoltra il traffico al valore predefinito di backend è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="43e55-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e55-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="43e55-152">-FrontDoorName</span></span>
<span data-ttu-id="43e55-153">Nome dello sportello anteriore a cui appartiene la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="43e55-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="43e55-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="43e55-154">-FrontendEndpointName</span></span>
<span data-ttu-id="43e55-155">Nomi degli endpoint frontend associati a questa regola</span><span class="sxs-lookup"><span data-stu-id="43e55-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="43e55-156">-Nome</span><span class="sxs-lookup"><span data-stu-id="43e55-156">-Name</span></span>
<span data-ttu-id="43e55-157">Nome RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="43e55-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="43e55-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="43e55-158">-PatternToMatch</span></span>
<span data-ttu-id="43e55-159">I modelli di route della regola non devono avere \* eccetto eventualmente dopo la finale/alla fine del percorso.</span><span class="sxs-lookup"><span data-stu-id="43e55-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="43e55-160">Il valore predefinito è/\*</span><span class="sxs-lookup"><span data-stu-id="43e55-160">Default value is /\*</span></span>

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

### <span data-ttu-id="43e55-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="43e55-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="43e55-162">Il trattamento dei termini di query URL quando si forma la chiave di cache.</span><span class="sxs-lookup"><span data-stu-id="43e55-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="43e55-163">Il valore predefinito è StripAll</span><span class="sxs-lookup"><span data-stu-id="43e55-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e55-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="43e55-164">-RedirectProtocol</span></span>
<span data-ttu-id="43e55-165">Il protocollo della destinazione in cui viene reindirizzato il traffico.</span><span class="sxs-lookup"><span data-stu-id="43e55-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="43e55-166">Il valore predefinito è MatchRequest</span><span class="sxs-lookup"><span data-stu-id="43e55-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e55-167">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="43e55-167">-RedirectType</span></span>
<span data-ttu-id="43e55-168">Il tipo di reindirizzamento che verrà usato dalla regola per reindirizzare il traffico.</span><span class="sxs-lookup"><span data-stu-id="43e55-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="43e55-169">Il valore predefinito viene spostato</span><span class="sxs-lookup"><span data-stu-id="43e55-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e55-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e55-170">-ResourceGroupName</span></span>
<span data-ttu-id="43e55-171">Nome del gruppo di risorse in cui verrà creato il RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="43e55-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="43e55-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e55-172">CommonParameters</span></span>
<span data-ttu-id="43e55-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e55-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e55-174">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43e55-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e55-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43e55-175">INPUTS</span></span>

### <span data-ttu-id="43e55-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="43e55-176">None</span></span>

## <span data-ttu-id="43e55-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43e55-177">OUTPUTS</span></span>

### <span data-ttu-id="43e55-178">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="43e55-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="43e55-179">Note</span><span class="sxs-lookup"><span data-stu-id="43e55-179">NOTES</span></span>

## <span data-ttu-id="43e55-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43e55-180">RELATED LINKS</span></span>

<span data-ttu-id="43e55-181">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="43e55-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
