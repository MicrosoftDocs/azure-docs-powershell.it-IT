---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cc2a30e5a5633dcda345184bef121befe710ad8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952141"
---
# <span data-ttu-id="07380-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07380-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="07380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07380-102">SYNOPSIS</span></span>
<span data-ttu-id="07380-103">Imposta la configurazione per una matrice di mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="07380-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="07380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07380-104">SYNTAX</span></span>

### <span data-ttu-id="07380-105">BackendSetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07380-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07380-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07380-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07380-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="07380-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07380-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07380-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07380-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="07380-109">DESCRIPTION</span></span>
<span data-ttu-id="07380-110">Il cmdlet **Set-AzApplicationGatewayUrlPathMapConfig** imposta la configurazione per una matrice di mapping del percorso URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="07380-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="07380-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07380-111">EXAMPLES</span></span>

### <span data-ttu-id="07380-112">Esempio 1: Aggiornare un mapping del percorso URL</span><span class="sxs-lookup"><span data-stu-id="07380-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="07380-113">Il primo comando recupera il gateway applicazione denominato appGwName e archivia il risultato nella $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="07380-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="07380-114">Il secondo comando aggiorna il mapping del percorso URL denominato map01 nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="07380-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="07380-115">Il terzo comando aggiorna il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="07380-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="07380-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07380-116">PARAMETERS</span></span>

### <span data-ttu-id="07380-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07380-117">-ApplicationGateway</span></span>
<span data-ttu-id="07380-118">Specifica il gateway applicazione su cui questo cmdlet imposta una configurazione della mappa del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="07380-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="07380-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="07380-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="07380-120">Specifica il pool di indirizzi back-end predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="07380-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="07380-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="07380-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="07380-122">Specifica l'ID pool di indirizzi back-end predefinito.</span><span class="sxs-lookup"><span data-stu-id="07380-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="07380-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="07380-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="07380-124">Specifica le impostazioni HTTP back-end predefinite da usare nel caso nessuna delle regole specificate nella corrispondenza del parametro *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="07380-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="07380-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="07380-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="07380-126">Specifica l'ID delle impostazioni HTTP back-end predefinito.</span><span class="sxs-lookup"><span data-stu-id="07380-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="07380-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07380-127">-DefaultProfile</span></span>
<span data-ttu-id="07380-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07380-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07380-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="07380-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="07380-130">RedirectConfiguration predefinita del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="07380-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="07380-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="07380-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="07380-132">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="07380-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="07380-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07380-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="07380-134">Set di regole di riscrittura predefinito di Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="07380-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="07380-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="07380-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="07380-136">ID del set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="07380-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="07380-137">-Name</span><span class="sxs-lookup"><span data-stu-id="07380-137">-Name</span></span>
<span data-ttu-id="07380-138">Specifica il nome della mappa del percorso URL per cui questo cmdlet imposta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="07380-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="07380-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="07380-139">-PathRules</span></span>
<span data-ttu-id="07380-140">Specifica un elenco di regole percorso.</span><span class="sxs-lookup"><span data-stu-id="07380-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="07380-141">Si noti che le regole per i percorsi sono sensibili all'ordine e vengono applicate nell'ordine in cui sono specificate.</span><span class="sxs-lookup"><span data-stu-id="07380-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="07380-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07380-142">CommonParameters</span></span>
<span data-ttu-id="07380-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07380-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07380-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07380-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07380-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="07380-145">INPUTS</span></span>

### <span data-ttu-id="07380-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07380-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07380-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07380-147">OUTPUTS</span></span>

### <span data-ttu-id="07380-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07380-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07380-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="07380-149">NOTES</span></span>

## <span data-ttu-id="07380-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07380-150">RELATED LINKS</span></span>

[<span data-ttu-id="07380-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07380-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="07380-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07380-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="07380-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07380-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="07380-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="07380-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


