---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385122"
---
# <span data-ttu-id="56af6-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="56af6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56af6-102">SYNOPSIS</span></span>
<span data-ttu-id="56af6-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56af6-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="56af6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56af6-104">SYNTAX</span></span>

### <span data-ttu-id="56af6-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56af6-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56af6-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="56af6-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af6-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="56af6-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af6-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="56af6-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af6-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="56af6-109">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af6-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="56af6-110">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56af6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56af6-111">DESCRIPTION</span></span>
<span data-ttu-id="56af6-112">Il cmdlet **set-AzVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56af6-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="56af6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56af6-113">EXAMPLES</span></span>

### <span data-ttu-id="56af6-114">Esempio 1: aggiornare l'ASN di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="56af6-115">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="56af6-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="56af6-116">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="56af6-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="56af6-117">Esempio 2: aggiungere criteri IPsec a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="56af6-118">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando crea l'oggetto criteri IPSec VPN in base ai parametri IPSec specificati.</span><span class="sxs-lookup"><span data-stu-id="56af6-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="56af6-119">Il terzo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="56af6-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="56af6-120">Il comando imposta anche il criterio IPSec VPN personalizzato specificato nell'oggetto $vpnclientipsecpolicy sul gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56af6-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="56af6-121">Esempio 3: aggiungere/aggiornare i tag a un gateway di rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="56af6-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="56af6-122">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale Gateway01 con i tag @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="56af6-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="56af6-123">Esempio 4: aggiungere/aggiornare la configurazione di autenticazione AAD per VpnClient di un gateway di rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="56af6-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="56af6-124">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale Gateway01 con le configurazioni di autenticazione AAD params: aadTenantUri, aadAudienceId, aadIssuerUri per VpnClient.</span><span class="sxs-lookup"><span data-stu-id="56af6-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="56af6-125">Il terzo comando rimuove la configurazione di autenticazione AAD da VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="56af6-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="56af6-126">Esempio 5: aggiungere/aggiornare IpConfigurationBgpPeeringAddresses a un gateway di rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="56af6-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="56af6-127">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando assegna il valore di Virtual Network Gateway Gateway01 IpConfiguration ID in ipconfigurationId1 variabile.</span><span class="sxs-lookup"><span data-stu-id="56af6-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="56af6-128">Il terzo comando assegna l'elenco di indirizzi in AddressList1.</span><span class="sxs-lookup"><span data-stu-id="56af6-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="56af6-129">Il quarto comando crea un oggetto PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="56af6-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="56af6-130">Il quinto comando imposta il nuovo PSIpConfigurationBgpPeeringAddress creato in IpConfigurationBgpPeeringAddresses e aggiorna il gateway.</span><span class="sxs-lookup"><span data-stu-id="56af6-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="56af6-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56af6-131">PARAMETERS</span></span>

