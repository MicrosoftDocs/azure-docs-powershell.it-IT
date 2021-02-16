---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179567"
---
# <span data-ttu-id="610cc-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="610cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="610cc-102">SYNOPSIS</span></span>
<span data-ttu-id="610cc-103">Crea una connessione IPSec che connette una VpnGateway a un ramo del cliente remoto rappresentato in RM come VpnSite.</span><span class="sxs-lookup"><span data-stu-id="610cc-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="610cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="610cc-104">SYNTAX</span></span>

### <span data-ttu-id="610cc-105">ByVpnGatewayNameByVpnSiteObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="610cc-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="610cc-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="610cc-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cc-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="610cc-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cc-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="610cc-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cc-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="610cc-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cc-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="610cc-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="610cc-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="610cc-111">DESCRIPTION</span></span>
<span data-ttu-id="610cc-112">Crea una connessione IPSec che connette una VpnGateway a un ramo del cliente remoto rappresentato in RM come VpnSite.</span><span class="sxs-lookup"><span data-stu-id="610cc-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="610cc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="610cc-113">EXAMPLES</span></span>

### <span data-ttu-id="610cc-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="610cc-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="610cc-115">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="610cc-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="610cc-116">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="610cc-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="610cc-117">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection></span><span class="sxs-lookup"><span data-stu-id="610cc-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="610cc-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="610cc-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="610cc-119">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn con 1 VpnSiteLinks negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="610cc-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="610cc-120">Successivamente verrà creato un gateway VPN nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="610cc-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="610cc-121">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection con 1 VpnSiteLinkConnections a VpnSiteLink del sito Vpn.</span><span class="sxs-lookup"><span data-stu-id="610cc-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="610cc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="610cc-122">PARAMETERS</span></span>

### <span data-ttu-id="610cc-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="610cc-123">-AsJob</span></span>
<span data-ttu-id="610cc-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="610cc-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="610cc-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="610cc-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="610cc-126">La larghezza di banda che deve essere gestita da questa connessione in mbps.</span><span class="sxs-lookup"><span data-stu-id="610cc-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610cc-127">-DefaultProfile</span></span>
<span data-ttu-id="610cc-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="610cc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610cc-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="610cc-129">-EnableBgp</span></span>
<span data-ttu-id="610cc-130">Abilita BGP per questa connessione</span><span class="sxs-lookup"><span data-stu-id="610cc-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="610cc-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="610cc-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="610cc-132">Abilita la sicurezza Internet per questa connessione</span><span class="sxs-lookup"><span data-stu-id="610cc-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="610cc-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="610cc-133">-IpSecPolicy</span></span>
<span data-ttu-id="610cc-134">La larghezza di banda che deve essere gestita da questa connessione in mbps.</span><span class="sxs-lookup"><span data-stu-id="610cc-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-135">-Name</span><span class="sxs-lookup"><span data-stu-id="610cc-135">-Name</span></span>
<span data-ttu-id="610cc-136">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="610cc-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="610cc-137">-ParentObject</span></span>
<span data-ttu-id="610cc-138">VpnGateway padre per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="610cc-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="610cc-139">-ParentResourceId</span></span>
<span data-ttu-id="610cc-140">ID risorsa di VpnGateway padre per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="610cc-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="610cc-141">-ParentResourceName</span></span>
<span data-ttu-id="610cc-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="610cc-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610cc-143">-ResourceGroupName</span></span>
<span data-ttu-id="610cc-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="610cc-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="610cc-145">-RoutingConfiguration</span></span>
<span data-ttu-id="610cc-146">Configurazione del routing per questa connessione</span><span class="sxs-lookup"><span data-stu-id="610cc-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="610cc-147">-SharedKey</span></span>
<span data-ttu-id="610cc-148">Chiave condivisa necessaria per configurare la connessione.</span><span class="sxs-lookup"><span data-stu-id="610cc-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="610cc-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="610cc-150">Usare l'indirizzo IP azure locale come indirizzo di origine durante l'avvio della connessione.</span><span class="sxs-lookup"><span data-stu-id="610cc-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="610cc-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="610cc-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="610cc-152">Usare selettori del traffico basati su criteri per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="610cc-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="610cc-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="610cc-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="610cc-154">Protocollo di connessione del gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="610cc-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="610cc-155">-VpnSite</span></span>
<span data-ttu-id="610cc-156">Sito vpn remoto a cui è connessa questa connessione di rete virtuale dell'hub.</span><span class="sxs-lookup"><span data-stu-id="610cc-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="610cc-157">-VpnSiteId</span></span>
<span data-ttu-id="610cc-158">Sito vpn remoto a cui è connessa questa connessione di rete virtuale dell'hub.</span><span class="sxs-lookup"><span data-stu-id="610cc-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="610cc-160">Elenco di VpnSiteLinkConnections di cui dispone questa VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="610cc-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="610cc-161">-Confirm</span></span>
<span data-ttu-id="610cc-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="610cc-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="610cc-163">-WhatIf</span></span>
<span data-ttu-id="610cc-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="610cc-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="610cc-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="610cc-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610cc-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610cc-166">CommonParameters</span></span>
<span data-ttu-id="610cc-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610cc-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610cc-168">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="610cc-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610cc-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="610cc-169">INPUTS</span></span>

### <span data-ttu-id="610cc-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="610cc-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="610cc-171">System.String</span><span class="sxs-lookup"><span data-stu-id="610cc-171">System.String</span></span>

## <span data-ttu-id="610cc-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="610cc-172">OUTPUTS</span></span>

### <span data-ttu-id="610cc-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="610cc-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="610cc-174">NOTES</span></span>

## <span data-ttu-id="610cc-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="610cc-175">RELATED LINKS</span></span>

[<span data-ttu-id="610cc-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="610cc-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="610cc-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="610cc-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="610cc-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="610cc-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
