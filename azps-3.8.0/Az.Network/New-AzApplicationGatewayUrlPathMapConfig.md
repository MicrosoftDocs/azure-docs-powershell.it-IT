---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022727"
---
# <span data-ttu-id="4b0dd-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b0dd-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4b0dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0dd-103">Crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4b0dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b0dd-104">SYNTAX</span></span>

### <span data-ttu-id="4b0dd-105">BackendSetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b0dd-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b0dd-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b0dd-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="4b0dd-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b0dd-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b0dd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b0dd-109">DESCRIPTION</span></span>
<span data-ttu-id="4b0dd-110">Il cmdlet **New-AzApplicationGatewayUrlPathMapConfig** crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4b0dd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b0dd-111">EXAMPLES</span></span>

### <span data-ttu-id="4b0dd-112">Esempio 1: creare una matrice di mapping dei percorsi URL in un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="4b0dd-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="4b0dd-113">Questo comando crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4b0dd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b0dd-114">PARAMETERS</span></span>

### <span data-ttu-id="4b0dd-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0dd-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4b0dd-116">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4b0dd-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4b0dd-118">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="4b0dd-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4b0dd-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4b0dd-120">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4b0dd-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4b0dd-122">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="4b0dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0dd-123">-DefaultProfile</span></span>
<span data-ttu-id="4b0dd-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b0dd-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b0dd-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4b0dd-126">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4b0dd-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4b0dd-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4b0dd-128">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b0dd-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4b0dd-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b0dd-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="4b0dd-130">Set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4b0dd-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="4b0dd-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="4b0dd-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="4b0dd-132">ID del set di regole di riscrittura predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4b0dd-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="4b0dd-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b0dd-133">-Name</span></span>
<span data-ttu-id="4b0dd-134">Specifica il nome della mappa percorso URL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4b0dd-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4b0dd-135">-PathRules</span></span>
<span data-ttu-id="4b0dd-136">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="4b0dd-137">Tieni presente che le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="4b0dd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0dd-138">CommonParameters</span></span>
<span data-ttu-id="4b0dd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0dd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0dd-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0dd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0dd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b0dd-141">INPUTS</span></span>

### <span data-ttu-id="4b0dd-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4b0dd-142">None</span></span>

## <span data-ttu-id="4b0dd-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b0dd-143">OUTPUTS</span></span>

### <span data-ttu-id="4b0dd-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="4b0dd-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="4b0dd-145">Note</span><span class="sxs-lookup"><span data-stu-id="4b0dd-145">NOTES</span></span>

## <span data-ttu-id="4b0dd-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b0dd-146">RELATED LINKS</span></span>

[<span data-ttu-id="4b0dd-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b0dd-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4b0dd-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b0dd-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4b0dd-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b0dd-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4b0dd-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b0dd-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


