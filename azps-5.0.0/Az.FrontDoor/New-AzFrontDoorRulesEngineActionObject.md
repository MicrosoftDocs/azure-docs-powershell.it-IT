---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200874"
---
# <span data-ttu-id="2caf1-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="2caf1-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="2caf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2caf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2caf1-103">Crea un oggetto PSRulesEngineAction per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="2caf1-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="2caf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2caf1-104">SYNTAX</span></span>

### <span data-ttu-id="2caf1-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="2caf1-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2caf1-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2caf1-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2caf1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2caf1-107">DESCRIPTION</span></span>
<span data-ttu-id="2caf1-108">Crea un oggetto PSRulesEngineAction per la creazione di una regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="2caf1-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="2caf1-109">Usa il cmdlet "New-AzFrontDoorHeaderActionObject" per creare PSHeaderObjects per passare ai parametri "-RequestHeaderActions" e "-ResponseHeaderActions". "</span><span class="sxs-lookup"><span data-stu-id="2caf1-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="2caf1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2caf1-110">EXAMPLES</span></span>

### <span data-ttu-id="2caf1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2caf1-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="2caf1-112">Creare un'azione motore regole e mostrare come visualizzare le proprietà dell'azione del motore regole create.</span><span class="sxs-lookup"><span data-stu-id="2caf1-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="2caf1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2caf1-113">PARAMETERS</span></span>

### <span data-ttu-id="2caf1-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="2caf1-114">-BackendPoolName</span></span>
<span data-ttu-id="2caf1-115">Nome del BackendPool a cui questa regola viene indirizzata</span><span class="sxs-lookup"><span data-stu-id="2caf1-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="2caf1-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="2caf1-116">-CustomForwardingPath</span></span>
<span data-ttu-id="2caf1-117">Percorso personalizzato usato per riscrivere i percorsi delle risorse corrispondenti alla regola.</span><span class="sxs-lookup"><span data-stu-id="2caf1-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="2caf1-118">Lascia vuoto per usare il percorso in arrivo.</span><span class="sxs-lookup"><span data-stu-id="2caf1-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="2caf1-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="2caf1-119">-CustomFragment</span></span>
<span data-ttu-id="2caf1-120">Frammento da aggiungere all'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="2caf1-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="2caf1-121">Fragment è la parte dell'URL che viene dopo #.</span><span class="sxs-lookup"><span data-stu-id="2caf1-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="2caf1-122">Non includere #.</span><span class="sxs-lookup"><span data-stu-id="2caf1-122">Do not include the #.</span></span>

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

### <span data-ttu-id="2caf1-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="2caf1-123">-CustomHost</span></span>
<span data-ttu-id="2caf1-124">Host da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="2caf1-124">Host to redirect.</span></span>
<span data-ttu-id="2caf1-125">Lascia vuoto per usare l'host in arrivo come host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2caf1-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="2caf1-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="2caf1-126">-CustomPath</span></span>
<span data-ttu-id="2caf1-127">Il percorso completo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="2caf1-127">The full path to redirect.</span></span>
<span data-ttu-id="2caf1-128">Il percorso non può essere vuoto e deve iniziare con/.</span><span class="sxs-lookup"><span data-stu-id="2caf1-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="2caf1-129">Lascia vuoto per usare il percorso in arrivo come percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2caf1-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="2caf1-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="2caf1-130">-CustomQueryString</span></span>
<span data-ttu-id="2caf1-131">Il set di stringhe di query da inserire nell'URL di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="2caf1-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="2caf1-132">L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente. lascia vuoto per mantenere la stringa di query in arrivo.</span><span class="sxs-lookup"><span data-stu-id="2caf1-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="2caf1-133">La stringa di query deve essere in \<key\> = \<value\> formato.</span><span class="sxs-lookup"><span data-stu-id="2caf1-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="2caf1-134">La prima?</span><span class="sxs-lookup"><span data-stu-id="2caf1-134">The first ?</span></span>
<span data-ttu-id="2caf1-135">e & verranno aggiunti automaticamente in modo da non includerli in primo piano, ma separare più stringhe di query con &.</span><span class="sxs-lookup"><span data-stu-id="2caf1-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="2caf1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2caf1-136">-DefaultProfile</span></span>
<span data-ttu-id="2caf1-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2caf1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2caf1-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="2caf1-138">-DynamicCompression</span></span>
<span data-ttu-id="2caf1-139">Se abilitare la compressione dinamica per il contenuto memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="2caf1-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="2caf1-140">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="2caf1-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="2caf1-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="2caf1-141">-EnableCaching</span></span>
<span data-ttu-id="2caf1-142">Se abilitare la memorizzazione nella cache per questa route.</span><span class="sxs-lookup"><span data-stu-id="2caf1-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="2caf1-143">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="2caf1-143">Default value is false</span></span>

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

