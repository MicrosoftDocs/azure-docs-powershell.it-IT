---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300637"
---
# <span data-ttu-id="37516-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37516-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="37516-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37516-102">SYNOPSIS</span></span>
<span data-ttu-id="37516-103">Crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-103">Creates an application gateway.</span></span>

## <span data-ttu-id="37516-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37516-104">SYNTAX</span></span>

### <span data-ttu-id="37516-105">IdentityByUserAssignedIdentityId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37516-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37516-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="37516-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37516-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="37516-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37516-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="37516-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37516-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37516-109">DESCRIPTION</span></span>
<span data-ttu-id="37516-110">Il cmdlet **New-AzApplicationGateway** crea un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="37516-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="37516-111">Un gateway applicazione richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="37516-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="37516-112">Un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37516-112">A resource group.</span></span>
- <span data-ttu-id="37516-113">Una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37516-113">A virtual network.</span></span>
- <span data-ttu-id="37516-114">Un pool di server back-end contenente gli indirizzi IP dei server back-end.</span><span class="sxs-lookup"><span data-stu-id="37516-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="37516-115">Impostazioni del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="37516-115">Back-end server pool settings.</span></span> <span data-ttu-id="37516-116">Ogni pool include impostazioni come la porta, il protocollo e l'affinità basata su cookie, che vengono applicati a tutti i server all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="37516-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="37516-117">Indirizzi IP front-end, ovvero gli indirizzi IP aperti nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="37516-118">Un indirizzo IP front-end può essere un indirizzo IP pubblico o un indirizzo IP interno.</span><span class="sxs-lookup"><span data-stu-id="37516-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="37516-119">Porte front-end, che sono le porte pubbliche aperte nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="37516-120">Il traffico che colpisce queste porte viene reindirizzato ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="37516-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="37516-121">Regola di routing delle richieste che associa il listener e il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="37516-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="37516-122">La regola definisce il pool di server back-end a cui il traffico deve essere indirizzato quando colpisce un determinato listener.</span><span class="sxs-lookup"><span data-stu-id="37516-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="37516-123">Un listener ha una porta front-end, un indirizzo IP front-end, un protocollo (HTTP o HTTPS) e un nome di certificato SSL (Secure Sockets Layer) (se si configura SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="37516-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="37516-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37516-124">EXAMPLES</span></span>

### <span data-ttu-id="37516-125">Esempio 1: creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="37516-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="37516-126">L'esempio seguente crea un gateway dell'applicazione creando prima di tutto un gruppo di risorse e una rete virtuale, nonché le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="37516-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="37516-127">Un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="37516-127">A back-end server pool</span></span>
- <span data-ttu-id="37516-128">Impostazioni del pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="37516-128">Back-end server pool settings</span></span>
- <span data-ttu-id="37516-129">Porte front-end</span><span class="sxs-lookup"><span data-stu-id="37516-129">Front-end ports</span></span>
- <span data-ttu-id="37516-130">Indirizzi IP front-end</span><span class="sxs-lookup"><span data-stu-id="37516-130">Front-end IP addresses</span></span>
- <span data-ttu-id="37516-131">Regola di routing delle richieste questi quattro comandi creano una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37516-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="37516-132">Il primo comando crea una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="37516-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="37516-133">Il secondo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37516-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="37516-134">Il terzo comando verifica la configurazione della subnet e il quarto comando verifica che la rete virtuale venga creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="37516-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="37516-135">I comandi seguenti creano il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="37516-136">Il primo comando crea una configurazione IP denominata GatewayIp01 per la subnet creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="37516-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="37516-137">Il secondo comando crea un pool di server back-end denominato Pool01 con un elenco di indirizzi IP di back-end e archivia il pool nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="37516-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="37516-138">Il terzo comando crea le impostazioni per il pool di server back-end e archivia le impostazioni nella variabile $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="37516-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="37516-139">Il comando Forth crea una porta front-end sulla porta 80, la chiama FrontEndPort01 e archivia la porta nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="37516-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="37516-140">Il quinto comando crea un indirizzo IP pubblico usando New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="37516-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="37516-141">Il sesto comando crea una configurazione IP front-end usando $PublicIp, la chiama FrontEndPortConfig01 e la memorizza nella variabile $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="37516-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="37516-142">Il settimo comando crea un listener usando il $FrontEndPort $FrontEndIpConfig creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="37516-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="37516-143">L'ottavo comando crea una regola per il listener.</span><span class="sxs-lookup"><span data-stu-id="37516-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="37516-144">Il nono comando imposta l'USK.</span><span class="sxs-lookup"><span data-stu-id="37516-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="37516-145">Il decimo comando crea il gateway usando gli oggetti impostati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="37516-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="37516-146">Esempio 2: creare un gateway dell'applicazione con l'identità UserAssigned</span><span class="sxs-lookup"><span data-stu-id="37516-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="37516-147">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37516-147">PARAMETERS</span></span>

### <span data-ttu-id="37516-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37516-148">-AsJob</span></span>
<span data-ttu-id="37516-149">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="37516-149">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="37516-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="37516-151">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="37516-153">Configurazione di scala automatica</span><span class="sxs-lookup"><span data-stu-id="37516-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="37516-154">-BackendAddressPools</span></span>
<span data-ttu-id="37516-155">Specifica l'elenco dei pool di indirizzi back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="37516-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="37516-157">Specifica l'elenco delle impostazioni HTTP di back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="37516-159">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="37516-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37516-160">-DefaultProfile</span></span>
<span data-ttu-id="37516-161">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37516-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="37516-162">-EnableFIPS</span></span>
<span data-ttu-id="37516-163">Se FIPS è abilitato.</span><span class="sxs-lookup"><span data-stu-id="37516-163">Whether FIPS is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="37516-164">-EnableHttp2</span></span>
<span data-ttu-id="37516-165">Se HTTP2 è abilitato.</span><span class="sxs-lookup"><span data-stu-id="37516-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="37516-166">-FirewallPolicy</span></span>
<span data-ttu-id="37516-167">Configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="37516-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="37516-168">-FirewallPolicyId</span></span>
<span data-ttu-id="37516-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="37516-169">FirewallPolicyId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-170">-Force</span><span class="sxs-lookup"><span data-stu-id="37516-170">-Force</span></span>
<span data-ttu-id="37516-171">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="37516-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="37516-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="37516-173">Se Force firewallPolicy Association è abilitato.</span><span class="sxs-lookup"><span data-stu-id="37516-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="37516-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="37516-175">Specifica un elenco di configurazioni IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="37516-176">-FrontendPorts</span></span>
<span data-ttu-id="37516-177">Specifica un elenco di porte front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="37516-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="37516-179">Specifica un elenco di configurazioni IP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="37516-180">-HttpListeners</span></span>
<span data-ttu-id="37516-181">Specifica un elenco di listener HTTP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-182">-Identità</span><span class="sxs-lookup"><span data-stu-id="37516-182">-Identity</span></span>
<span data-ttu-id="37516-183">Identità del gateway dell'applicazione da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-184">-Posizione</span><span class="sxs-lookup"><span data-stu-id="37516-184">-Location</span></span>
<span data-ttu-id="37516-185">Specifica l'area geografica in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-186">-Nome</span><span class="sxs-lookup"><span data-stu-id="37516-186">-Name</span></span>
<span data-ttu-id="37516-187">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-187">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="37516-189">L'elenco della configurazione di privateLink</span><span class="sxs-lookup"><span data-stu-id="37516-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-190">-Sonde</span><span class="sxs-lookup"><span data-stu-id="37516-190">-Probes</span></span>
<span data-ttu-id="37516-191">Specifica le sonde per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="37516-192">-RedirectConfigurations</span></span>
<span data-ttu-id="37516-193">Elenco della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="37516-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="37516-194">-RequestRoutingRules</span></span>
<span data-ttu-id="37516-195">Specifica un elenco di regole di routing delle richieste per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37516-196">-ResourceGroupName</span></span>
<span data-ttu-id="37516-197">Specifica il nome del gruppo di risorse in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37516-198">-RewriteRuleSet</span></span>
<span data-ttu-id="37516-199">Elenco di RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37516-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="37516-200">-Sku</span></span>
<span data-ttu-id="37516-201">Specifica l'unità di conservazione delle scorte (SKU) del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="37516-202">-SslCertificates</span></span>
<span data-ttu-id="37516-203">Specifica l'elenco dei certificati SSL (Secure Sockets Layer) per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="37516-204">-SslPolicy</span></span>
<span data-ttu-id="37516-205">Specifica un criterio SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-206">-Tag</span><span class="sxs-lookup"><span data-stu-id="37516-206">-Tag</span></span>
<span data-ttu-id="37516-207">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="37516-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="37516-208">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="37516-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="37516-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="37516-210">Elenco dei certificati radice attendibili</span><span class="sxs-lookup"><span data-stu-id="37516-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="37516-211">-UrlPathMaps</span></span>
<span data-ttu-id="37516-212">Specifica le mappe Path URL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="37516-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="37516-214">ResourceId dell'identità assegnata dall'utente da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="37516-216">Specifica una configurazione WAF (Web Application Firewall).</span><span class="sxs-lookup"><span data-stu-id="37516-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="37516-217">Puoi usare il cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration per ottenere un WAF.</span><span class="sxs-lookup"><span data-stu-id="37516-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-218">-Zona</span><span class="sxs-lookup"><span data-stu-id="37516-218">-Zone</span></span>
<span data-ttu-id="37516-219">Elenco delle aree di disponibilità che indicano da dove deve provenire il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37516-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-220">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37516-220">-Confirm</span></span>
<span data-ttu-id="37516-221">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37516-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37516-222">-WhatIf</span></span>
<span data-ttu-id="37516-223">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37516-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37516-224">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37516-224">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37516-225">CommonParameters</span></span>
<span data-ttu-id="37516-226">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37516-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37516-227">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37516-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37516-228">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37516-228">INPUTS</span></span>

### <span data-ttu-id="37516-229">System. String</span><span class="sxs-lookup"><span data-stu-id="37516-229">System.String</span></span>

### <span data-ttu-id="37516-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="37516-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="37516-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="37516-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="37516-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="37516-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="37516-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="37516-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="37516-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="37516-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="37516-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="37516-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="37516-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="37516-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="37516-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="37516-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="37516-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="37516-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="37516-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="37516-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="37516-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="37516-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="37516-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="37516-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="37516-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="37516-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="37516-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="37516-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="37516-244">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="37516-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="37516-245">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="37516-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="37516-246">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="37516-247">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="37516-248">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="37516-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="37516-249">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="37516-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="37516-250">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37516-250">OUTPUTS</span></span>

### <span data-ttu-id="37516-251">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37516-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37516-252">Note</span><span class="sxs-lookup"><span data-stu-id="37516-252">NOTES</span></span>

## <span data-ttu-id="37516-253">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37516-253">RELATED LINKS</span></span>

[<span data-ttu-id="37516-254">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="37516-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="37516-255">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="37516-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="37516-256">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="37516-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="37516-257">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37516-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="37516-258">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37516-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="37516-259">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="37516-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="37516-260">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37516-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="37516-261">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="37516-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="37516-262">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37516-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="37516-263">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="37516-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
