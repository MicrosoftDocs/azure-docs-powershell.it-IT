---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201779"
---
# <span data-ttu-id="766ff-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="766ff-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="766ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="766ff-102">SYNOPSIS</span></span>
<span data-ttu-id="766ff-103">Crea un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="766ff-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="766ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="766ff-104">SYNTAX</span></span>

### <span data-ttu-id="766ff-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="766ff-105">Default (Default)</span></span>
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

### <span data-ttu-id="766ff-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="766ff-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766ff-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="766ff-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="766ff-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="766ff-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="766ff-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="766ff-109">DESCRIPTION</span></span>
<span data-ttu-id="766ff-110">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="766ff-111">Il cmdlet **New-AzVirtualNetworkGateway** crea l'oggetto del gateway in Azure in base al nome, al nome del gruppo di risorse, alla posizione e alla configurazione IP, oltre al tipo di gateway e alla rete VPN, ovvero il tipo di VPN.</span><span class="sxs-lookup"><span data-stu-id="766ff-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="766ff-112">È anche possibile assegnare un nome alla SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="766ff-113">Se questo gateway viene usato per le connessioni Point-to-site, sarà necessario includere anche il pool di indirizzi del client VPN da cui assegnare gli indirizzi ai client di connessione e il certificato radice del client VPN usato per autenticare i client VPN che si connettono al gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="766ff-114">Puoi anche scegliere di includere altre caratteristiche come BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="766ff-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="766ff-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="766ff-115">EXAMPLES</span></span>

### <span data-ttu-id="766ff-116">Esempio 1: creare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="766ff-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="766ff-117">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="766ff-118">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="766ff-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="766ff-119">Esempio 2: creare un gateway di rete virtuale con configurazione RADIUS esterna</span><span class="sxs-lookup"><span data-stu-id="766ff-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="766ff-120">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="766ff-121">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="766ff-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="766ff-122">Aggiunge anche un server RADIUS esterno con l'indirizzo "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="766ff-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="766ff-123">Consentirà anche di impostare route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="766ff-124">Esempio 3: creare un gateway di rete virtuale con le impostazioni di P2S</span><span class="sxs-lookup"><span data-stu-id="766ff-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
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

<span data-ttu-id="766ff-125">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale con le impostazioni di P2S, ad esempio VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy e così via in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="766ff-126">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="766ff-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="766ff-127">Le impostazioni VPN verranno impostate nel gateway, ad esempio VpnProtocol impostato come Ikev2, VpnClientAddressPool come "201.169.0.0/16", VpnClientRootCertificate impostato come passato: clientRootCertName e criteri IPSec VPN personalizzati passati in oggetto: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="766ff-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="766ff-128">Consentirà anche di impostare route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="766ff-129">Esempio 4: creare un gateway di rete virtuale con la configurazione di autenticazione AAD per VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="766ff-130">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="766ff-131">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="766ff-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="766ff-132">Configura anche le configurazioni di autenticazione AAD: AadTenantUri, AadIssuerUri e AadAudienceId per VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="766ff-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="766ff-133">Esempio 5: creare un gateway di rete virtuale con VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="766ff-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="766ff-134">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="766ff-135">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway di "VPN", il tipo di VPN "RouteBased", l'SKU "VpnGw4" e VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="766ff-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="766ff-136">Esempio 6: creare un gateway di rete virtuale con IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="766ff-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
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

<span data-ttu-id="766ff-137">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="766ff-138">ipconfigurationId1 del gateway IPConfiguration appena creato e archiviato in ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="766ff-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="766ff-139">Il gateway verrà chiamato "gateway1" nel gruppo di risorse "resourcegroup1resourcegroup1" nella posizione "UK West" con l'indirizzo di Bgppeering configurazioni IP creato in precedenza salvato nella variabile "gw1ipconfBgp1", il tipo di gateway di "VPN", il tipo di VPN "RouteBased", l'SKU "VpnGw4" e VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="766ff-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="766ff-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="766ff-140">PARAMETERS</span></span>

