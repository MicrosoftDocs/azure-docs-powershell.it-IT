---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855182"
---
# <span data-ttu-id="e2885-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="e2885-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2885-102">SYNOPSIS</span></span>
<span data-ttu-id="e2885-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="e2885-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2885-104">SYNTAX</span></span>

### <span data-ttu-id="e2885-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2885-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2885-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2885-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2885-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="e2885-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2885-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2885-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2885-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="e2885-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2885-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2885-110">DESCRIPTION</span></span>
<span data-ttu-id="e2885-111">Il cmdlet **set-AzVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="e2885-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2885-112">EXAMPLES</span></span>

### <span data-ttu-id="e2885-113">Esempio 1: aggiornare l'ASN di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e2885-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="e2885-114">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="e2885-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="e2885-115">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="e2885-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="e2885-116">Esempio 2: aggiungere criteri IPsec a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e2885-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="e2885-117">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando crea l'oggetto criteri IPSec VPN in base ai parametri IPSec specificati.</span><span class="sxs-lookup"><span data-stu-id="e2885-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="e2885-118">Il terzo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="e2885-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="e2885-119">Il comando imposta anche il criterio IPSec VPN personalizzato specificato nell'oggetto $vpnclientipsecpolicy sul gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="e2885-120">Esempio 3: aggiungere/aggiornare i tag a un gateway di rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e2885-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="e2885-121">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale Gateway01 con i tag @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="e2885-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="e2885-122">Esempio 4: aggiungere/aggiornare la configurazione di autenticazione AAD per VpnClient di un gateway di rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e2885-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="e2885-123">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale Gateway01 con le configurazioni di autenticazione AAD params: aadTenantUri, aadAudienceId, aadIssuerUri per VpnClient.</span><span class="sxs-lookup"><span data-stu-id="e2885-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="e2885-124">Il terzo comando rimuove la configurazione di autenticazione AAD da VpnClient di Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2885-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="e2885-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2885-125">PARAMETERS</span></span>

