---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 9c1d07a8e8c02b57a67b009f0ebe438134d7d56c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021421"
---
# <span data-ttu-id="dacdb-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="dacdb-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="dacdb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dacdb-102">SYNOPSIS</span></span>
<span data-ttu-id="dacdb-103">Ottiene una connessione ExpressRoute per nome o elenca tutte le connessioni ExpressRoute connesse a un ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="dacdb-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="dacdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dacdb-104">SYNTAX</span></span>

### <span data-ttu-id="dacdb-105">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dacdb-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dacdb-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dacdb-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dacdb-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="dacdb-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dacdb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dacdb-108">DESCRIPTION</span></span>
<span data-ttu-id="dacdb-109">Ottiene una connessione ExpressRoute per nome o elenca tutte le connessioni ExpressRoute connesse a un ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="dacdb-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="dacdb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dacdb-110">EXAMPLES</span></span>

### <span data-ttu-id="dacdb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dacdb-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="dacdb-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un ExpressRouteSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="dacdb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="dacdb-113">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dacdb-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="dacdb-114">Dopo aver creato il gateway, viene collegato al circuito ExpressRoute locale usando il comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="dacdb-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="dacdb-115">Ottiene quindi la connessione usando il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="dacdb-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="dacdb-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dacdb-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="dacdb-117">Questo comando otterrà tutte le connessioni in ExpressRoute "testExpressRoutegw" che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="dacdb-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="dacdb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dacdb-118">PARAMETERS</span></span>

### <span data-ttu-id="dacdb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacdb-119">-DefaultProfile</span></span>
<span data-ttu-id="dacdb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dacdb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacdb-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="dacdb-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="dacdb-122">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="dacdb-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacdb-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dacdb-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="dacdb-124">ExpressRouteGateway padre per la connessione.</span><span class="sxs-lookup"><span data-stu-id="dacdb-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dacdb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="dacdb-125">-Name</span></span>
<span data-ttu-id="dacdb-126">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dacdb-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="dacdb-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dacdb-127">-ParentResourceId</span></span>
<span data-ttu-id="dacdb-128">ID risorsa dell'elemento padre ExpressRouteGateway per la connessione.</span><span class="sxs-lookup"><span data-stu-id="dacdb-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dacdb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacdb-129">-ResourceGroupName</span></span>
<span data-ttu-id="dacdb-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dacdb-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacdb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacdb-131">CommonParameters</span></span>
<span data-ttu-id="dacdb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dacdb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacdb-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dacdb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacdb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dacdb-134">INPUTS</span></span>

### <span data-ttu-id="dacdb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dacdb-135">System.String</span></span>

## <span data-ttu-id="dacdb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dacdb-136">OUTPUTS</span></span>

### <span data-ttu-id="dacdb-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="dacdb-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="dacdb-138">Note</span><span class="sxs-lookup"><span data-stu-id="dacdb-138">NOTES</span></span>

## <span data-ttu-id="dacdb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dacdb-139">RELATED LINKS</span></span>
