---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 82f14ce9418566793572e2b5722d09460ab1e827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853558"
---
# <span data-ttu-id="16adc-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="16adc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16adc-102">SYNOPSIS</span></span>
<span data-ttu-id="16adc-103">Crea una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="16adc-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="16adc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16adc-104">SYNTAX</span></span>

### <span data-ttu-id="16adc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="16adc-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16adc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="16adc-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16adc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16adc-107">DESCRIPTION</span></span>
<span data-ttu-id="16adc-108">**Il cmdlet Add-AzApplicationGatewayRequestRoutingRule** crea una regola di routing delle richieste per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="16adc-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="16adc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16adc-109">EXAMPLES</span></span>

### <span data-ttu-id="16adc-110">Esempio 1: creare una regola di routing delle richieste per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="16adc-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="16adc-111">Questo comando crea una regola di routing delle richieste di base denominata Rule01 e archivia il risultato nella variabile denominata $Rule.</span><span class="sxs-lookup"><span data-stu-id="16adc-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="16adc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16adc-112">PARAMETERS</span></span>

### <span data-ttu-id="16adc-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16adc-113">-BackendAddressPool</span></span>
<span data-ttu-id="16adc-114">Specifica il pool di indirizzi back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="16adc-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="16adc-116">Specifica l'ID del pool di indirizzi back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16adc-117">-BackendHttpSettings</span></span>
<span data-ttu-id="16adc-118">Specifica le impostazioni HTTP di back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="16adc-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="16adc-120">Specifica l'ID delle impostazioni HTTP back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16adc-121">-DefaultProfile</span></span>
<span data-ttu-id="16adc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16adc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16adc-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="16adc-123">-HttpListener</span></span>
<span data-ttu-id="16adc-124">Specifica il listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="16adc-125">-HttpListenerId</span></span>
<span data-ttu-id="16adc-126">Specifica l'ID del listener HTTP di backend per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="16adc-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="16adc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="16adc-127">-Name</span></span>
<span data-ttu-id="16adc-128">Specifica il nome della regola di routing delle richieste creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16adc-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="16adc-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="16adc-129">-RedirectConfiguration</span></span>
<span data-ttu-id="16adc-130">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="16adc-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="16adc-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16adc-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="16adc-132">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="16adc-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="16adc-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="16adc-133">-RewriteRuleSet</span></span>
<span data-ttu-id="16adc-134">App gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="16adc-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="16adc-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="16adc-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="16adc-136">ID dell'applicazione gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="16adc-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="16adc-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="16adc-137">-RuleType</span></span>
<span data-ttu-id="16adc-138">Specifica il tipo della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="16adc-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="16adc-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="16adc-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="16adc-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="16adc-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="16adc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16adc-141">CommonParameters</span></span>
<span data-ttu-id="16adc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16adc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16adc-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16adc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16adc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16adc-144">INPUTS</span></span>

### <span data-ttu-id="16adc-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16adc-145">None</span></span>

## <span data-ttu-id="16adc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16adc-146">OUTPUTS</span></span>

### <span data-ttu-id="16adc-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="16adc-148">Note</span><span class="sxs-lookup"><span data-stu-id="16adc-148">NOTES</span></span>

## <span data-ttu-id="16adc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16adc-149">RELATED LINKS</span></span>

[<span data-ttu-id="16adc-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16adc-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16adc-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16adc-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16adc-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