### <span data-ttu-id="e2885-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="e2885-126">-AadAudienceId</span></span>
<span data-ttu-id="e2885-127">Opzione di autenticazione P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="e2885-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="e2885-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="e2885-128">-AadIssuerUri</span></span>
<span data-ttu-id="e2885-129">Opzione di autenticazione P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="e2885-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="e2885-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="e2885-130">-AadTenantUri</span></span>
<span data-ttu-id="e2885-131">Opzione di autenticazione P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="e2885-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="e2885-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2885-132">-AsJob</span></span>
<span data-ttu-id="e2885-133">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2885-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2885-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="e2885-134">-Asn</span></span>
<span data-ttu-id="e2885-135">Specifica il codice ASN (Virtual Network Gateway Autonomous System Number) usato per configurare sessioni BGP (Border Gateway Protocol) all'interno di tunnel IPsec.</span><span class="sxs-lookup"><span data-stu-id="e2885-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="e2885-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="e2885-136">-CustomRoute</span></span>
<span data-ttu-id="e2885-137">Route personalizzate AddressPool specificate dal cliente</span><span class="sxs-lookup"><span data-stu-id="e2885-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="e2885-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2885-138">-DefaultProfile</span></span>
<span data-ttu-id="e2885-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2885-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2885-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="e2885-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="e2885-141">Disabilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="e2885-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="e2885-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="e2885-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="e2885-143">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="e2885-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="e2885-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e2885-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="e2885-145">Specifica il sito predefinito da usare per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="e2885-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="e2885-146">Se si specifica un sito predefinito, tutto il traffico Internet proveniente dalla rete privata virtuale (VPN) del gateway viene instradato al sito.</span><span class="sxs-lookup"><span data-stu-id="e2885-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="e2885-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="e2885-147">-GatewaySku</span></span>
<span data-ttu-id="e2885-148">Specifica l'unità di conservazione delle scorte (SKU) del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="e2885-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2885-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e2885-150">Base</span><span class="sxs-lookup"><span data-stu-id="e2885-150">Basic</span></span>
- <span data-ttu-id="e2885-151">Standard</span><span class="sxs-lookup"><span data-stu-id="e2885-151">Standard</span></span>
- <span data-ttu-id="e2885-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="e2885-152">HighPerformance</span></span>
- <span data-ttu-id="e2885-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="e2885-153">VpnGw1</span></span>
- <span data-ttu-id="e2885-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="e2885-154">VpnGw2</span></span>
- <span data-ttu-id="e2885-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="e2885-155">VpnGw3</span></span>
- <span data-ttu-id="e2885-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-156">VpnGw1AZ</span></span>
- <span data-ttu-id="e2885-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-157">VpnGw2AZ</span></span>
- <span data-ttu-id="e2885-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-158">VpnGw3AZ</span></span>
- <span data-ttu-id="e2885-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-159">ErGw1AZ</span></span>
- <span data-ttu-id="e2885-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-160">ErGw2AZ</span></span>
- <span data-ttu-id="e2885-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="e2885-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="e2885-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e2885-162">-PeerWeight</span></span>
<span data-ttu-id="e2885-163">Specifica il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e2885-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="e2885-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="e2885-164">-RadiusServerAddress</span></span>
<span data-ttu-id="e2885-165">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="e2885-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="e2885-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="e2885-166">-RadiusServerSecret</span></span>
<span data-ttu-id="e2885-167">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="e2885-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="e2885-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="e2885-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="e2885-169">Contrassegna per rimuovere l'autenticazione AAD per il client P2S dal gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="e2885-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2885-170">-Tag</span></span>
<span data-ttu-id="e2885-171">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e2885-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e2885-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="e2885-173">Specifica l'oggetto gateway di rete virtuale a cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="e2885-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="e2885-174">Puoi usare il cmdlet Get-AzVirtualNetworkGateway per ottenere l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2885-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="e2885-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2885-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="e2885-176">Specifica lo spazio degli indirizzi usato da questo cmdlet per allocare gli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="e2885-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="e2885-177">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="e2885-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="e2885-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="e2885-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="e2885-179">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="e2885-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="e2885-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="e2885-180">-VpnClientProtocol</span></span>
<span data-ttu-id="e2885-181">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="e2885-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="e2885-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="e2885-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="e2885-183">Specifica un elenco di certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="e2885-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="e2885-184">Viene rimosso un client VPN che presenta un certificato che corrisponde a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="e2885-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="e2885-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="e2885-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="e2885-186">Specifica un elenco di certificati radice client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="e2885-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="e2885-187">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="e2885-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="e2885-188">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2885-188">-Confirm</span></span>
<span data-ttu-id="e2885-189">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2885-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2885-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2885-190">-WhatIf</span></span>
<span data-ttu-id="e2885-191">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2885-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2885-192">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2885-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2885-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2885-193">CommonParameters</span></span>
<span data-ttu-id="e2885-194">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2885-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2885-195">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2885-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2885-196">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2885-196">INPUTS</span></span>

### <span data-ttu-id="e2885-197">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e2885-198">System. String</span><span class="sxs-lookup"><span data-stu-id="e2885-198">System.String</span></span>

### <span data-ttu-id="e2885-199">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="e2885-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="e2885-200">System.String[]</span></span>

### <span data-ttu-id="e2885-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="e2885-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="e2885-202">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="e2885-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="e2885-203">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="e2885-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="e2885-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="e2885-204">System.UInt32</span></span>

### <span data-ttu-id="e2885-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e2885-205">System.Int32</span></span>

### <span data-ttu-id="e2885-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e2885-206">System.Security.SecureString</span></span>

## <span data-ttu-id="e2885-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2885-207">OUTPUTS</span></span>

### <span data-ttu-id="e2885-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e2885-209">Note</span><span class="sxs-lookup"><span data-stu-id="e2885-209">NOTES</span></span>
* <span data-ttu-id="e2885-210">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="e2885-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e2885-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2885-211">RELATED LINKS</span></span>

[<span data-ttu-id="e2885-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e2885-213">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e2885-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e2885-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e2885-216">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e2885-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
