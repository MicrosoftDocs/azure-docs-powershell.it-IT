---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192866"
---
# <span data-ttu-id="0b0b2-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b0b2-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="0b0b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0b2-103">Aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0b0b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b0b2-104">SYNTAX</span></span>

### <span data-ttu-id="0b0b2-105">BackendSetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b0b2-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b0b2-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b0b2-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="0b0b2-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b0b2-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b0b2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b0b2-109">DESCRIPTION</span></span>
<span data-ttu-id="0b0b2-110">Il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="0b0b2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b0b2-111">EXAMPLES</span></span>

### <span data-ttu-id="0b0b2-112">Esempio 1: aggiungere il mapping di un percorso URL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="0b0b2-113">Il primo comando ottiene un gateway dell'applicazione denominato appGwName e lo archivia in $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="0b0b2-114">Il secondo comando ottiene il pool di indirizzi back-end e lo archivia in $pool variabile.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="0b0b2-115">Il terzo comando ottiene le impostazioni http di backend e lo archivia in $poolSettings variabile.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="0b0b2-116">Il quarto comando crea una nuova configurazione di regola di percorso denominata rule01 e la archivia in $pathRule variabile.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="0b0b2-117">Il quinto comando aggiunge la configurazione del mapping dei percorsi URL denominata url01 al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="0b0b2-118">Il sesto comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="0b0b2-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b0b2-119">PARAMETERS</span></span>

### <span data-ttu-id="0b0b2-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b0b2-120">-ApplicationGateway</span></span>
<span data-ttu-id="0b0b2-121">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="0b0b2-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0b0b2-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="0b0b2-123">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="0b0b2-125">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0b0b2-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="0b0b2-127">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="0b0b2-129">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0b2-130">-DefaultProfile</span></span>
<span data-ttu-id="0b0b2-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b0b2-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b0b2-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="0b0b2-133">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0b0b2-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="0b0b2-135">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b0b2-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b0b2-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="0b0b2-137">Set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0b0b2-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0b0b2-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="0b0b2-139">ID del set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0b0b2-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b0b2-140">-Name</span></span>
<span data-ttu-id="0b0b2-141">Specifica il nome della mappa percorso URL che questo cmdlet aggiunge al pool del server back-end.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="0b0b2-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="0b0b2-142">-PathRules</span></span>
<span data-ttu-id="0b0b2-143">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="0b0b2-144">Le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0b2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0b2-145">CommonParameters</span></span>
<span data-ttu-id="0b0b2-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0b2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0b2-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b0b2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0b2-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b0b2-148">INPUTS</span></span>

### <span data-ttu-id="0b0b2-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b0b2-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0b0b2-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b0b2-150">OUTPUTS</span></span>

### <span data-ttu-id="0b0b2-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b0b2-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0b0b2-152">Note</span><span class="sxs-lookup"><span data-stu-id="0b0b2-152">NOTES</span></span>

## <span data-ttu-id="0b0b2-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b0b2-153">RELATED LINKS</span></span>

[<span data-ttu-id="0b0b2-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b0b2-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0b0b2-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b0b2-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0b0b2-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b0b2-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0b0b2-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b0b2-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

