---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ebb73225a8afa7bb4c1061326aa9262dd46d9dc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011886"
---
# <span data-ttu-id="838d9-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="838d9-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="838d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="838d9-102">SYNOPSIS</span></span>
<span data-ttu-id="838d9-103">Crea una matrice di mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="838d9-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="838d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="838d9-104">SYNTAX</span></span>

### <span data-ttu-id="838d9-105">BackendSetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="838d9-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="838d9-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="838d9-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838d9-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="838d9-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838d9-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="838d9-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="838d9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="838d9-109">DESCRIPTION</span></span>
<span data-ttu-id="838d9-110">Il cmdlet **New-AzApplicationGatewayUrlPathMapConfig** crea una matrice di mapping del percorso URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="838d9-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="838d9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="838d9-111">EXAMPLES</span></span>

### <span data-ttu-id="838d9-112">Esempio 1: Creare una matrice di mapping del percorso URL a un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="838d9-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="838d9-113">Questo comando crea una matrice di mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="838d9-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="838d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="838d9-114">PARAMETERS</span></span>

### <span data-ttu-id="838d9-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="838d9-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="838d9-116">Specifica il pool di indirizzi back-end predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="838d9-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="838d9-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="838d9-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="838d9-118">Specifica l'ID pool di indirizzi back-end predefinito.</span><span class="sxs-lookup"><span data-stu-id="838d9-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="838d9-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="838d9-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="838d9-120">Specifica le impostazioni HTTP back-end predefinite da usare nel caso nessuna delle regole specificate nella corrispondenza del parametro *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="838d9-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="838d9-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="838d9-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="838d9-122">Specifica l'ID delle impostazioni HTTP back-end predefinito.</span><span class="sxs-lookup"><span data-stu-id="838d9-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="838d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838d9-123">-DefaultProfile</span></span>
<span data-ttu-id="838d9-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="838d9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="838d9-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="838d9-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="838d9-126">RedirectConfiguration predefinita del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="838d9-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="838d9-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="838d9-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="838d9-128">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="838d9-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="838d9-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="838d9-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="838d9-130">Set di regole di riscrittura predefinito di Gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="838d9-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="838d9-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="838d9-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="838d9-132">ID del set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="838d9-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="838d9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="838d9-133">-Name</span></span>
<span data-ttu-id="838d9-134">Specifica il nome della mappa del percorso URL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="838d9-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="838d9-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="838d9-135">-PathRules</span></span>
<span data-ttu-id="838d9-136">Specifica un elenco di regole percorso.</span><span class="sxs-lookup"><span data-stu-id="838d9-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="838d9-137">Si noti che le regole per i percorsi sono sensibili all'ordine e vengono applicate nell'ordine in cui sono specificate.</span><span class="sxs-lookup"><span data-stu-id="838d9-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="838d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838d9-138">CommonParameters</span></span>
<span data-ttu-id="838d9-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838d9-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838d9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838d9-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="838d9-141">INPUTS</span></span>

### <span data-ttu-id="838d9-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="838d9-142">None</span></span>

## <span data-ttu-id="838d9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="838d9-143">OUTPUTS</span></span>

### <span data-ttu-id="838d9-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="838d9-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="838d9-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="838d9-145">NOTES</span></span>

## <span data-ttu-id="838d9-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="838d9-146">RELATED LINKS</span></span>

[<span data-ttu-id="838d9-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="838d9-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="838d9-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="838d9-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="838d9-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="838d9-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="838d9-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="838d9-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


