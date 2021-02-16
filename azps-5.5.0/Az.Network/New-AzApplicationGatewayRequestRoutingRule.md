---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202888"
---
# <span data-ttu-id="86adf-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="86adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86adf-102">SYNOPSIS</span></span>
<span data-ttu-id="86adf-103">Crea una regola di routing delle richieste per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="86adf-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="86adf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86adf-104">SYNTAX</span></span>

### <span data-ttu-id="86adf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="86adf-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86adf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="86adf-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86adf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86adf-107">DESCRIPTION</span></span>
<span data-ttu-id="86adf-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** crea una regola di routing delle richieste per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="86adf-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="86adf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86adf-109">EXAMPLES</span></span>

### <span data-ttu-id="86adf-110">Esempio 1: Creare una regola di routing delle richieste per un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="86adf-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="86adf-111">Questo comando crea una regola di routing delle richieste di base denominata Rule01 e archivia il risultato nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="86adf-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="86adf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86adf-112">PARAMETERS</span></span>

### <span data-ttu-id="86adf-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="86adf-113">-BackendAddressPool</span></span>
<span data-ttu-id="86adf-114">Specifica il pool di indirizzi back-end come oggetto per la creazione della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="86adf-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="86adf-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="86adf-116">Specifica l'ID pool di indirizzi back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="86adf-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="86adf-117">-BackendHttpSettings</span></span>
<span data-ttu-id="86adf-118">Specifica le impostazioni HTTP di back-end come oggetto per la creazione della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="86adf-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="86adf-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="86adf-120">Specifica l'ID delle impostazioni HTTP back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="86adf-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86adf-121">-DefaultProfile</span></span>
<span data-ttu-id="86adf-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86adf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86adf-123">-Http Listener</span><span class="sxs-lookup"><span data-stu-id="86adf-123">-HttpListener</span></span>
<span data-ttu-id="86adf-124">Specifica il listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="86adf-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-125">-HttpDirId</span><span class="sxs-lookup"><span data-stu-id="86adf-125">-HttpListenerId</span></span>
<span data-ttu-id="86adf-126">Specifica l'ID del listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="86adf-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="86adf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="86adf-127">-Name</span></span>
<span data-ttu-id="86adf-128">Specifica il nome della regola di routing delle richieste creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86adf-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="86adf-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="86adf-129">-Priority</span></span>
<span data-ttu-id="86adf-130">Priorità della regola</span><span class="sxs-lookup"><span data-stu-id="86adf-130">The priority of the rule</span></span>

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

### <span data-ttu-id="86adf-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="86adf-131">-RedirectConfiguration</span></span>
<span data-ttu-id="86adf-132">RedirectConfiguration del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="86adf-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="86adf-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="86adf-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="86adf-134">ID del gateway applicazione RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="86adf-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="86adf-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86adf-135">-RewriteRuleSet</span></span>
<span data-ttu-id="86adf-136">RewriteRuleSet del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="86adf-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="86adf-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="86adf-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="86adf-138">ID del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86adf-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="86adf-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="86adf-139">-RuleType</span></span>
<span data-ttu-id="86adf-140">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="86adf-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="86adf-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="86adf-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="86adf-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="86adf-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="86adf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86adf-143">CommonParameters</span></span>
<span data-ttu-id="86adf-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86adf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86adf-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86adf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86adf-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="86adf-146">INPUTS</span></span>

### <span data-ttu-id="86adf-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86adf-147">None</span></span>

## <span data-ttu-id="86adf-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86adf-148">OUTPUTS</span></span>

### <span data-ttu-id="86adf-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="86adf-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="86adf-150">NOTES</span></span>

## <span data-ttu-id="86adf-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86adf-151">RELATED LINKS</span></span>

[<span data-ttu-id="86adf-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86adf-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86adf-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86adf-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86adf-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


