---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 3c30f7a341615b7e12843f3cd745cd691fa205aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021191"
---
# <span data-ttu-id="fd8d2-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd8d2-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="fd8d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8d2-103">Crea un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fd8d2-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="fd8d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd8d2-104">SYNTAX</span></span>

### <span data-ttu-id="fd8d2-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd8d2-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8d2-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd8d2-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd8d2-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd8d2-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd8d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="fd8d2-109">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-110">Il cmdlet **New-AzVirtualNetworkGateway** crea l'oggetto del gateway in Azure in base al nome, al nome del gruppo di risorse, alla posizione e alla configurazione IP, oltre al tipo di gateway e alla rete VPN, ovvero il tipo di VPN.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="fd8d2-111">È anche possibile assegnare un nome alla SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="fd8d2-112">Se questo gateway viene usato per le connessioni Point-to-site, sarà necessario includere anche il pool di indirizzi del client VPN da cui assegnare gli indirizzi ai client di connessione e il certificato radice del client VPN usato per autenticare i client VPN che si connettono al gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="fd8d2-113">Puoi anche scegliere di includere altre caratteristiche come BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="fd8d2-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd8d2-114">EXAMPLES</span></span>

### <span data-ttu-id="fd8d2-115">1: creare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fd8d2-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="fd8d2-116">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-117">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="fd8d2-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="fd8d2-118">2: creare un gateway di rete virtuale con configurazione RADIUS esterna</span><span class="sxs-lookup"><span data-stu-id="fd8d2-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="fd8d2-119">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-120">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="fd8d2-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="fd8d2-121">Aggiunge anche un server RADIUS esterno con l'indirizzo "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="fd8d2-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="fd8d2-122">Consentirà anche di impostare route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="fd8d2-123">3: creare un gateway di rete virtuale con le impostazioni di P2S</span><span class="sxs-lookup"><span data-stu-id="fd8d2-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="fd8d2-124">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale con le impostazioni di P2S, ad esempio VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy e così via in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="fd8d2-125">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="fd8d2-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="fd8d2-126">Le impostazioni VPN verranno impostate nel gateway, ad esempio VpnProtocol impostato come Ikev2, VpnClientAddressPool come "201.169.0.0/16", VpnClientRootCertificate impostato come passato: clientRootCertName e criteri IPSec VPN personalizzati passati in oggetto: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="fd8d2-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="fd8d2-127">Consentirà anche di impostare route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="fd8d2-128">4: creare un gateway di rete virtuale con la configurazione di autenticazione AAD per VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="fd8d2-129">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-130">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="fd8d2-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="fd8d2-131">Configura anche le configurazioni di autenticazione AAD: AadTenantUri, AadIssuerUri e AadAudienceId per VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="fd8d2-132">5: creare un gateway di rete virtuale con VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="fd8d2-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="fd8d2-133">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-134">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway di "VPN", il tipo di VPN "RouteBased", l'SKU "VpnGw4" e VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="fd8d2-135">6: creare un gateway di rete virtuale con IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="fd8d2-135">6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="fd8d2-136">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-136">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="fd8d2-137">ipconfigurationId1 del gateway IPConfiguration appena creato e archiviato in ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-137">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="fd8d2-138">Il gateway verrà chiamato "gateway1" nel gruppo di risorse "resourcegroup1resourcegroup1" nella posizione "UK West" con l'indirizzo di Bgppeering configurazioni IP creato in precedenza salvato nella variabile "gw1ipconfBgp1", il tipo di gateway di "VPN", il tipo di VPN "RouteBased", l'SKU "VpnGw4" e VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-138">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="fd8d2-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd8d2-139">PARAMETERS</span></span>

### <span data-ttu-id="fd8d2-140">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="fd8d2-140">-AadAudienceId</span></span>
<span data-ttu-id="fd8d2-141">Opzione di autenticazione P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-141">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-142">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="fd8d2-142">-AadIssuerUri</span></span>
<span data-ttu-id="fd8d2-143">Opzione di autenticazione P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-143">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-144">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="fd8d2-144">-AadTenantUri</span></span>
<span data-ttu-id="fd8d2-145">Opzione di autenticazione P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-145">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd8d2-146">-AsJob</span></span>
<span data-ttu-id="fd8d2-147">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fd8d2-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd8d2-148">-ASN</span><span class="sxs-lookup"><span data-stu-id="fd8d2-148">-Asn</span></span>
<span data-ttu-id="fd8d2-149">ASN di Virtual Network del gateway per BGP su VPN</span><span class="sxs-lookup"><span data-stu-id="fd8d2-149">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-150">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="fd8d2-150">-CustomRoute</span></span>
<span data-ttu-id="fd8d2-151">Route personalizzate AddressPool specificate dal cliente</span><span class="sxs-lookup"><span data-stu-id="fd8d2-151">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8d2-152">-DefaultProfile</span></span>
<span data-ttu-id="fd8d2-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8d2-154">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="fd8d2-154">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="fd8d2-155">Contrassegno per abilitare la funzionalità attiva attiva nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fd8d2-155">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="fd8d2-156">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fd8d2-156">-EnableBgp</span></span>
<span data-ttu-id="fd8d2-157">Flag EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fd8d2-157">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-158">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd8d2-158">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="fd8d2-159">Contrassegno per l'abilitazione di IPAddress privato sul gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fd8d2-159">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="fd8d2-160">-Force</span><span class="sxs-lookup"><span data-stu-id="fd8d2-160">-Force</span></span>
<span data-ttu-id="fd8d2-161">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="fd8d2-161">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd8d2-162">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fd8d2-162">-GatewayDefaultSite</span></span>
<span data-ttu-id="fd8d2-163">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fd8d2-163">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-164">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="fd8d2-164">-GatewaySku</span></span>
<span data-ttu-id="fd8d2-165">Livello SKU gateway</span><span class="sxs-lookup"><span data-stu-id="fd8d2-165">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-166">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="fd8d2-166">-GatewayType</span></span>
<span data-ttu-id="fd8d2-167">Il tipo di questo gateway di rete virtuale: VPN, ExoressRoute</span><span class="sxs-lookup"><span data-stu-id="fd8d2-167">The type of this virtual network gateway: Vpn, ExoressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-168">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="fd8d2-168">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="fd8d2-169">BgpPeeringAddresses for Virtual Network Gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-169">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-170">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="fd8d2-170">-IpConfigurations</span></span>
<span data-ttu-id="fd8d2-171">Il gateway di rete virtuale IpConfigurations per.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-171">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-172">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fd8d2-172">-Location</span></span>
<span data-ttu-id="fd8d2-173">posizione.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-173">location.</span></span>

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

