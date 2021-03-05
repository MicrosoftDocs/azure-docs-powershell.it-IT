---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977885"
---
# <span data-ttu-id="95927-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95927-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="95927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95927-102">SYNOPSIS</span></span>
<span data-ttu-id="95927-103">Crea un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="95927-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="95927-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95927-104">SYNTAX</span></span>

### <span data-ttu-id="95927-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95927-105">Default (Default)</span></span>
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

### <span data-ttu-id="95927-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="95927-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="95927-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="95927-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="95927-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="95927-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="95927-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="95927-109">DESCRIPTION</span></span>
<span data-ttu-id="95927-110">Il Gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="95927-111">Il cmdlet **New-AzVirtualNetworkGateway** crea l'oggetto del gateway in Azure in base al nome, al nome del gruppo di risorse, alla posizione e alla configurazione IP, nonché al tipo di gateway e, se VPN, al tipo di VPN.</span><span class="sxs-lookup"><span data-stu-id="95927-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="95927-112">È anche possibile assegnare un nome alla SKU del gateway.</span><span class="sxs-lookup"><span data-stu-id="95927-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="95927-113">Se il gateway viene usato per le connessioni da punto a sito, sarà necessario includere anche il pool di indirizzi client VPN da cui assegnare gli indirizzi ai client di connessione e il certificato radice del client VPN usato per autenticare i client VPN che si connettono al gateway.</span><span class="sxs-lookup"><span data-stu-id="95927-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="95927-114">È anche possibile scegliere di includere altre funzionalità, ad esempio BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="95927-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="95927-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95927-115">EXAMPLES</span></span>

### <span data-ttu-id="95927-116">Esempio 1: Creare un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="95927-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="95927-117">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="95927-118">Il gateway sarà denominato "myNGW" all'interno del gruppo di risorse "vnet-gateway" nel percorso "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di vpn "RouteBased" e la sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="95927-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="95927-119">Esempio 2: Creare un gateway di rete virtuale con configurazione del raggio esterno</span><span class="sxs-lookup"><span data-stu-id="95927-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="95927-120">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="95927-121">Il gateway sarà denominato "myNGW" all'interno del gruppo di risorse "vnet-gateway" nel percorso "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di vpn "RouteBased" e la sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="95927-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="95927-122">Aggiunge anche un server di raggio esterno con indirizzo "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="95927-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="95927-123">Verranno impostate anche route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="95927-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="95927-124">Esempio 3: Creare un Gateway di rete virtuale con impostazioni P2S</span><span class="sxs-lookup"><span data-stu-id="95927-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="95927-125">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale con impostazioni P2S, ad esempio VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy e così via in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="95927-126">Il gateway sarà denominato "myNGW" all'interno del gruppo di risorse "vnet-gateway" nel percorso "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di vpn "RouteBased" e la sku "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="95927-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="95927-127">Le impostazioni vpn verranno impostate su Gateway, ad esempio VpnProtocol, impostato su Ikev2, VpnClientAddressPool come "201.169.0.0/16", VpnClientRootCertificate impostato come superato: clientRootCertName e il criterio personalizzato vpn ipsec passati in object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="95927-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="95927-128">Verranno impostate anche route personalizzate specificate dai clienti nel gateway.</span><span class="sxs-lookup"><span data-stu-id="95927-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="95927-129">Esempio 4: Creare un Gateway di rete virtuale con configurazione di autenticazione AAD per VpnClient del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="95927-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="95927-130">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="95927-131">Il gateway sarà denominato "myNGW" all'interno del gruppo di risorse "vnet-gateway" nel percorso "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di vpn "RouteBased" e la sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="95927-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="95927-132">Configura anche le configurazioni di autenticazione AAD: AadTenantUri, AadIssuerUri e AadAudienceId per VpnClient del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="95927-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="95927-133">Esempio 5: Creare un gateway di rete virtuale con VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="95927-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="95927-134">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="95927-135">Il gateway sarà denominato "myNGW" all'interno del gruppo di risorse "vnet-gateway" nel percorso "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di vpn "RouteBased", le sku "VpnGw4" e VpnGatewayGeneration Generation2 abilitate.</span><span class="sxs-lookup"><span data-stu-id="95927-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="95927-136">Esempio 6: Creare un gateway di rete virtuale con IpConfigurationBgpAddressingAddresses</span><span class="sxs-lookup"><span data-stu-id="95927-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="95927-137">La procedura descritta sopra consente di creare un gruppo di risorse, richiedere un indirizzo IP pubblico, creare una rete virtuale e una subnet e un Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="95927-138">ipconfigurationId1 della configurazione ip del gateway appena creata e archiviata in ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="95927-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="95927-139">Il gateway sarà denominato "gateway1" all'interno del gruppo di risorse "resourcegroup1resourcegroup1" nel percorso "UK West" con le configurazioni IP Bgptinging create in precedenza, salvate nella variabile "gw1ipconfBgp1", il tipo di gateway "VPN", il tipo di vpn "RouteBased", le SKU "VpnGw4" e VpnGatewayGeneration Generation2 abilitate.</span><span class="sxs-lookup"><span data-stu-id="95927-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="95927-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95927-140">PARAMETERS</span></span>

