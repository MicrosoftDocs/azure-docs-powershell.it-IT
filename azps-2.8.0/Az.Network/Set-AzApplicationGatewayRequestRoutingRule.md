---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854142"
---
# <span data-ttu-id="9d50d-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d50d-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="9d50d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d50d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d50d-103">Modifica una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="9d50d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d50d-104">SYNTAX</span></span>

### <span data-ttu-id="9d50d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d50d-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d50d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d50d-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d50d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d50d-107">DESCRIPTION</span></span>
<span data-ttu-id="9d50d-108">Il cmdlet **set-AzApplicationGatewayRequestRoutingRule** modifica una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9d50d-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="9d50d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d50d-109">EXAMPLES</span></span>

### <span data-ttu-id="9d50d-110">Esempio 1: aggiornare una regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="9d50d-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="9d50d-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9d50d-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9d50d-112">Il secondo comando modifica la regola di routing delle richieste per il gateway dell'applicazione per l'uso delle impostazioni HTTP di back-end specificate nella variabile $Setting, un listener HTTP specificato nella variabile $Listener e un pool di indirizzi back-end specificato nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="9d50d-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="9d50d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d50d-113">PARAMETERS</span></span>

### <span data-ttu-id="9d50d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d50d-114">-ApplicationGateway</span></span>
<span data-ttu-id="9d50d-115">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9d50d-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="9d50d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9d50d-116">-BackendAddressPool</span></span>
<span data-ttu-id="9d50d-117">Specifica il pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="9d50d-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9d50d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="9d50d-119">Specifica l'ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="9d50d-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9d50d-120">-BackendHttpSettings</span></span>
<span data-ttu-id="9d50d-121">Specifica le impostazioni HTTP di backend del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="9d50d-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9d50d-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="9d50d-123">Specifica l'ID delle impostazioni HTTP di back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="9d50d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d50d-124">-DefaultProfile</span></span>
<span data-ttu-id="9d50d-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d50d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d50d-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9d50d-126">-HttpListener</span></span>
<span data-ttu-id="9d50d-127">Specifica il listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="9d50d-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="9d50d-128">-HttpListenerId</span></span>
<span data-ttu-id="9d50d-129">Specifica l'ID del listener HTTP gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d50d-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="9d50d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d50d-130">-Name</span></span>
<span data-ttu-id="9d50d-131">Specifica il nome della regola di routing delle richieste modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d50d-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9d50d-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d50d-132">-RedirectConfiguration</span></span>
<span data-ttu-id="9d50d-133">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d50d-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9d50d-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9d50d-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="9d50d-135">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d50d-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9d50d-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d50d-136">-RewriteRuleSet</span></span>
<span data-ttu-id="9d50d-137">App gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d50d-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9d50d-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9d50d-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="9d50d-139">ID dell'applicazione gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d50d-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9d50d-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9d50d-140">-RuleType</span></span>
<span data-ttu-id="9d50d-141">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9d50d-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="9d50d-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="9d50d-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="9d50d-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="9d50d-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="9d50d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d50d-144">CommonParameters</span></span>
<span data-ttu-id="9d50d-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d50d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d50d-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d50d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d50d-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d50d-147">INPUTS</span></span>

### <span data-ttu-id="9d50d-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d50d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d50d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d50d-149">OUTPUTS</span></span>

### <span data-ttu-id="9d50d-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d50d-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d50d-151">Note</span><span class="sxs-lookup"><span data-stu-id="9d50d-151">NOTES</span></span>

## <span data-ttu-id="9d50d-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d50d-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d50d-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d50d-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d50d-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d50d-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d50d-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d50d-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9d50d-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9d50d-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