### <span data-ttu-id="fd8d2-174">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd8d2-174">-Name</span></span>
<span data-ttu-id="fd8d2-175">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-175">The resource name.</span></span>

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

### <span data-ttu-id="fd8d2-176">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="fd8d2-176">-PeerWeight</span></span>
<span data-ttu-id="fd8d2-177">Il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fd8d2-177">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-178">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="fd8d2-178">-RadiusServerAddress</span></span>
<span data-ttu-id="fd8d2-179">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-179">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-180">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="fd8d2-180">-RadiusServerSecret</span></span>
<span data-ttu-id="fd8d2-181">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-181">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8d2-182">-ResourceGroupName</span></span>
<span data-ttu-id="fd8d2-183">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-183">The resource group name.</span></span>

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

### <span data-ttu-id="fd8d2-184">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd8d2-184">-Tag</span></span>
<span data-ttu-id="fd8d2-185">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-185">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd8d2-186">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="fd8d2-186">-VpnClientAddressPool</span></span>
<span data-ttu-id="fd8d2-187">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="fd8d2-187">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-188">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fd8d2-188">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="fd8d2-189">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-189">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-190">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="fd8d2-190">-VpnClientProtocol</span></span>
<span data-ttu-id="fd8d2-191">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="fd8d2-191">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-192">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="fd8d2-192">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="fd8d2-193">Elenco di VpnClientCertificates da revocare.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-193">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-194">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="fd8d2-194">-VpnClientRootCertificates</span></span>
<span data-ttu-id="fd8d2-195">Elenco di VpnClientRootCertificates da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-195">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-196">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="fd8d2-196">-VpnGatewayGeneration</span></span>
<span data-ttu-id="fd8d2-197">Generazione per questo gateway VPN di VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-197">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="fd8d2-198">Deve essere None se GatewayType non è VPN.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-198">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-199">-VpnType</span><span class="sxs-lookup"><span data-stu-id="fd8d2-199">-VpnType</span></span>
<span data-ttu-id="fd8d2-200">Tipo di VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="fd8d2-200">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-201">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd8d2-201">-Confirm</span></span>
<span data-ttu-id="fd8d2-202">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8d2-203">-WhatIf</span></span>
<span data-ttu-id="fd8d2-204">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8d2-205">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8d2-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8d2-206">CommonParameters</span></span>
<span data-ttu-id="fd8d2-207">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd8d2-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8d2-208">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd8d2-208">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8d2-209">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd8d2-209">INPUTS</span></span>

### <span data-ttu-id="fd8d2-210">System. String</span><span class="sxs-lookup"><span data-stu-id="fd8d2-210">System.String</span></span>

### <span data-ttu-id="fd8d2-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="fd8d2-212">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8d2-212">System.Boolean</span></span>

### <span data-ttu-id="fd8d2-213">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd8d2-213">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="fd8d2-214">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-214">System.String[]</span></span>

### <span data-ttu-id="fd8d2-215">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-215">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="fd8d2-216">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-216">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="fd8d2-217">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-217">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="fd8d2-218">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="fd8d2-218">System.UInt32</span></span>

### <span data-ttu-id="fd8d2-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fd8d2-219">System.Int32</span></span>

### <span data-ttu-id="fd8d2-220">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="fd8d2-220">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="fd8d2-221">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd8d2-221">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fd8d2-222">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fd8d2-222">System.Security.SecureString</span></span>

## <span data-ttu-id="fd8d2-223">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd8d2-223">OUTPUTS</span></span>

### <span data-ttu-id="fd8d2-224">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd8d2-224">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fd8d2-225">Note</span><span class="sxs-lookup"><span data-stu-id="fd8d2-225">NOTES</span></span>

## <span data-ttu-id="fd8d2-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd8d2-226">RELATED LINKS</span></span>
