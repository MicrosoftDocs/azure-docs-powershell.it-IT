---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 3de80ca92f86ab969b9d44ffc9f63871486d969a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951469"
---
# <span data-ttu-id="a6ca5-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="a6ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ca5-103">Aggiorna una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="a6ca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6ca5-104">SYNTAX</span></span>

### <span data-ttu-id="a6ca5-105">ByVpnConnectionName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6ca5-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ca5-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ca5-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ca5-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a6ca5-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ca5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6ca5-108">DESCRIPTION</span></span>
<span data-ttu-id="a6ca5-109">Il cmdlet **Update-AzVpnConnection** aggiorna una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="a6ca5-110">La connessione VPN crea una connessione IPsec che connette un gateway VPN a un ramo del cliente remoto rappresentato in Azure come sito VPN.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="a6ca5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6ca5-111">EXAMPLES</span></span>

### <span data-ttu-id="a6ca5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6ca5-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="a6ca5-113">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a6ca5-114">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a6ca5-115">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection></span><span class="sxs-lookup"><span data-stu-id="a6ca5-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="a6ca5-116">La connessione viene quindi aggiornata in modo da avere un nuovo IpSecPolicy usando il comando Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="a6ca5-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6ca5-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="a6ca5-118">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un sito Vpn negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a6ca5-119">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a6ca5-120">Una volta creato, il gateway viene connesso a VpnSite usando il comando New-AzVpnConnection></span><span class="sxs-lookup"><span data-stu-id="a6ca5-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="a6ca5-121">La connessione viene quindi aggiornata in modo da avere una nuova chiave condivisa usando il costrutto di stringa di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="a6ca5-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6ca5-122">PARAMETERS</span></span>

### <span data-ttu-id="a6ca5-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6ca5-123">-AsJob</span></span>
<span data-ttu-id="a6ca5-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a6ca5-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6ca5-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="a6ca5-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="a6ca5-126">La larghezza di banda che deve essere gestita da questa connessione in mbps.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="a6ca5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ca5-127">-DefaultProfile</span></span>
<span data-ttu-id="a6ca5-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ca5-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a6ca5-129">-EnableBgp</span></span>
<span data-ttu-id="a6ca5-130">Abilita BGP per questa connessione</span><span class="sxs-lookup"><span data-stu-id="a6ca5-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a6ca5-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="a6ca5-132">Abilita la sicurezza Internet per questa connessione</span><span class="sxs-lookup"><span data-stu-id="a6ca5-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6ca5-133">-InputObject</span></span>
<span data-ttu-id="a6ca5-134">L'oggetto VpnConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="a6ca5-135">-IpSecPolicy</span></span>
<span data-ttu-id="a6ca5-136">La larghezza di banda che deve essere gestita da questa connessione in mbps.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="a6ca5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a6ca5-137">-Name</span></span>
<span data-ttu-id="a6ca5-138">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a6ca5-139">-ParentResourceName</span></span>
<span data-ttu-id="a6ca5-140">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ca5-141">-ResourceGroupName</span></span>
<span data-ttu-id="a6ca5-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ca5-143">-ResourceId</span></span>
<span data-ttu-id="a6ca5-144">ID risorsa dell'oggetto VpnConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6ca5-145">-RoutingConfiguration</span></span>
<span data-ttu-id="a6ca5-146">Configurazione del routing per questa connessione</span><span class="sxs-lookup"><span data-stu-id="a6ca5-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="a6ca5-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a6ca5-147">-SharedKey</span></span>
<span data-ttu-id="a6ca5-148">Chiave condivisa necessaria per configurare la connessione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="a6ca5-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="a6ca5-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="a6ca5-150">Usare l'indirizzo IP azure locale come indirizzo di origine durante l'avvio della connessione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a6ca5-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a6ca5-152">Usare selettori del traffico basati su criteri per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ca5-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="a6ca5-154">L'elenco di VpnSiteLinkConnections di cui ha bisogno vpnConnection.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="a6ca5-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6ca5-155">-Confirm</span></span>
<span data-ttu-id="a6ca5-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ca5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ca5-157">-WhatIf</span></span>
<span data-ttu-id="a6ca5-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ca5-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ca5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ca5-160">CommonParameters</span></span>
<span data-ttu-id="a6ca5-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ca5-162">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ca5-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6ca5-163">INPUTS</span></span>

### <span data-ttu-id="a6ca5-164">System.String</span><span class="sxs-lookup"><span data-stu-id="a6ca5-164">System.String</span></span>

### <span data-ttu-id="a6ca5-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a6ca5-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6ca5-166">OUTPUTS</span></span>

### <span data-ttu-id="a6ca5-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a6ca5-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6ca5-168">NOTES</span></span>

## <span data-ttu-id="a6ca5-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6ca5-169">RELATED LINKS</span></span>

[<span data-ttu-id="a6ca5-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="a6ca5-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="a6ca5-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6ca5-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="a6ca5-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6ca5-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