### <span data-ttu-id="56af6-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="56af6-132">-AadAudienceId</span></span>
<span data-ttu-id="56af6-133">Opzione di autenticazione P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="56af6-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="56af6-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="56af6-134">-AadIssuerUri</span></span>
<span data-ttu-id="56af6-135">Opzione di autenticazione P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="56af6-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="56af6-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="56af6-136">-AadTenantUri</span></span>
<span data-ttu-id="56af6-137">Opzione di autenticazione P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="56af6-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="56af6-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56af6-138">-AsJob</span></span>
<span data-ttu-id="56af6-139">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="56af6-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56af6-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="56af6-140">-Asn</span></span>
<span data-ttu-id="56af6-141">ASN del gateway di rete virtuale, usato per configurare sessioni BGP all'interno di tunnel IPsec</span><span class="sxs-lookup"><span data-stu-id="56af6-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="56af6-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="56af6-142">-CustomRoute</span></span>
<span data-ttu-id="56af6-143">Route personalizzate AddressPool specificate dal cliente</span><span class="sxs-lookup"><span data-stu-id="56af6-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="56af6-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56af6-144">-DefaultProfile</span></span>
<span data-ttu-id="56af6-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56af6-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56af6-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="56af6-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="56af6-147">Contrassegno per disabilitare la funzionalità attiva Active nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="56af6-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="56af6-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="56af6-149">Contrassegno per abilitare la funzionalità attiva attiva nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="56af6-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="56af6-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="56af6-151">Contrassegno per abilitare la funzionalità attiva attiva nel gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-151">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af6-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="56af6-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="56af6-153">Il sito predefinito da usare per forzare il tunneling.</span><span class="sxs-lookup"><span data-stu-id="56af6-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="56af6-154">Se viene specificato un sito predefinito, tutto il traffico Internet proveniente dalla VNET del gateway viene indirizzato al sito.</span><span class="sxs-lookup"><span data-stu-id="56af6-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="56af6-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="56af6-155">-GatewaySku</span></span>
<span data-ttu-id="56af6-156">SKU del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="56af6-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="56af6-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="56af6-158">BgpPeeringAddresses for Virtual Network Gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="56af6-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="56af6-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="56af6-159">-PeerWeight</span></span>
<span data-ttu-id="56af6-160">Il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56af6-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="56af6-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="56af6-161">-RadiusServerAddress</span></span>
<span data-ttu-id="56af6-162">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="56af6-162">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af6-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="56af6-163">-RadiusServerList</span></span>
<span data-ttu-id="56af6-164">P2S più server RADIUS esterni.</span><span class="sxs-lookup"><span data-stu-id="56af6-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="56af6-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="56af6-165">-RadiusServerSecret</span></span>
<span data-ttu-id="56af6-166">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="56af6-166">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af6-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="56af6-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="56af6-168">Contrassegna per rimuovere l'autenticazione AAD per il client P2S dal gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56af6-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="56af6-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="56af6-169">-Tag</span></span>
<span data-ttu-id="56af6-170">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="56af6-170">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af6-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="56af6-172">L'oggetto gateway di rete virtuale su cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="56af6-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="56af6-173">Questa operazione può essere recuperata usando Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56af6-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="56af6-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="56af6-175">Spazio degli indirizzi per l'assegnazione degli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="56af6-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="56af6-176">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="56af6-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="56af6-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="56af6-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="56af6-178">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="56af6-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="56af6-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="56af6-179">-VpnClientProtocol</span></span>
<span data-ttu-id="56af6-180">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="56af6-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="56af6-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="56af6-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="56af6-182">Elenco dei certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="56af6-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="56af6-183">Un client VPN che presenta un certificato che corrisponde a uno di questi sarà detto di scomparire.</span><span class="sxs-lookup"><span data-stu-id="56af6-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="56af6-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="56af6-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="56af6-185">Elenco dei certificati radice del client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="56af6-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="56af6-186">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="56af6-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="56af6-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56af6-187">-Confirm</span></span>
<span data-ttu-id="56af6-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56af6-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56af6-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56af6-189">-WhatIf</span></span>
<span data-ttu-id="56af6-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56af6-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56af6-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56af6-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56af6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56af6-192">CommonParameters</span></span>
<span data-ttu-id="56af6-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56af6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56af6-194">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56af6-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56af6-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56af6-195">INPUTS</span></span>

### <span data-ttu-id="56af6-196">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="56af6-197">System. String</span><span class="sxs-lookup"><span data-stu-id="56af6-197">System.String</span></span>

### <span data-ttu-id="56af6-198">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="56af6-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="56af6-199">System.String[]</span></span>

### <span data-ttu-id="56af6-200">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="56af6-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="56af6-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="56af6-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="56af6-202">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="56af6-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="56af6-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="56af6-203">System.UInt32</span></span>

### <span data-ttu-id="56af6-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="56af6-204">System.Int32</span></span>

### <span data-ttu-id="56af6-205">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="56af6-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="56af6-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="56af6-206">System.Security.SecureString</span></span>

## <span data-ttu-id="56af6-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56af6-207">OUTPUTS</span></span>

### <span data-ttu-id="56af6-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56af6-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="56af6-209">Note</span><span class="sxs-lookup"><span data-stu-id="56af6-209">NOTES</span></span>

## <span data-ttu-id="56af6-210">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56af6-210">RELATED LINKS</span></span>
