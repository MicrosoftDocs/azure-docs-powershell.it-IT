---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005886"
---
# <span data-ttu-id="6f924-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f924-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6f924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f924-102">SYNOPSIS</span></span>
<span data-ttu-id="6f924-103">Modifica una regola di routing delle richieste per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6f924-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6f924-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f924-104">SYNTAX</span></span>

### <span data-ttu-id="6f924-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f924-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f924-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6f924-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f924-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f924-107">DESCRIPTION</span></span>
<span data-ttu-id="6f924-108">Il cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modifica una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="6f924-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6f924-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f924-109">EXAMPLES</span></span>

### <span data-ttu-id="6f924-110">Esempio 1: Aggiornare una regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="6f924-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6f924-111">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="6f924-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6f924-112">Il secondo comando modifica la regola di routing delle richieste per il gateway di applicazione in modo che usi le impostazioni HTTP back-end specificate nella variabile $Setting, un listener HTTP specificato nella variabile $Listener e un pool di indirizzi back-end specificato nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="6f924-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6f924-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f924-113">PARAMETERS</span></span>

### <span data-ttu-id="6f924-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f924-114">-ApplicationGateway</span></span>
<span data-ttu-id="6f924-115">Specifica l'oggetto gateway applicazione a cui questo cmdlet associa una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="6f924-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="6f924-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6f924-116">-BackendAddressPool</span></span>
<span data-ttu-id="6f924-117">Specifica il pool di indirizzi back-end del gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6f924-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6f924-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6f924-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6f924-119">Specifica l'ID pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f924-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6f924-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f924-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6f924-121">Specifica le impostazioni HTTP back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f924-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6f924-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6f924-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6f924-123">Specifica l'ID delle impostazioni HTTP back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f924-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6f924-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f924-124">-DefaultProfile</span></span>
<span data-ttu-id="6f924-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f924-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f924-126">-HttpDir</span><span class="sxs-lookup"><span data-stu-id="6f924-126">-HttpListener</span></span>
<span data-ttu-id="6f924-127">Specifica il listener HTTP del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f924-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6f924-128">-HttpDirId</span><span class="sxs-lookup"><span data-stu-id="6f924-128">-HttpListenerId</span></span>
<span data-ttu-id="6f924-129">Specifica l'ID listener HTTP del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f924-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6f924-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6f924-130">-Name</span></span>
<span data-ttu-id="6f924-131">Specifica il nome della regola di routing delle richieste modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f924-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f924-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="6f924-132">-Priority</span></span>
<span data-ttu-id="6f924-133">Priorità della regola</span><span class="sxs-lookup"><span data-stu-id="6f924-133">The priority of the rule</span></span>

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

### <span data-ttu-id="6f924-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f924-134">-RedirectConfiguration</span></span>
<span data-ttu-id="6f924-135">RedirectConfiguration del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="6f924-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6f924-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6f924-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="6f924-137">ID del gateway applicazione RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f924-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6f924-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f924-138">-RewriteRuleSet</span></span>
<span data-ttu-id="6f924-139">RewriteRuleSet del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="6f924-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6f924-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6f924-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="6f924-141">ID del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f924-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6f924-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6f924-142">-RuleType</span></span>
<span data-ttu-id="6f924-143">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="6f924-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="6f924-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6f924-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="6f924-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6f924-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6f924-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f924-146">CommonParameters</span></span>
<span data-ttu-id="6f924-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f924-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f924-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f924-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f924-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f924-149">INPUTS</span></span>

### <span data-ttu-id="6f924-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f924-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f924-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f924-151">OUTPUTS</span></span>

### <span data-ttu-id="6f924-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f924-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f924-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f924-153">NOTES</span></span>

## <span data-ttu-id="6f924-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f924-154">RELATED LINKS</span></span>

[<span data-ttu-id="6f924-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f924-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6f924-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f924-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6f924-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f924-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6f924-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f924-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


