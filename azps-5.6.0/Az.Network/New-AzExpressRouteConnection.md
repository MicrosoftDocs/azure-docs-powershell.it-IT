---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 3089d3654e471bbf31eb81e42e4374525d84010d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974781"
---
# <span data-ttu-id="d6ed8-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d6ed8-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="d6ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ed8-103">Crea una connessione ExpressRoute che connette un gateway ExpressRoute a un circuito ExpressRoute locale</span><span class="sxs-lookup"><span data-stu-id="d6ed8-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="d6ed8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6ed8-104">SYNTAX</span></span>

### <span data-ttu-id="d6ed8-105">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6ed8-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ed8-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d6ed8-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ed8-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ed8-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ed8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6ed8-109">Crea una connessione ExpressRoute tra un peering BGP del circuito BGP locale e il gateway ExpressRoute all'interno di un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="d6ed8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6ed8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6ed8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6ed8-111">Example 1</span></span>

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
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="d6ed8-112">Questa procedura consente di creare un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale, un gateway Express Route e un circuito ExpressRoute con peering privato negli Stati Uniti centrali occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d6ed8-113">Una volta creato, il gateway viene connesso al peering del circuito ExpressRoute usando il comando New-AzExpressRouteConnection></span><span class="sxs-lookup"><span data-stu-id="d6ed8-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="d6ed8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ed8-114">PARAMETERS</span></span>

### <span data-ttu-id="d6ed8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6ed8-115">-AsJob</span></span>
<span data-ttu-id="d6ed8-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d6ed8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6ed8-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="d6ed8-117">-AuthorizationKey</span></span>
<span data-ttu-id="d6ed8-118">Chiave ottenuta dal proprietario del circuito ExpressRoute per poter creare una connessione con un gateway in un abbonamento diverso.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ed8-119">-DefaultProfile</span></span>
<span data-ttu-id="d6ed8-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ed8-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d6ed8-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="d6ed8-122">Abilitare la sicurezza Internet per questa connessione Gateway ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d6ed8-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="d6ed8-123">-ExpressRouteCircuitIingId</span><span class="sxs-lookup"><span data-stu-id="d6ed8-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="d6ed8-124">ID risorsa del peering del circuito Express Route a cui deve essere creata questa connessione gateway Express Route.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="d6ed8-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="d6ed8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d6ed8-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="d6ed8-128">Elemento padre ExpressRouteGateway per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d6ed8-129">-Name</span></span>
<span data-ttu-id="d6ed8-130">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ed8-131">-ParentResourceId</span></span>
<span data-ttu-id="d6ed8-132">ID risorsa dell'elemento padre ExpressRouteGateway per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ed8-133">-ResourceGroupName</span></span>
<span data-ttu-id="d6ed8-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ed8-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6ed8-135">-RoutingConfiguration</span></span>
<span data-ttu-id="d6ed8-136">Configurazione del routing per questa connessione</span><span class="sxs-lookup"><span data-stu-id="d6ed8-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="d6ed8-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d6ed8-137">-RoutingWeight</span></span>
<span data-ttu-id="d6ed8-138">Peso del routing dei pacchetti che deve essere assegnato a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="d6ed8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6ed8-139">-Confirm</span></span>
<span data-ttu-id="d6ed8-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ed8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ed8-141">-WhatIf</span></span>
<span data-ttu-id="d6ed8-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ed8-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ed8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ed8-144">CommonParameters</span></span>
<span data-ttu-id="d6ed8-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ed8-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6ed8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ed8-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6ed8-147">INPUTS</span></span>

### <span data-ttu-id="d6ed8-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d6ed8-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="d6ed8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d6ed8-149">System.String</span></span>

## <span data-ttu-id="d6ed8-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6ed8-150">OUTPUTS</span></span>

### <span data-ttu-id="d6ed8-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d6ed8-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="d6ed8-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6ed8-152">NOTES</span></span>

## <span data-ttu-id="d6ed8-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6ed8-153">RELATED LINKS</span></span>

[<span data-ttu-id="d6ed8-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6ed8-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
