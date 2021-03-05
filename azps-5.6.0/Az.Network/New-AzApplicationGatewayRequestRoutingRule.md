---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010333"
---
# <span data-ttu-id="52abe-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="52abe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52abe-102">SYNOPSIS</span></span>
<span data-ttu-id="52abe-103">Crea una regola di routing delle richieste per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="52abe-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="52abe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52abe-104">SYNTAX</span></span>

### <span data-ttu-id="52abe-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="52abe-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52abe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="52abe-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52abe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52abe-107">DESCRIPTION</span></span>
<span data-ttu-id="52abe-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** crea una regola di routing delle richieste per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="52abe-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="52abe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52abe-109">EXAMPLES</span></span>

### <span data-ttu-id="52abe-110">Esempio 1: Creare una regola di routing delle richieste per un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="52abe-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="52abe-111">Questo comando crea una regola di routing delle richieste di base denominata Rule01 e archivia il risultato nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="52abe-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="52abe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52abe-112">PARAMETERS</span></span>

### <span data-ttu-id="52abe-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52abe-113">-BackendAddressPool</span></span>
<span data-ttu-id="52abe-114">Specifica il pool di indirizzi back-end come oggetto per la creazione della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="52abe-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="52abe-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="52abe-116">Specifica l'ID pool di indirizzi back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="52abe-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52abe-117">-BackendHttpSettings</span></span>
<span data-ttu-id="52abe-118">Specifica le impostazioni HTTP back-end come oggetto per la creazione della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="52abe-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="52abe-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="52abe-120">Specifica l'ID delle impostazioni HTTP back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="52abe-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52abe-121">-DefaultProfile</span></span>
<span data-ttu-id="52abe-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52abe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52abe-123">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="52abe-123">-HttpListener</span></span>
<span data-ttu-id="52abe-124">Specifica il listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="52abe-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-125">-HttpDirId</span><span class="sxs-lookup"><span data-stu-id="52abe-125">-HttpListenerId</span></span>
<span data-ttu-id="52abe-126">Specifica l'ID del listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="52abe-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="52abe-127">-Name</span><span class="sxs-lookup"><span data-stu-id="52abe-127">-Name</span></span>
<span data-ttu-id="52abe-128">Specifica il nome della regola di routing delle richieste creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52abe-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="52abe-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="52abe-129">-Priority</span></span>
<span data-ttu-id="52abe-130">Priorità della regola</span><span class="sxs-lookup"><span data-stu-id="52abe-130">The priority of the rule</span></span>

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

### <span data-ttu-id="52abe-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="52abe-131">-RedirectConfiguration</span></span>
<span data-ttu-id="52abe-132">RedirectConfiguration del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="52abe-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="52abe-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="52abe-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="52abe-134">ID del gateway applicazione RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="52abe-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="52abe-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="52abe-135">-RewriteRuleSet</span></span>
<span data-ttu-id="52abe-136">RewriteRuleSet del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="52abe-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="52abe-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="52abe-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="52abe-138">ID del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="52abe-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="52abe-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="52abe-139">-RuleType</span></span>
<span data-ttu-id="52abe-140">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="52abe-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="52abe-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="52abe-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="52abe-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="52abe-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="52abe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52abe-143">CommonParameters</span></span>
<span data-ttu-id="52abe-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52abe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52abe-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52abe-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52abe-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="52abe-146">INPUTS</span></span>

### <span data-ttu-id="52abe-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="52abe-147">None</span></span>

## <span data-ttu-id="52abe-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52abe-148">OUTPUTS</span></span>

### <span data-ttu-id="52abe-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="52abe-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="52abe-150">NOTES</span></span>

## <span data-ttu-id="52abe-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52abe-151">RELATED LINKS</span></span>

[<span data-ttu-id="52abe-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="52abe-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="52abe-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="52abe-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="52abe-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


