---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022469"
---
# <span data-ttu-id="9c3cd-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="9c3cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3cd-103">Aggiorna una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="9c3cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c3cd-104">SYNTAX</span></span>

### <span data-ttu-id="9c3cd-105">ByVpnConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c3cd-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c3cd-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="9c3cd-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c3cd-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="9c3cd-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c3cd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c3cd-108">DESCRIPTION</span></span>
<span data-ttu-id="9c3cd-109">Il cmdlet **Update-AzVpnConnection** aggiorna una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="9c3cd-110">La connessione VPN crea una connessione IPsec che connette un gateway VPN a un ramo cliente remoto rappresentato in Azure come sito VPN.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="9c3cd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c3cd-111">EXAMPLES</span></span>

### <span data-ttu-id="9c3cd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c3cd-112">Example 1</span></span>

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
```

<span data-ttu-id="9c3cd-113">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9c3cd-114">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9c3cd-115">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="9c3cd-116">La connessione viene quindi aggiornata per avere un nuovo IpSecPolicy usando il comando Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="9c3cd-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9c3cd-117">Example 2</span></span>

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
```

<span data-ttu-id="9c3cd-118">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9c3cd-119">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9c3cd-120">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="9c3cd-121">La connessione viene quindi aggiornata per avere una nuova chiave condivisa usando il costrutto di stringa sicura.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="9c3cd-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c3cd-122">PARAMETERS</span></span>

### <span data-ttu-id="9c3cd-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c3cd-123">-AsJob</span></span>
<span data-ttu-id="9c3cd-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9c3cd-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c3cd-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="9c3cd-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="9c3cd-126">Larghezza di banda che deve essere gestita da questa connessione in Mbps.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="9c3cd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3cd-127">-DefaultProfile</span></span>
<span data-ttu-id="9c3cd-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c3cd-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="9c3cd-129">-EnableBgp</span></span>
<span data-ttu-id="9c3cd-130">Abilitare BGP per la connessione</span><span class="sxs-lookup"><span data-stu-id="9c3cd-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="9c3cd-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="9c3cd-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="9c3cd-132">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="9c3cd-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="9c3cd-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c3cd-133">-InputObject</span></span>
<span data-ttu-id="9c3cd-134">L'oggetto VpnConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="9c3cd-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="9c3cd-135">-IpSecPolicy</span></span>
<span data-ttu-id="9c3cd-136">Larghezza di banda che deve essere gestita da questa connessione in Mbps.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="9c3cd-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c3cd-137">-Name</span></span>
<span data-ttu-id="9c3cd-138">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-138">The resource name.</span></span>

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

### <span data-ttu-id="9c3cd-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9c3cd-139">-ParentResourceName</span></span>
<span data-ttu-id="9c3cd-140">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-140">The parent resource name.</span></span>

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

### <span data-ttu-id="9c3cd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3cd-141">-ResourceGroupName</span></span>
<span data-ttu-id="9c3cd-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-142">The resource group name.</span></span>

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

### <span data-ttu-id="9c3cd-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c3cd-143">-ResourceId</span></span>
<span data-ttu-id="9c3cd-144">ID risorsa dell'oggetto VpnConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="9c3cd-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9c3cd-145">-SharedKey</span></span>
<span data-ttu-id="9c3cd-146">Chiave condivisa necessaria per impostare la connessione.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="9c3cd-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="9c3cd-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="9c3cd-148">Usare l'indirizzo IP locale di Azure come indirizzo di origine durante l'avvio della connessione.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="9c3cd-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="9c3cd-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="9c3cd-150">Usare i selettori del traffico basati su criteri per la connessione.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="9c3cd-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="9c3cd-152">L'elenco di VpnSiteLinkConnections che deve avere questo VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="9c3cd-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c3cd-153">-Confirm</span></span>
<span data-ttu-id="9c3cd-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c3cd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c3cd-155">-WhatIf</span></span>
<span data-ttu-id="9c3cd-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c3cd-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c3cd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3cd-158">CommonParameters</span></span>
<span data-ttu-id="9c3cd-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3cd-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c3cd-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3cd-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c3cd-161">INPUTS</span></span>

### <span data-ttu-id="9c3cd-162">System. String</span><span class="sxs-lookup"><span data-stu-id="9c3cd-162">System.String</span></span>

### <span data-ttu-id="9c3cd-163">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="9c3cd-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c3cd-164">OUTPUTS</span></span>

### <span data-ttu-id="9c3cd-165">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="9c3cd-166">Note</span><span class="sxs-lookup"><span data-stu-id="9c3cd-166">NOTES</span></span>

## <span data-ttu-id="9c3cd-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c3cd-167">RELATED LINKS</span></span>

[<span data-ttu-id="9c3cd-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="9c3cd-169">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="9c3cd-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9c3cd-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
