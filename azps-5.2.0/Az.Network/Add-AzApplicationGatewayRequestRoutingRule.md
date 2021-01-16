---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362988"
---
# <span data-ttu-id="c78f4-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c78f4-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c78f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c78f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c78f4-103">Aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c78f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c78f4-104">SYNTAX</span></span>

### <span data-ttu-id="c78f4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c78f4-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c78f4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c78f4-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c78f4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c78f4-107">DESCRIPTION</span></span>
<span data-ttu-id="c78f4-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c78f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c78f4-109">EXAMPLES</span></span>

### <span data-ttu-id="c78f4-110">Esempio 1: aggiungere una regola di routing delle richieste a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c78f4-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c78f4-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c78f4-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c78f4-112">Il secondo comando aggiunge la regola di routing delle richieste al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="c78f4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c78f4-113">PARAMETERS</span></span>

### <span data-ttu-id="c78f4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c78f4-114">-ApplicationGateway</span></span>
<span data-ttu-id="c78f4-115">Specifica un gateway dell'applicazione a cui questo cmdlet aggiunge una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="c78f4-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c78f4-116">-BackendAddressPool</span></span>
<span data-ttu-id="c78f4-117">Specifica un oggetto pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c78f4-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c78f4-119">Specifica un ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c78f4-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c78f4-121">Specifica un oggetto impostazioni HTTP back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c78f4-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c78f4-123">Specifica un ID di impostazioni HTTP di backend per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78f4-124">-DefaultProfile</span></span>
<span data-ttu-id="c78f4-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c78f4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c78f4-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c78f4-126">-HttpListener</span></span>
<span data-ttu-id="c78f4-127">Specifica l'oggetto listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c78f4-128">-HttpListenerId</span></span>
<span data-ttu-id="c78f4-129">Specifica l'ID listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78f4-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c78f4-130">-Name</span></span>
<span data-ttu-id="c78f4-131">Specifica il nome della regola di routing della richiesta aggiunta dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c78f4-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="c78f4-132">-Priorità</span><span class="sxs-lookup"><span data-stu-id="c78f4-132">-Priority</span></span>
<span data-ttu-id="c78f4-133">Priorità della regola</span><span class="sxs-lookup"><span data-stu-id="c78f4-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c78f4-134">-RedirectConfiguration</span></span>
<span data-ttu-id="c78f4-135">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c78f4-135">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c78f4-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="c78f4-137">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c78f4-137">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c78f4-138">-RewriteRuleSet</span></span>
<span data-ttu-id="c78f4-139">App gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c78f4-139">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c78f4-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="c78f4-141">ID dell'applicazione gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c78f4-141">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c78f4-142">-RuleType</span></span>
<span data-ttu-id="c78f4-143">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="c78f4-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c78f4-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c78f4-145">-UrlPathMapId</span></span>
<span data-ttu-id="c78f4-146">Specifica l'ID Mappa percorso URL per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="c78f4-146">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78f4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78f4-147">CommonParameters</span></span>
<span data-ttu-id="c78f4-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78f4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78f4-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c78f4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78f4-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c78f4-150">INPUTS</span></span>

### <span data-ttu-id="c78f4-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c78f4-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c78f4-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c78f4-152">OUTPUTS</span></span>

### <span data-ttu-id="c78f4-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c78f4-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c78f4-154">Note</span><span class="sxs-lookup"><span data-stu-id="c78f4-154">NOTES</span></span>

## <span data-ttu-id="c78f4-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c78f4-155">RELATED LINKS</span></span>

[<span data-ttu-id="c78f4-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c78f4-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c78f4-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c78f4-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c78f4-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c78f4-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c78f4-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c78f4-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


