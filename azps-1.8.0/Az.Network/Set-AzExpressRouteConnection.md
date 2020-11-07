---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 70f349fbb6a97009db4ba11e8de945b0700e3c2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677980"
---
# <span data-ttu-id="94c96-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="94c96-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="94c96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94c96-102">SYNOPSIS</span></span>
<span data-ttu-id="94c96-103">Aggiorna una connessione di route espressa creata tra un gateway di Route Express e il peering del circuito di Route Express locale.</span><span class="sxs-lookup"><span data-stu-id="94c96-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="94c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94c96-104">SYNTAX</span></span>

### <span data-ttu-id="94c96-105">ByExpressRouteConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94c96-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c96-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="94c96-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c96-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="94c96-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94c96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94c96-108">DESCRIPTION</span></span>
<span data-ttu-id="94c96-109">Il cmdlet **set-AzExpressRouteConnection** aggiorna una connessione di route espressa creata tra un gateway Express Route e il peering del circuito di Route Express locale.</span><span class="sxs-lookup"><span data-stu-id="94c96-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="94c96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94c96-110">EXAMPLES</span></span>

### <span data-ttu-id="94c96-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94c96-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="94c96-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e un ExpressRouteSite in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="94c96-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="94c96-113">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="94c96-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="94c96-114">Dopo aver creato il gateway, viene collegato al circuito ExpressRoute locale con il comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="94c96-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="94c96-115">La connessione viene quindi aggiornata per avere un RoutingWeight diverso usando il comando Set-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="94c96-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="94c96-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94c96-116">PARAMETERS</span></span>

### <span data-ttu-id="94c96-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94c96-117">-AsJob</span></span>
<span data-ttu-id="94c96-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="94c96-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94c96-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="94c96-119">-AuthorizationKey</span></span>
<span data-ttu-id="94c96-120">Chiave di autorizzazione da usare per creare la connessione al gateway ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="94c96-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="94c96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c96-121">-DefaultProfile</span></span>
<span data-ttu-id="94c96-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94c96-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c96-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="94c96-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="94c96-124">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="94c96-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94c96-125">-InputObject</span></span>
<span data-ttu-id="94c96-126">L'oggetto ExpressRouteConenction da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="94c96-126">The ExpressRouteConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="94c96-127">-Name</span></span>
<span data-ttu-id="94c96-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="94c96-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c96-129">-ResourceGroupName</span></span>
<span data-ttu-id="94c96-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94c96-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94c96-131">-ResourceId</span></span>
<span data-ttu-id="94c96-132">ID risorsa dell'oggetto ExpressRouteConenction da eliminare.</span><span class="sxs-lookup"><span data-stu-id="94c96-132">The resource id of the ExpressRouteConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="94c96-133">-RoutingWeight</span></span>
<span data-ttu-id="94c96-134">Il peso che deve essere assegnato alla connessione per il routing dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="94c96-134">The weight that needs to be assigned to this connection for packet routing.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c96-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94c96-135">-Confirm</span></span>
<span data-ttu-id="94c96-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c96-137">-WhatIf</span></span>
<span data-ttu-id="94c96-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94c96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c96-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94c96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c96-140">CommonParameters</span></span>
<span data-ttu-id="94c96-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c96-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c96-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c96-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94c96-143">INPUTS</span></span>

### <span data-ttu-id="94c96-144">System. String</span><span class="sxs-lookup"><span data-stu-id="94c96-144">System.String</span></span>

### <span data-ttu-id="94c96-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="94c96-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="94c96-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94c96-146">OUTPUTS</span></span>

### <span data-ttu-id="94c96-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="94c96-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="94c96-148">Note</span><span class="sxs-lookup"><span data-stu-id="94c96-148">NOTES</span></span>

## <span data-ttu-id="94c96-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94c96-149">RELATED LINKS</span></span>