### <span data-ttu-id="2caf1-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="2caf1-144">-ForwardingProtocol</span></span>
<span data-ttu-id="2caf1-145">Protocollo che questa regola userà quando si inoltra il traffico ai backend.</span><span class="sxs-lookup"><span data-stu-id="2caf1-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="2caf1-146">Il valore predefinito è MatchRequest</span><span class="sxs-lookup"><span data-stu-id="2caf1-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="2caf1-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2caf1-147">-FrontDoorName</span></span>
<span data-ttu-id="2caf1-148">Nome dello sportello anteriore a cui appartiene la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="2caf1-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="2caf1-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="2caf1-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="2caf1-150">Il trattamento dei termini di query URL quando si forma la chiave di cache.</span><span class="sxs-lookup"><span data-stu-id="2caf1-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="2caf1-151">Il valore predefinito è StripAll</span><span class="sxs-lookup"><span data-stu-id="2caf1-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="2caf1-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="2caf1-152">-RedirectProtocol</span></span>
<span data-ttu-id="2caf1-153">Il protocollo della destinazione in cui viene reindirizzato il traffico.</span><span class="sxs-lookup"><span data-stu-id="2caf1-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="2caf1-154">Il valore predefinito è MatchRequest</span><span class="sxs-lookup"><span data-stu-id="2caf1-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="2caf1-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="2caf1-155">-RedirectType</span></span>
<span data-ttu-id="2caf1-156">Il tipo di reindirizzamento che verrà usato dalla regola per reindirizzare il traffico.</span><span class="sxs-lookup"><span data-stu-id="2caf1-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="2caf1-157">Il valore predefinito viene spostato</span><span class="sxs-lookup"><span data-stu-id="2caf1-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="2caf1-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="2caf1-158">-RequestHeaderAction</span></span>
<span data-ttu-id="2caf1-159">Elenco di azioni di intestazione da applicare alla richiesta da AFD all'origine.</span><span class="sxs-lookup"><span data-stu-id="2caf1-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2caf1-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2caf1-160">-ResourceGroupName</span></span>
<span data-ttu-id="2caf1-161">Nome del gruppo di risorse in cui verrà creato il RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="2caf1-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="2caf1-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="2caf1-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="2caf1-163">Elenco di azioni di intestazione da applicare alla risposta da AFD al client.</span><span class="sxs-lookup"><span data-stu-id="2caf1-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2caf1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2caf1-164">CommonParameters</span></span>
<span data-ttu-id="2caf1-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2caf1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2caf1-166">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2caf1-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2caf1-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2caf1-167">INPUTS</span></span>

### <span data-ttu-id="2caf1-168">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2caf1-168">None</span></span>

## <span data-ttu-id="2caf1-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2caf1-169">OUTPUTS</span></span>

### <span data-ttu-id="2caf1-170">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="2caf1-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="2caf1-171">Note</span><span class="sxs-lookup"><span data-stu-id="2caf1-171">NOTES</span></span>

## <span data-ttu-id="2caf1-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2caf1-172">RELATED LINKS</span></span>