### <span data-ttu-id="95927-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="95927-141">-AadAudienceId</span></span>
<span data-ttu-id="95927-142">Opzione di autenticazione AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="95927-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="95927-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="95927-143">-AadIssuerUri</span></span>
<span data-ttu-id="95927-144">Opzione di autenticazione AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="95927-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="95927-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="95927-145">-AadTenantUri</span></span>
<span data-ttu-id="95927-146">Opzione di autenticazione AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="95927-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="95927-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95927-147">-AsJob</span></span>
<span data-ttu-id="95927-148">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="95927-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95927-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="95927-149">-Asn</span></span>
<span data-ttu-id="95927-150">ASN del gateway di rete virtuale per BGP su VPN</span><span class="sxs-lookup"><span data-stu-id="95927-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="95927-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="95927-151">-CustomRoute</span></span>
<span data-ttu-id="95927-152">Route personalizzate AddressPool specificate dal cliente</span><span class="sxs-lookup"><span data-stu-id="95927-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="95927-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95927-153">-DefaultProfile</span></span>
<span data-ttu-id="95927-154">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95927-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95927-155">-EnableActiveFeature</span><span class="sxs-lookup"><span data-stu-id="95927-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="95927-156">Contrassegno per abilitare la caratteristica Attiva nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="95927-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="95927-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="95927-157">-EnableBgp</span></span>
<span data-ttu-id="95927-158">Contrassegno EnableBgp</span><span class="sxs-lookup"><span data-stu-id="95927-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="95927-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="95927-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="95927-160">Flag per abilitare IPAddress privato nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="95927-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="95927-161">-Force</span><span class="sxs-lookup"><span data-stu-id="95927-161">-Force</span></span>
<span data-ttu-id="95927-162">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="95927-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="95927-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="95927-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="95927-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="95927-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="95927-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="95927-165">-GatewaySku</span></span>
<span data-ttu-id="95927-166">Livello SKU gateway</span><span class="sxs-lookup"><span data-stu-id="95927-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="95927-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="95927-167">-GatewayType</span></span>
<span data-ttu-id="95927-168">Il tipo di gateway di rete virtuale: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="95927-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="95927-169">-IpConfigurationBgpAddressingAddresses</span><span class="sxs-lookup"><span data-stu-id="95927-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="95927-170">BgpAddressingAddresses per bgpsettings del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="95927-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="95927-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="95927-171">-IpConfigurations</span></span>
<span data-ttu-id="95927-172">IpConfigurations per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="95927-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="95927-173">-Location</span><span class="sxs-lookup"><span data-stu-id="95927-173">-Location</span></span>
<span data-ttu-id="95927-174">posizione.</span><span class="sxs-lookup"><span data-stu-id="95927-174">location.</span></span>

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

