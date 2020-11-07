---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1bde6608f5dd87c2c102f3f2957832a2eb41e50a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853610"
---
# <span data-ttu-id="9b7b2-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b2-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="9b7b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7b2-103">Crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-103">Creates an application gateway.</span></span>

## <span data-ttu-id="9b7b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b7b2-104">SYNTAX</span></span>

### <span data-ttu-id="9b7b2-105">IdentityByUserAssignedIdentityId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b7b2-105">IdentityByUserAssignedIdentityId (Default)</span></span>
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
 [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7b2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b7b2-106">SetByResourceId</span></span>
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
 [-EnableHttp2] [-EnableFIPS] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7b2-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b7b2-107">SetByResource</span></span>
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
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7b2-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="9b7b2-108">IdentityByIdentityObject</span></span>
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
 [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity> [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b7b2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b7b2-109">DESCRIPTION</span></span>
<span data-ttu-id="9b7b2-110">Il cmdlet **New-AzApplicationGateway** crea un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="9b7b2-111">Un gateway applicazione richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b7b2-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="9b7b2-112">Un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-112">A resource group.</span></span>
- <span data-ttu-id="9b7b2-113">Una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-113">A virtual network.</span></span>
- <span data-ttu-id="9b7b2-114">Un pool di server back-end contenente gli indirizzi IP dei server back-end.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="9b7b2-115">Impostazioni del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-115">Back-end server pool settings.</span></span> <span data-ttu-id="9b7b2-116">Ogni pool include impostazioni come la porta, il protocollo e l'affinità basata su cookie, che vengono applicati a tutti i server all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="9b7b2-117">Indirizzi IP front-end, ovvero gli indirizzi IP aperti nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="9b7b2-118">Un indirizzo IP front-end può essere un indirizzo IP pubblico o un indirizzo IP interno.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="9b7b2-119">Porte front-end, che sono le porte pubbliche aperte nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="9b7b2-120">Il traffico che colpisce queste porte viene reindirizzato ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="9b7b2-121">Regola di routing delle richieste che associa il listener e il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="9b7b2-122">La regola definisce il pool di server back-end a cui il traffico deve essere indirizzato quando colpisce un determinato listener.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="9b7b2-123">Un listener ha una porta front-end, un indirizzo IP front-end, un protocollo (HTTP o HTTPS) e un nome di certificato SSL (Secure Sockets Layer) (se si configura SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="9b7b2-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b7b2-124">EXAMPLES</span></span>

### <span data-ttu-id="9b7b2-125">Esempio 1: creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9b7b2-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="9b7b2-126">L'esempio seguente crea un gateway dell'applicazione creando prima di tutto un gruppo di risorse e una rete virtuale, nonché le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b7b2-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="9b7b2-127">Un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="9b7b2-127">A back-end server pool</span></span>
- <span data-ttu-id="9b7b2-128">Impostazioni del pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="9b7b2-128">Back-end server pool settings</span></span>
- <span data-ttu-id="9b7b2-129">Porte front-end</span><span class="sxs-lookup"><span data-stu-id="9b7b2-129">Front-end ports</span></span>
- <span data-ttu-id="9b7b2-130">Indirizzi IP front-end</span><span class="sxs-lookup"><span data-stu-id="9b7b2-130">Front-end IP addresses</span></span>
- <span data-ttu-id="9b7b2-131">Regola di routing delle richieste questi quattro comandi creano una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="9b7b2-132">Il primo comando crea una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="9b7b2-133">Il secondo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="9b7b2-134">Il terzo comando verifica la configurazione della subnet e il quarto comando verifica che la rete virtuale venga creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="9b7b2-135">I comandi seguenti creano il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="9b7b2-136">Il primo comando crea una configurazione IP denominata GatewayIp01 per la subnet creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="9b7b2-137">Il secondo comando crea un pool di server back-end denominato Pool01 con un elenco di indirizzi IP di back-end e archivia il pool nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="9b7b2-138">Il terzo comando crea le impostazioni per il pool di server back-end e archivia le impostazioni nella variabile $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="9b7b2-139">Il comando Forth crea una porta front-end sulla porta 80, la chiama FrontEndPort01 e archivia la porta nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="9b7b2-140">Il quinto comando crea un indirizzo IP pubblico usando New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="9b7b2-141">Il sesto comando crea una configurazione IP front-end usando $PublicIp, la chiama FrontEndPortConfig01 e la memorizza nella variabile $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="9b7b2-142">Il settimo comando crea un listener usando il $FrontEndPort $FrontEndIpConfig creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="9b7b2-143">L'ottavo comando crea una regola per il listener.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="9b7b2-144">Il nono comando imposta l'USK.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="9b7b2-145">Il decimo comando crea il gateway usando gli oggetti impostati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="9b7b2-146">Esempio 2: creare un gateway dell'applicazione con l'identità UserAssigned</span><span class="sxs-lookup"><span data-stu-id="9b7b2-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="9b7b2-147">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b7b2-147">PARAMETERS</span></span>

### <span data-ttu-id="9b7b2-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b7b2-148">-AsJob</span></span>
<span data-ttu-id="9b7b2-149">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b7b2-149">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="9b7b2-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="9b7b2-151">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="9b7b2-153">Configurazione di scala automatica</span><span class="sxs-lookup"><span data-stu-id="9b7b2-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="9b7b2-154">-BackendAddressPools</span></span>
<span data-ttu-id="9b7b2-155">Specifica l'elenco dei pool di indirizzi back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="9b7b2-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="9b7b2-157">Specifica l'elenco delle impostazioni HTTP di back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="9b7b2-159">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9b7b2-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7b2-160">-DefaultProfile</span></span>
<span data-ttu-id="9b7b2-161">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b7b2-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="9b7b2-162">-EnableFIPS</span></span>
<span data-ttu-id="9b7b2-163">Se FIPS è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-163">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="9b7b2-164">-EnableHttp2</span></span>
<span data-ttu-id="9b7b2-165">Se HTTP2 è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7b2-166">-FirewallPolicy</span></span>
<span data-ttu-id="9b7b2-167">Configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="9b7b2-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="9b7b2-168">-FirewallPolicyId</span></span>
<span data-ttu-id="9b7b2-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="9b7b2-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="9b7b2-170">-Force</span><span class="sxs-lookup"><span data-stu-id="9b7b2-170">-Force</span></span>
<span data-ttu-id="9b7b2-171">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-172">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="9b7b2-172">-FrontendIPConfigurations</span></span>
<span data-ttu-id="9b7b2-173">Specifica un elenco di configurazioni IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-173">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-174">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="9b7b2-174">-FrontendPorts</span></span>
<span data-ttu-id="9b7b2-175">Specifica un elenco di porte front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-175">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-176">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="9b7b2-176">-GatewayIPConfigurations</span></span>
<span data-ttu-id="9b7b2-177">Specifica un elenco di configurazioni IP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-177">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-178">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="9b7b2-178">-HttpListeners</span></span>
<span data-ttu-id="9b7b2-179">Specifica un elenco di listener HTTP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-179">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-180">-Identità</span><span class="sxs-lookup"><span data-stu-id="9b7b2-180">-Identity</span></span>
<span data-ttu-id="9b7b2-181">Identità del gateway dell'applicazione da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-181">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-182">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9b7b2-182">-Location</span></span>
<span data-ttu-id="9b7b2-183">Specifica l'area geografica in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-183">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-184">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b7b2-184">-Name</span></span>
<span data-ttu-id="9b7b2-185">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-185">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-186">-Sonde</span><span class="sxs-lookup"><span data-stu-id="9b7b2-186">-Probes</span></span>
<span data-ttu-id="9b7b2-187">Specifica le sonde per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-187">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-188">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="9b7b2-188">-RedirectConfigurations</span></span>
<span data-ttu-id="9b7b2-189">Elenco della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="9b7b2-189">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-190">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="9b7b2-190">-RequestRoutingRules</span></span>
<span data-ttu-id="9b7b2-191">Specifica un elenco di regole di routing delle richieste per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-191">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7b2-192">-ResourceGroupName</span></span>
<span data-ttu-id="9b7b2-193">Specifica il nome del gruppo di risorse in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-193">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-194">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b7b2-194">-RewriteRuleSet</span></span>
<span data-ttu-id="9b7b2-195">Elenco di RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b7b2-195">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-196">-SKU</span><span class="sxs-lookup"><span data-stu-id="9b7b2-196">-Sku</span></span>
<span data-ttu-id="9b7b2-197">Specifica l'unità di conservazione delle scorte (SKU) del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-197">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-198">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="9b7b2-198">-SslCertificates</span></span>
<span data-ttu-id="9b7b2-199">Specifica l'elenco dei certificati SSL (Secure Sockets Layer) per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-199">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-200">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7b2-200">-SslPolicy</span></span>
<span data-ttu-id="9b7b2-201">Specifica un criterio SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-201">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-202">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b7b2-202">-Tag</span></span>
<span data-ttu-id="9b7b2-203">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-203">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b7b2-204">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9b7b2-204">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-205">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b7b2-205">-TrustedRootCertificate</span></span>
<span data-ttu-id="9b7b2-206">Elenco dei certificati radice attendibili</span><span class="sxs-lookup"><span data-stu-id="9b7b2-206">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-207">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="9b7b2-207">-UrlPathMaps</span></span>
<span data-ttu-id="9b7b2-208">Specifica le mappe Path URL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-208">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-209">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="9b7b2-209">-UserAssignedIdentityId</span></span>
<span data-ttu-id="9b7b2-210">ResourceId dell'identità assegnata dall'utente da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-210">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-211">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-211">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="9b7b2-212">Specifica una configurazione WAF (Web Application Firewall).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-212">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="9b7b2-213">Puoi usare il cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration per ottenere un WAF.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-213">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-214">-Zona</span><span class="sxs-lookup"><span data-stu-id="9b7b2-214">-Zone</span></span>
<span data-ttu-id="9b7b2-215">Elenco delle aree di disponibilità che indicano da dove deve provenire il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-215">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-216">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b7b2-216">-Confirm</span></span>
<span data-ttu-id="9b7b2-217">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-217">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7b2-218">-WhatIf</span></span>
<span data-ttu-id="9b7b2-219">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b7b2-220">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-220">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b2-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7b2-221">CommonParameters</span></span>
<span data-ttu-id="9b7b2-222">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7b2-223">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7b2-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7b2-224">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b7b2-224">INPUTS</span></span>

### <span data-ttu-id="9b7b2-225">System. String</span><span class="sxs-lookup"><span data-stu-id="9b7b2-225">System.String</span></span>

### <span data-ttu-id="9b7b2-226">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9b7b2-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="9b7b2-227">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9b7b2-227">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="9b7b2-228">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="9b7b2-229">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="9b7b2-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="9b7b2-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="9b7b2-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="9b7b2-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="9b7b2-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="9b7b2-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="9b7b2-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="9b7b2-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="9b7b2-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="9b7b2-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="9b7b2-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="9b7b2-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9b7b2-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="9b7b2-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="9b7b2-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="9b7b2-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b7b2-244">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b7b2-245">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b7b2-245">OUTPUTS</span></span>

### <span data-ttu-id="9b7b2-246">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b2-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b7b2-247">Note</span><span class="sxs-lookup"><span data-stu-id="9b7b2-247">NOTES</span></span>

## <span data-ttu-id="9b7b2-248">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b7b2-248">RELATED LINKS</span></span>

[<span data-ttu-id="9b7b2-249">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9b7b2-249">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9b7b2-250">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b7b2-250">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="9b7b2-251">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9b7b2-251">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9b7b2-252">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9b7b2-252">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9b7b2-253">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9b7b2-253">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9b7b2-254">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b2-254">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9b7b2-255">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9b7b2-255">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9b7b2-256">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9b7b2-256">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="9b7b2-257">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9b7b2-257">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9b7b2-258">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b7b2-258">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
