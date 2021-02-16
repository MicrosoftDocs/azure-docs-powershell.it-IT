---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 0f3d65c629218fc903035cb9df669f1c3dc7a50c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202998"
---
# <span data-ttu-id="60567-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60567-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="60567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60567-102">SYNOPSIS</span></span>
<span data-ttu-id="60567-103">Crea un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-103">Creates an application gateway.</span></span>

## <span data-ttu-id="60567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60567-104">SYNTAX</span></span>

### <span data-ttu-id="60567-105">IdentityByUserAssignedIdentityId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60567-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="60567-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="60567-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="60567-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="60567-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="60567-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="60567-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

## <span data-ttu-id="60567-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60567-109">DESCRIPTION</span></span>
<span data-ttu-id="60567-110">Il cmdlet **New-AzApplicationGateway** crea un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="60567-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="60567-111">Un gateway applicazione richiede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="60567-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="60567-112">Un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60567-112">A resource group.</span></span>
- <span data-ttu-id="60567-113">Una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="60567-113">A virtual network.</span></span>
- <span data-ttu-id="60567-114">Pool di server back-end contenente gli indirizzi IP dei server back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="60567-115">Impostazioni del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-115">Back-end server pool settings.</span></span> <span data-ttu-id="60567-116">Ogni pool include impostazioni come porta, protocollo e affinità basata su cookie, applicate a tutti i server all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="60567-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="60567-117">Indirizzi IP front-end, ovvero gli indirizzi IP aperti nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="60567-118">Un indirizzo IP front-end può essere un indirizzo IP pubblico o interno.</span><span class="sxs-lookup"><span data-stu-id="60567-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="60567-119">Porte front-end, ovvero le porte pubbliche aperte nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="60567-120">Il traffico che raggiunge queste porte viene reindirizzato ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="60567-121">Regola di routing delle richieste che associa il listener e il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="60567-122">La regola definisce a quale pool di server back-end deve essere indirizzato il traffico quando raggiunge un determinato ascoltatore.</span><span class="sxs-lookup"><span data-stu-id="60567-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="60567-123">Un ascoltatore ha una porta front-end, un indirizzo IP front-end, un protocollo (HTTP o HTTPS) e un nome di certificato SSL (Secure Sockets Layer) (se si configura l'offload SSL).</span><span class="sxs-lookup"><span data-stu-id="60567-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="60567-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60567-124">EXAMPLES</span></span>

### <span data-ttu-id="60567-125">Esempio 1: Creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="60567-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="60567-126">L'esempio seguente crea un gateway applicazione creando prima un gruppo di risorse e una rete virtuale, oltre a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="60567-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="60567-127">Pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="60567-127">A back-end server pool</span></span>
- <span data-ttu-id="60567-128">Impostazioni pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="60567-128">Back-end server pool settings</span></span>
- <span data-ttu-id="60567-129">Porte front-end</span><span class="sxs-lookup"><span data-stu-id="60567-129">Front-end ports</span></span>
- <span data-ttu-id="60567-130">Indirizzi IP front-end</span><span class="sxs-lookup"><span data-stu-id="60567-130">Front-end IP addresses</span></span>
- <span data-ttu-id="60567-131">Una regola di routing delle richieste Questi quattro comandi creano una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="60567-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="60567-132">Il primo comando crea una configurazione subnet.</span><span class="sxs-lookup"><span data-stu-id="60567-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="60567-133">Il secondo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="60567-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="60567-134">Il terzo comando verifica la configurazione della subnet e il quarto comando verifica che la rete virtuale sia stata creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="60567-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="60567-135">I comandi seguenti creano il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="60567-136">Il primo comando crea una configurazione IP denominata GatewayIp01 per la subnet creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="60567-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="60567-137">Il secondo comando crea un pool di server back-end denominato Pool01 con un elenco di indirizzi IP back-end e archivia il pool nella variabile $Pool back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="60567-138">Il terzo comando crea le impostazioni per il pool di server back-end e le archivia nella variabile $PoolSetting back-end.</span><span class="sxs-lookup"><span data-stu-id="60567-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="60567-139">Il comando crea una porta front-end sulla porta 80, la crea FrontEndPort01 e la archivia nella variabile $FrontEndPort locale.</span><span class="sxs-lookup"><span data-stu-id="60567-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="60567-140">Il quinto comando crea un indirizzo IP pubblico usando New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="60567-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="60567-141">Il sesto comando crea una configurazione IP front-end con $PublicIp, la denome FrontEndPortConfig01 e la archivia nella variabile $FrontEndIpConfig front-end.</span><span class="sxs-lookup"><span data-stu-id="60567-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="60567-142">Il settimo comando crea un ascoltatore usando il comando creato in precedenza $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="60567-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="60567-143">L'ottavo comando crea una regola per chi ascolta.</span><span class="sxs-lookup"><span data-stu-id="60567-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="60567-144">Il nono comando imposta lo SKU.</span><span class="sxs-lookup"><span data-stu-id="60567-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="60567-145">Il decimo comando crea il gateway usando gli oggetti impostati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="60567-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="60567-146">Esempio 2: Creare un gateway applicazione con identità UserAssigned</span><span class="sxs-lookup"><span data-stu-id="60567-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="60567-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60567-147">PARAMETERS</span></span>

### <span data-ttu-id="60567-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60567-148">-AsJob</span></span>
<span data-ttu-id="60567-149">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60567-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60567-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="60567-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="60567-151">Specifica i certificati di autenticazione per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="60567-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="60567-153">Configurazione della scala automatica</span><span class="sxs-lookup"><span data-stu-id="60567-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="60567-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="60567-154">-BackendAddressPools</span></span>
<span data-ttu-id="60567-155">Specifica l'elenco di pool di indirizzi back-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="60567-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="60567-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="60567-157">Specifica l'elenco delle impostazioni HTTP di back-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="60567-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="60567-159">Errore del cliente di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="60567-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="60567-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60567-160">-DefaultProfile</span></span>
<span data-ttu-id="60567-161">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60567-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60567-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="60567-162">-EnableFIPS</span></span>
<span data-ttu-id="60567-163">Se FIPS è abilitato.</span><span class="sxs-lookup"><span data-stu-id="60567-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="60567-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="60567-164">-EnableHttp2</span></span>
<span data-ttu-id="60567-165">Se è abilitato HTTP2.</span><span class="sxs-lookup"><span data-stu-id="60567-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="60567-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="60567-166">-FirewallPolicy</span></span>
<span data-ttu-id="60567-167">Configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="60567-167">Firewall configuration</span></span>

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

### <span data-ttu-id="60567-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="60567-168">-FirewallPolicyId</span></span>
<span data-ttu-id="60567-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="60567-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="60567-170">-Force</span><span class="sxs-lookup"><span data-stu-id="60567-170">-Force</span></span>
<span data-ttu-id="60567-171">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="60567-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60567-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="60567-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="60567-173">Se l'associazione Force firewallPolicy è abilitata.</span><span class="sxs-lookup"><span data-stu-id="60567-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="60567-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="60567-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="60567-175">Specifica un elenco di configurazioni IP front-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="60567-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="60567-176">-FrontendPorts</span></span>
<span data-ttu-id="60567-177">Specifica un elenco di porte front-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="60567-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="60567-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="60567-179">Specifica un elenco di configurazioni IP per il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="60567-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="60567-180">-Http AllIs</span><span class="sxs-lookup"><span data-stu-id="60567-180">-HttpListeners</span></span>
<span data-ttu-id="60567-181">Specifica un elenco di listener HTTP per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="60567-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="60567-182">-Identity</span></span>
<span data-ttu-id="60567-183">Identità del Gateway applicazione da assegnare al Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="60567-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="60567-184">-Location</span><span class="sxs-lookup"><span data-stu-id="60567-184">-Location</span></span>
<span data-ttu-id="60567-185">Specifica l'area in cui creare il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="60567-186">-Name</span><span class="sxs-lookup"><span data-stu-id="60567-186">-Name</span></span>
<span data-ttu-id="60567-187">Specifica il nome del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="60567-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="60567-189">Elenco di configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="60567-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60567-190">-Avari</span><span class="sxs-lookup"><span data-stu-id="60567-190">-Probes</span></span>
<span data-ttu-id="60567-191">Specifica i criteri per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-191">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="60567-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="60567-192">-RedirectConfigurations</span></span>
<span data-ttu-id="60567-193">Elenco della configurazione di reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="60567-193">The list of redirect configuration</span></span>

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

### <span data-ttu-id="60567-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="60567-194">-RequestRoutingRules</span></span>
<span data-ttu-id="60567-195">Specifica un elenco di regole di routing delle richieste per il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="60567-195">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="60567-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60567-196">-ResourceGroupName</span></span>
<span data-ttu-id="60567-197">Specifica il nome del gruppo di risorse in cui creare il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="60567-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60567-198">-RewriteRuleSet</span></span>
<span data-ttu-id="60567-199">Elenco di RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60567-199">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="60567-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="60567-200">-Sku</span></span>
<span data-ttu-id="60567-201">Specifica l'unità di conservazione dei titoli azionari del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="60567-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="60567-202">-SslCertificates</span></span>
<span data-ttu-id="60567-203">Specifica l'elenco di certificati SSL (Secure Sockets Layer) per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="60567-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="60567-204">-SslPolicy</span></span>
<span data-ttu-id="60567-205">Specifica un criterio SSL per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-205">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="60567-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="60567-206">-SslProfiles</span></span>
<span data-ttu-id="60567-207">Elenco dei profili SSL</span><span class="sxs-lookup"><span data-stu-id="60567-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60567-208">-Tag</span><span class="sxs-lookup"><span data-stu-id="60567-208">-Tag</span></span>
<span data-ttu-id="60567-209">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="60567-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="60567-210">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="60567-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="60567-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="60567-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="60567-212">Elenco delle catene di certificati CA dei client attendibili</span><span class="sxs-lookup"><span data-stu-id="60567-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60567-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="60567-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="60567-214">Elenco di certificati radice attendibili</span><span class="sxs-lookup"><span data-stu-id="60567-214">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="60567-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="60567-215">-UrlPathMaps</span></span>
<span data-ttu-id="60567-216">Specifica i mapping del percorso URL per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-216">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="60567-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="60567-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="60567-218">ResourceId dell'identità assegnata all'utente da assegnare a Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="60567-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="60567-220">Specifica una configurazione firewall applicazione Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="60567-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="60567-221">È possibile usare il cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration per ottenere un waf.</span><span class="sxs-lookup"><span data-stu-id="60567-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="60567-222">-Zone</span><span class="sxs-lookup"><span data-stu-id="60567-222">-Zone</span></span>
<span data-ttu-id="60567-223">Elenco di aree di disponibilità che denotono la destinazione del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="60567-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="60567-224">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60567-224">-Confirm</span></span>
<span data-ttu-id="60567-225">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60567-225">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60567-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60567-226">-WhatIf</span></span>
<span data-ttu-id="60567-227">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60567-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60567-228">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60567-228">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60567-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60567-229">CommonParameters</span></span>
<span data-ttu-id="60567-230">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60567-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60567-231">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60567-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60567-232">INPUT</span><span class="sxs-lookup"><span data-stu-id="60567-232">INPUTS</span></span>

### <span data-ttu-id="60567-233">System.String</span><span class="sxs-lookup"><span data-stu-id="60567-233">System.String</span></span>

### <span data-ttu-id="60567-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="60567-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="60567-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="60567-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="60567-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="60567-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="60567-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="60567-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="60567-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="60567-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="60567-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="60567-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="60567-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="60567-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="60567-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="60567-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="60567-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="60567-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="60567-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="60567-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="60567-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="60567-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="60567-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication[]</span><span class="sxs-lookup"><span data-stu-id="60567-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="60567-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="60567-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="60567-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="60567-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="60567-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="60567-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="60567-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="60567-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="60567-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="60567-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="60567-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="60567-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="60567-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="60567-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="60567-254">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60567-254">OUTPUTS</span></span>

### <span data-ttu-id="60567-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60567-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60567-256">NOTE</span><span class="sxs-lookup"><span data-stu-id="60567-256">NOTES</span></span>

## <span data-ttu-id="60567-257">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60567-257">RELATED LINKS</span></span>

[<span data-ttu-id="60567-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60567-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="60567-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="60567-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="60567-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="60567-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="60567-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="60567-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="60567-262">New-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="60567-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="60567-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="60567-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="60567-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60567-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="60567-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="60567-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="60567-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="60567-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="60567-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60567-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