### <span data-ttu-id="95927-175">-Name</span><span class="sxs-lookup"><span data-stu-id="95927-175">-Name</span></span>
<span data-ttu-id="95927-176">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="95927-176">The resource name.</span></span>

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

### <span data-ttu-id="95927-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="95927-177">-PeerWeight</span></span>
<span data-ttu-id="95927-178">Il peso aggiunto alle route apprese tramite BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="95927-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="95927-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="95927-179">-RadiusServerAddress</span></span>
<span data-ttu-id="95927-180">Indirizzo server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="95927-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="95927-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="95927-181">-RadiusServerList</span></span>
<span data-ttu-id="95927-182">P2S più server di raggio esterni.</span><span class="sxs-lookup"><span data-stu-id="95927-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="95927-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="95927-183">-RadiusServerSecret</span></span>
<span data-ttu-id="95927-184">Segreto server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="95927-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="95927-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95927-185">-ResourceGroupName</span></span>
<span data-ttu-id="95927-186">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="95927-186">The resource group name.</span></span>

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

### <span data-ttu-id="95927-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="95927-187">-Tag</span></span>
<span data-ttu-id="95927-188">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="95927-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="95927-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="95927-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="95927-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="95927-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="95927-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="95927-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="95927-192">Elenco dei criteri IPSec per i protocolli di tunneling del client VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="95927-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="95927-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="95927-193">-VpnClientProtocol</span></span>
<span data-ttu-id="95927-194">Elenco dei protocolli di tunneling del client VPN P2S</span><span class="sxs-lookup"><span data-stu-id="95927-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="95927-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="95927-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="95927-196">Elenco di VpnClientCertificates da revocare.</span><span class="sxs-lookup"><span data-stu-id="95927-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="95927-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="95927-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="95927-198">Elenco di VpnClientRootCertificates da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="95927-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="95927-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="95927-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="95927-200">La generazione di questo gateway VPN VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="95927-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="95927-201">Deve essere Nessuno se GatewayType non è VPN.</span><span class="sxs-lookup"><span data-stu-id="95927-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="95927-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="95927-202">-VpnType</span></span>
<span data-ttu-id="95927-203">Il tipo di Vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="95927-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="95927-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95927-204">-Confirm</span></span>
<span data-ttu-id="95927-205">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95927-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95927-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95927-206">-WhatIf</span></span>
<span data-ttu-id="95927-207">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95927-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95927-208">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95927-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95927-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95927-209">CommonParameters</span></span>
<span data-ttu-id="95927-210">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95927-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95927-211">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95927-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95927-212">INPUT</span><span class="sxs-lookup"><span data-stu-id="95927-212">INPUTS</span></span>

### <span data-ttu-id="95927-213">System.String</span><span class="sxs-lookup"><span data-stu-id="95927-213">System.String</span></span>

### <span data-ttu-id="95927-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="95927-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="95927-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95927-215">System.Boolean</span></span>

### <span data-ttu-id="95927-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95927-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="95927-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="95927-217">System.String[]</span></span>

### <span data-ttu-id="95927-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="95927-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="95927-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="95927-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="95927-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="95927-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="95927-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="95927-221">System.UInt32</span></span>

### <span data-ttu-id="95927-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="95927-222">System.Int32</span></span>

### <span data-ttu-id="95927-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpAddress[]</span><span class="sxs-lookup"><span data-stu-id="95927-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="95927-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95927-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95927-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="95927-225">System.Security.SecureString</span></span>

## <span data-ttu-id="95927-226">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95927-226">OUTPUTS</span></span>

### <span data-ttu-id="95927-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95927-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="95927-228">NOTE</span><span class="sxs-lookup"><span data-stu-id="95927-228">NOTES</span></span>

## <span data-ttu-id="95927-229">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95927-229">RELATED LINKS</span></span>
