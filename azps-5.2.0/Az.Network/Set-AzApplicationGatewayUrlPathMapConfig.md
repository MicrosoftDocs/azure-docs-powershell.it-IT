---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371307"
---
# <span data-ttu-id="50ce4-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50ce4-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="50ce4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="50ce4-103">Imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="50ce4-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="50ce4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50ce4-104">SYNTAX</span></span>

### <span data-ttu-id="50ce4-105">BackendSetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50ce4-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50ce4-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50ce4-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50ce4-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="50ce4-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50ce4-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50ce4-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50ce4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ce4-109">DESCRIPTION</span></span>
<span data-ttu-id="50ce4-110">Il cmdlet **set-AzApplicationGatewayUrlPathMapConfig** imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="50ce4-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="50ce4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50ce4-111">EXAMPLES</span></span>

### <span data-ttu-id="50ce4-112">Esempio 1: aggiornare un mapping del percorso URL</span><span class="sxs-lookup"><span data-stu-id="50ce4-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="50ce4-113">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e archivia il risultato nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="50ce4-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="50ce4-114">Il secondo comando Aggiorna il mapping del percorso URL denominato map01 nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="50ce4-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="50ce4-115">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="50ce4-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="50ce4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ce4-116">PARAMETERS</span></span>

### <span data-ttu-id="50ce4-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50ce4-117">-ApplicationGateway</span></span>
<span data-ttu-id="50ce4-118">Specifica il gateway dell'applicazione a cui questo cmdlet imposta una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="50ce4-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="50ce4-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50ce4-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="50ce4-120">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="50ce4-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="50ce4-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="50ce4-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="50ce4-122">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="50ce4-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="50ce4-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="50ce4-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="50ce4-124">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="50ce4-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="50ce4-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="50ce4-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="50ce4-126">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="50ce4-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="50ce4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ce4-127">-DefaultProfile</span></span>
<span data-ttu-id="50ce4-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50ce4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50ce4-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="50ce4-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="50ce4-130">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="50ce4-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="50ce4-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="50ce4-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="50ce4-132">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="50ce4-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="50ce4-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50ce4-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="50ce4-134">Set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="50ce4-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="50ce4-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="50ce4-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="50ce4-136">ID del set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="50ce4-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="50ce4-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="50ce4-137">-Name</span></span>
<span data-ttu-id="50ce4-138">Specifica il nome della mappa percorso URL in cui questo cmdlet imposta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="50ce4-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="50ce4-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="50ce4-139">-PathRules</span></span>
<span data-ttu-id="50ce4-140">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="50ce4-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="50ce4-141">Tieni presente che le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="50ce4-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="50ce4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ce4-142">CommonParameters</span></span>
<span data-ttu-id="50ce4-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ce4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ce4-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ce4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ce4-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50ce4-145">INPUTS</span></span>

### <span data-ttu-id="50ce4-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50ce4-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50ce4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50ce4-147">OUTPUTS</span></span>

### <span data-ttu-id="50ce4-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50ce4-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50ce4-149">Note</span><span class="sxs-lookup"><span data-stu-id="50ce4-149">NOTES</span></span>

## <span data-ttu-id="50ce4-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50ce4-150">RELATED LINKS</span></span>

[<span data-ttu-id="50ce4-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50ce4-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="50ce4-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50ce4-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="50ce4-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50ce4-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="50ce4-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50ce4-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