### <span data-ttu-id="766ff-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="766ff-141">-AadAudienceId</span></span>
<span data-ttu-id="766ff-142">Opzione di autenticazione P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="766ff-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="766ff-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="766ff-143">-AadIssuerUri</span></span>
<span data-ttu-id="766ff-144">Opzione di autenticazione P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="766ff-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="766ff-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="766ff-145">-AadTenantUri</span></span>
<span data-ttu-id="766ff-146">Opzione di autenticazione P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="766ff-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="766ff-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="766ff-147">-AsJob</span></span>
<span data-ttu-id="766ff-148">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="766ff-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="766ff-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="766ff-149">-Asn</span></span>
<span data-ttu-id="766ff-150">ASN di Virtual Network del gateway per BGP su VPN</span><span class="sxs-lookup"><span data-stu-id="766ff-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="766ff-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="766ff-151">-CustomRoute</span></span>
<span data-ttu-id="766ff-152">Route personalizzate AddressPool specificate dal cliente</span><span class="sxs-lookup"><span data-stu-id="766ff-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="766ff-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766ff-153">-DefaultProfile</span></span>
<span data-ttu-id="766ff-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="766ff-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766ff-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="766ff-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="766ff-156">Contrassegno per abilitare la funzionalità attiva attiva nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="766ff-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="766ff-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="766ff-157">-EnableBgp</span></span>
<span data-ttu-id="766ff-158">Flag EnableBgp</span><span class="sxs-lookup"><span data-stu-id="766ff-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="766ff-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="766ff-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="766ff-160">Contrassegno per l'abilitazione di IPAddress privato sul gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="766ff-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="766ff-161">-Force</span><span class="sxs-lookup"><span data-stu-id="766ff-161">-Force</span></span>
<span data-ttu-id="766ff-162">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="766ff-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="766ff-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="766ff-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="766ff-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="766ff-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="766ff-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="766ff-165">-GatewaySku</span></span>
<span data-ttu-id="766ff-166">Livello SKU gateway</span><span class="sxs-lookup"><span data-stu-id="766ff-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="766ff-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="766ff-167">-GatewayType</span></span>
<span data-ttu-id="766ff-168">Il tipo di questo gateway di rete virtuale: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="766ff-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="766ff-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="766ff-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="766ff-170">BgpPeeringAddresses for Virtual Network Gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="766ff-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="766ff-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="766ff-171">-IpConfigurations</span></span>
<span data-ttu-id="766ff-172">Il gateway di rete virtuale IpConfigurations per.</span><span class="sxs-lookup"><span data-stu-id="766ff-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="766ff-173">-Posizione</span><span class="sxs-lookup"><span data-stu-id="766ff-173">-Location</span></span>
<span data-ttu-id="766ff-174">posizione.</span><span class="sxs-lookup"><span data-stu-id="766ff-174">location.</span></span>

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

### <span data-ttu-id="766ff-175">-Nome</span><span class="sxs-lookup"><span data-stu-id="766ff-175">-Name</span></span>
<span data-ttu-id="766ff-176">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="766ff-176">The resource name.</span></span>

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

### <span data-ttu-id="766ff-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="766ff-177">-PeerWeight</span></span>
<span data-ttu-id="766ff-178">Il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="766ff-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="766ff-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="766ff-179">-RadiusServerAddress</span></span>
<span data-ttu-id="766ff-180">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="766ff-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="766ff-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="766ff-181">-RadiusServerList</span></span>
<span data-ttu-id="766ff-182">P2S più server RADIUS esterni.</span><span class="sxs-lookup"><span data-stu-id="766ff-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766ff-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="766ff-183">-RadiusServerSecret</span></span>
<span data-ttu-id="766ff-184">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="766ff-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="766ff-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766ff-185">-ResourceGroupName</span></span>
<span data-ttu-id="766ff-186">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="766ff-186">The resource group name.</span></span>

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

### <span data-ttu-id="766ff-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="766ff-187">-Tag</span></span>
<span data-ttu-id="766ff-188">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="766ff-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="766ff-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="766ff-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="766ff-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="766ff-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="766ff-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="766ff-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="766ff-192">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="766ff-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="766ff-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="766ff-193">-VpnClientProtocol</span></span>
<span data-ttu-id="766ff-194">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="766ff-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="766ff-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="766ff-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="766ff-196">Elenco di VpnClientCertificates da revocare.</span><span class="sxs-lookup"><span data-stu-id="766ff-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="766ff-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="766ff-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="766ff-198">Elenco di VpnClientRootCertificates da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="766ff-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="766ff-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="766ff-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="766ff-200">Generazione per questo gateway VPN di VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="766ff-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="766ff-201">Deve essere None se GatewayType non è VPN.</span><span class="sxs-lookup"><span data-stu-id="766ff-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="766ff-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="766ff-202">-VpnType</span></span>
<span data-ttu-id="766ff-203">Tipo di VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="766ff-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="766ff-204">-Confermare</span><span class="sxs-lookup"><span data-stu-id="766ff-204">-Confirm</span></span>
<span data-ttu-id="766ff-205">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="766ff-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766ff-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766ff-206">-WhatIf</span></span>
<span data-ttu-id="766ff-207">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="766ff-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="766ff-208">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="766ff-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766ff-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766ff-209">CommonParameters</span></span>
<span data-ttu-id="766ff-210">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766ff-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766ff-211">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="766ff-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766ff-212">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="766ff-212">INPUTS</span></span>

### <span data-ttu-id="766ff-213">System. String</span><span class="sxs-lookup"><span data-stu-id="766ff-213">System.String</span></span>

### <span data-ttu-id="766ff-214">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="766ff-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="766ff-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="766ff-215">System.Boolean</span></span>

### <span data-ttu-id="766ff-216">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="766ff-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="766ff-217">System. String []</span><span class="sxs-lookup"><span data-stu-id="766ff-217">System.String[]</span></span>

### <span data-ttu-id="766ff-218">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="766ff-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="766ff-219">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="766ff-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="766ff-220">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="766ff-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="766ff-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="766ff-221">System.UInt32</span></span>

### <span data-ttu-id="766ff-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="766ff-222">System.Int32</span></span>

### <span data-ttu-id="766ff-223">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="766ff-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="766ff-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="766ff-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="766ff-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="766ff-225">System.Security.SecureString</span></span>

## <span data-ttu-id="766ff-226">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="766ff-226">OUTPUTS</span></span>

### <span data-ttu-id="766ff-227">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="766ff-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="766ff-228">Note</span><span class="sxs-lookup"><span data-stu-id="766ff-228">NOTES</span></span>

## <span data-ttu-id="766ff-229">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="766ff-229">RELATED LINKS</span></span>
