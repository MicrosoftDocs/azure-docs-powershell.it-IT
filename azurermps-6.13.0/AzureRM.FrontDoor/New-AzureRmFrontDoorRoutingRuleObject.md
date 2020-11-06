---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518652"
---
# <span data-ttu-id="ab8b3-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab8b3-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="ab8b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8b3-103">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="ab8b3-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab8b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab8b3-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab8b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab8b3-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8b3-106">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="ab8b3-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="ab8b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab8b3-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8b3-108">Esempio 1: creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="ab8b3-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

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

<span data-ttu-id="ab8b3-109">Creare un PSRoutingRuleObject per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="ab8b3-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="ab8b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab8b3-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8b3-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="ab8b3-111">-AcceptedProtocol</span></span>
<span data-ttu-id="ab8b3-112">Schemi di protocollo da corrispondere per la regola.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="ab8b3-113">Il valore predefinito è {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="ab8b3-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="ab8b3-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="ab8b3-114">-BackendPoolName</span></span>
<span data-ttu-id="ab8b3-115">ID risorsa della BackendPool a cui questa regola viene indirizzata</span><span class="sxs-lookup"><span data-stu-id="ab8b3-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="ab8b3-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="ab8b3-116">-CustomForwardingPath</span></span>
<span data-ttu-id="ab8b3-117">Percorso personalizzato usato per riscrivere i percorsi delle risorse corrispondenti alla regola.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="ab8b3-118">Lascia vuoto per usare il percorso in arrivo.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="ab8b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8b3-119">-DefaultProfile</span></span>
<span data-ttu-id="ab8b3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b3-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="ab8b3-121">-DynamicCompression</span></span>
<span data-ttu-id="ab8b3-122">Se abilitare la compressione dinamica per il contenuto memorizzato nella cache quando è abilitata la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="ab8b3-123">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="ab8b3-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="ab8b3-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="ab8b3-124">-EnableCaching</span></span>
<span data-ttu-id="ab8b3-125">Se abilitare la memorizzazione nella cache per questa route.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="ab8b3-126">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="ab8b3-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b3-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ab8b3-127">-EnabledState</span></span>
<span data-ttu-id="ab8b3-128">Se abilitare l'uso di questa regola.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="ab8b3-129">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="ab8b3-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="ab8b3-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="ab8b3-130">-ForwardingProtocol</span></span>
<span data-ttu-id="ab8b3-131">Il protocollo che questa regola userà quando si inoltra il traffico al valore predefinito di backend è MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b3-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ab8b3-132">-FrontDoorName</span></span>
<span data-ttu-id="ab8b3-133">Nome dello sportello anteriore a cui appartiene la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="ab8b3-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="ab8b3-134">-FrontendEndpointName</span></span>
<span data-ttu-id="ab8b3-135">Nomi degli endpoint frontend associati a questa regola</span><span class="sxs-lookup"><span data-stu-id="ab8b3-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="ab8b3-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab8b3-136">-Name</span></span>
<span data-ttu-id="ab8b3-137">Nome RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="ab8b3-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="ab8b3-138">-PatternToMatch</span></span>
<span data-ttu-id="ab8b3-139">I modelli di route della regola non devono avere \* eccetto eventualmente dopo la finale/alla fine del percorso.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="ab8b3-140">Il valore predefinito è/\*</span><span class="sxs-lookup"><span data-stu-id="ab8b3-140">Default value is /\*</span></span>

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

### <span data-ttu-id="ab8b3-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="ab8b3-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="ab8b3-142">Il trattamento dei termini di query URL quando si forma la chiave di cache.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="ab8b3-143">Il valore predefinito è StripAll</span><span class="sxs-lookup"><span data-stu-id="ab8b3-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8b3-144">-ResourceGroupName</span></span>
<span data-ttu-id="ab8b3-145">Nome del gruppo di risorse in cui verrà creato il RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="ab8b3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8b3-146">CommonParameters</span></span>
<span data-ttu-id="ab8b3-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8b3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8b3-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8b3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8b3-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab8b3-149">INPUTS</span></span>

### <span data-ttu-id="ab8b3-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ab8b3-150">None</span></span>

## <span data-ttu-id="ab8b3-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab8b3-151">OUTPUTS</span></span>

### <span data-ttu-id="ab8b3-152">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ab8b3-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="ab8b3-153">Note</span><span class="sxs-lookup"><span data-stu-id="ab8b3-153">NOTES</span></span>

## <span data-ttu-id="ab8b3-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab8b3-154">RELATED LINKS</span></span>

<span data-ttu-id="ab8b3-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ab8b3-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
