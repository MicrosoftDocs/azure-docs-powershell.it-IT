---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 6ad7f5fcdaafed47d7292444370e332188f444b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301981"
---
# <span data-ttu-id="5d6bd-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d6bd-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="5d6bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6bd-103">Ottiene una connessione VPN per nome o elenca tutte le connessioni VPN connesse a un VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="5d6bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d6bd-104">SYNTAX</span></span>

### <span data-ttu-id="5d6bd-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d6bd-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d6bd-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="5d6bd-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d6bd-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6bd-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d6bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d6bd-108">DESCRIPTION</span></span>
<span data-ttu-id="5d6bd-109">Ottiene una connessione VPN per nome o elenca tutte le connessioni VPN connesse a un VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="5d6bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d6bd-110">EXAMPLES</span></span>

### <span data-ttu-id="5d6bd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d6bd-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
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

<span data-ttu-id="5d6bd-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un VpnSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5d6bd-113">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5d6bd-114">Dopo aver creato il gateway, viene collegato al VpnSite usando il comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="5d6bd-115">Ottiene quindi la connessione usando il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="5d6bd-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5d6bd-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
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

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
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

<span data-ttu-id="5d6bd-117">Questo cmdlet consente di ottenere tutte le connessioni che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="5d6bd-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="5d6bd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d6bd-118">PARAMETERS</span></span>

### <span data-ttu-id="5d6bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6bd-119">-DefaultProfile</span></span>
<span data-ttu-id="5d6bd-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d6bd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d6bd-121">-Name</span></span>
<span data-ttu-id="5d6bd-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6bd-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5d6bd-123">-ParentObject</span></span>
<span data-ttu-id="5d6bd-124">VpnGateway padre per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6bd-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6bd-125">-ParentResourceId</span></span>
<span data-ttu-id="5d6bd-126">ID risorsa dell'elemento padre VpnGateway per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6bd-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5d6bd-127">-ParentResourceName</span></span>
<span data-ttu-id="5d6bd-128">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6bd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6bd-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d6bd-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6bd-131">CommonParameters</span></span>
<span data-ttu-id="5d6bd-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6bd-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d6bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6bd-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d6bd-134">INPUTS</span></span>

### <span data-ttu-id="5d6bd-135">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d6bd-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="5d6bd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5d6bd-136">System.String</span></span>

## <span data-ttu-id="5d6bd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d6bd-137">OUTPUTS</span></span>

### <span data-ttu-id="5d6bd-138">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d6bd-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="5d6bd-139">Note</span><span class="sxs-lookup"><span data-stu-id="5d6bd-139">NOTES</span></span>

## <span data-ttu-id="5d6bd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d6bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d6bd-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d6bd-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="5d6bd-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d6bd-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="5d6bd-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d6bd-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
