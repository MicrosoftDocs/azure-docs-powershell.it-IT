---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: b0335fd0700b256650809c4548efe4d1e620442b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203478"
---
# <span data-ttu-id="2d58a-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d58a-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2d58a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d58a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d58a-103">Aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="2d58a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d58a-104">SYNTAX</span></span>

### <span data-ttu-id="2d58a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d58a-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d58a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2d58a-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d58a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d58a-107">DESCRIPTION</span></span>
<span data-ttu-id="2d58a-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="2d58a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d58a-109">EXAMPLES</span></span>

### <span data-ttu-id="2d58a-110">Esempio 1: aggiungere una regola di routing delle richieste a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2d58a-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="2d58a-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2d58a-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2d58a-112">Il secondo comando aggiunge la regola di routing delle richieste al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="2d58a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d58a-113">PARAMETERS</span></span>

### <span data-ttu-id="2d58a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d58a-114">-ApplicationGateway</span></span>
<span data-ttu-id="2d58a-115">Specifica un gateway dell'applicazione a cui questo cmdlet aggiunge una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="2d58a-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="2d58a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d58a-116">-BackendAddressPool</span></span>
<span data-ttu-id="2d58a-117">Specifica un oggetto pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="2d58a-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2d58a-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="2d58a-119">Specifica un ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="2d58a-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2d58a-120">-BackendHttpSettings</span></span>
<span data-ttu-id="2d58a-121">Specifica un oggetto impostazioni HTTP back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="2d58a-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2d58a-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2d58a-123">Specifica un ID di impostazioni HTTP di backend per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="2d58a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d58a-124">-DefaultProfile</span></span>
<span data-ttu-id="2d58a-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d58a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d58a-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="2d58a-126">-HttpListener</span></span>
<span data-ttu-id="2d58a-127">Specifica l'oggetto listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="2d58a-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="2d58a-128">-HttpListenerId</span></span>
<span data-ttu-id="2d58a-129">Specifica l'ID listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d58a-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="2d58a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d58a-130">-Name</span></span>
<span data-ttu-id="2d58a-131">Specifica il nome della regola di routing della richiesta aggiunta dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d58a-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="2d58a-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d58a-132">-RedirectConfiguration</span></span>
<span data-ttu-id="2d58a-133">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d58a-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2d58a-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2d58a-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="2d58a-135">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d58a-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2d58a-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d58a-136">-RewriteRuleSet</span></span>
<span data-ttu-id="2d58a-137">App gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d58a-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2d58a-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2d58a-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="2d58a-139">ID dell'applicazione gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d58a-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2d58a-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="2d58a-140">-RuleType</span></span>
<span data-ttu-id="2d58a-141">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="2d58a-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="2d58a-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2d58a-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="2d58a-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="2d58a-143">-UrlPathMapId</span></span>
<span data-ttu-id="2d58a-144">Specifica l'ID Mappa percorso URL per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="2d58a-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="2d58a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d58a-145">CommonParameters</span></span>
<span data-ttu-id="2d58a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d58a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d58a-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d58a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d58a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d58a-148">INPUTS</span></span>

### <span data-ttu-id="2d58a-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d58a-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d58a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d58a-150">OUTPUTS</span></span>

### <span data-ttu-id="2d58a-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d58a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d58a-152">Note</span><span class="sxs-lookup"><span data-stu-id="2d58a-152">NOTES</span></span>

## <span data-ttu-id="2d58a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d58a-153">RELATED LINKS</span></span>

[<span data-ttu-id="2d58a-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d58a-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d58a-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d58a-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d58a-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d58a-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d58a-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d58a-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


