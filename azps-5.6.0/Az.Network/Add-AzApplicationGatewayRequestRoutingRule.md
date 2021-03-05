---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d86810ec15d38ecbe57a7471297b4ac167a2e526
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982509"
---
# <span data-ttu-id="2a8a6-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a8a6-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2a8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8a6-103">Aggiunge una regola di routing delle richieste a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="2a8a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a8a6-104">SYNTAX</span></span>

### <span data-ttu-id="2a8a6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a8a6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a8a6-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a8a6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8a6-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** aggiunge una regola di routing delle richieste a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="2a8a6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a8a6-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8a6-110">Esempio 1: Aggiungere una regola di routing delle richieste a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2a8a6-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="2a8a6-111">Il primo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2a8a6-112">Il secondo comando aggiunge la regola di routing delle richieste al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="2a8a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a8a6-113">PARAMETERS</span></span>

### <span data-ttu-id="2a8a6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a8a6-114">-ApplicationGateway</span></span>
<span data-ttu-id="2a8a6-115">Specifica un gateway applicazione a cui questo cmdlet aggiunge una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="2a8a6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a8a6-116">-BackendAddressPool</span></span>
<span data-ttu-id="2a8a6-117">Specifica un oggetto pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="2a8a6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="2a8a6-119">Specifica un ID pool di indirizzi back-end del gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="2a8a6-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2a8a6-120">-BackendHttpSettings</span></span>
<span data-ttu-id="2a8a6-121">Specifica un oggetto impostazioni HTTP back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="2a8a6-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2a8a6-123">Specifica un ID di impostazioni HTTP back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="2a8a6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8a6-124">-DefaultProfile</span></span>
<span data-ttu-id="2a8a6-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a8a6-126">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="2a8a6-126">-HttpListener</span></span>
<span data-ttu-id="2a8a6-127">Specifica l'oggetto listener HTTP del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="2a8a6-128">-HttpDirId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-128">-HttpListenerId</span></span>
<span data-ttu-id="2a8a6-129">Specifica l'ID listener HTTP del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="2a8a6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2a8a6-130">-Name</span></span>
<span data-ttu-id="2a8a6-131">Specifica il nome della regola di routing delle richieste che questo cmdlet aggiunge.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="2a8a6-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="2a8a6-132">-Priority</span></span>
<span data-ttu-id="2a8a6-133">Priorità della regola</span><span class="sxs-lookup"><span data-stu-id="2a8a6-133">The priority of the rule</span></span>

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

### <span data-ttu-id="2a8a6-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a8a6-134">-RedirectConfiguration</span></span>
<span data-ttu-id="2a8a6-135">RedirectConfiguration del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2a8a6-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2a8a6-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="2a8a6-137">ID del gateway applicazione RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a8a6-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2a8a6-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a8a6-138">-RewriteRuleSet</span></span>
<span data-ttu-id="2a8a6-139">RewriteRuleSet del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="2a8a6-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2a8a6-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="2a8a6-141">ID del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a8a6-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2a8a6-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="2a8a6-142">-RuleType</span></span>
<span data-ttu-id="2a8a6-143">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="2a8a6-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2a8a6-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="2a8a6-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="2a8a6-145">-UrlPathMapId</span></span>
<span data-ttu-id="2a8a6-146">Specifica l'ID mappa del percorso URL per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="2a8a6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8a6-147">CommonParameters</span></span>
<span data-ttu-id="2a8a6-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8a6-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a8a6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8a6-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a8a6-150">INPUTS</span></span>

### <span data-ttu-id="2a8a6-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a8a6-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a8a6-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a8a6-152">OUTPUTS</span></span>

### <span data-ttu-id="2a8a6-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a8a6-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a8a6-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a8a6-154">NOTES</span></span>

## <span data-ttu-id="2a8a6-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a8a6-155">RELATED LINKS</span></span>

[<span data-ttu-id="2a8a6-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a8a6-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a8a6-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a8a6-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a8a6-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a8a6-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a8a6-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a8a6-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


