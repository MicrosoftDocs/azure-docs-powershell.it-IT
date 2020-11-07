---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 72aa8af012addf4fa309adc7c63467ecaf667fff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852993"
---
# <span data-ttu-id="7799d-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7799d-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="7799d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7799d-102">SYNOPSIS</span></span>
<span data-ttu-id="7799d-103">Crea una connessione ExpressRoute che connette un gateway ExpressRoute a un circuito ExpressRoute locale</span><span class="sxs-lookup"><span data-stu-id="7799d-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="7799d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7799d-104">SYNTAX</span></span>

### <span data-ttu-id="7799d-105">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7799d-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7799d-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7799d-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7799d-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7799d-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7799d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7799d-108">DESCRIPTION</span></span>
<span data-ttu-id="7799d-109">Crea una connessione ExpressRoute tra un circuito di ExpressRoute locale BGP che scruta il gateway ExpressRoute all'interno di un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="7799d-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="7799d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7799d-110">EXAMPLES</span></span>

### <span data-ttu-id="7799d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7799d-111">Example 1</span></span>

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
```

<span data-ttu-id="7799d-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale, un gateway di Route Express e un circuito di ExpressRoute con peering privato in West Central US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="7799d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7799d-113">Dopo aver creato il gateway, viene collegato al ExpressRoute Circuit peering usando il comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="7799d-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="7799d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7799d-114">PARAMETERS</span></span>

### <span data-ttu-id="7799d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7799d-115">-AsJob</span></span>
<span data-ttu-id="7799d-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7799d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7799d-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7799d-117">-AuthorizationKey</span></span>
<span data-ttu-id="7799d-118">Chiave ottenuta dal proprietario del circuito ExpressRoute per poter creare una connessione con un gateway in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7799d-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="7799d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7799d-119">-DefaultProfile</span></span>
<span data-ttu-id="7799d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7799d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7799d-121">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="7799d-121">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="7799d-122">ID risorsa del circuito Express Route peering a cui deve essere creata questa connessione Express Route gateway.</span><span class="sxs-lookup"><span data-stu-id="7799d-122">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7799d-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="7799d-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="7799d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7799d-124">The resource group name.</span></span>

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

### <span data-ttu-id="7799d-125">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7799d-125">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="7799d-126">ExpressRouteGateway padre per la connessione.</span><span class="sxs-lookup"><span data-stu-id="7799d-126">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="7799d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7799d-127">-Name</span></span>
<span data-ttu-id="7799d-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7799d-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7799d-129">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7799d-129">-ParentResourceId</span></span>
<span data-ttu-id="7799d-130">ID risorsa dell'elemento padre ExpressRouteGateway per la connessione.</span><span class="sxs-lookup"><span data-stu-id="7799d-130">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="7799d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7799d-131">-ResourceGroupName</span></span>
<span data-ttu-id="7799d-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7799d-132">The resource group name.</span></span>

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

### <span data-ttu-id="7799d-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7799d-133">-RoutingWeight</span></span>
<span data-ttu-id="7799d-134">Peso per il routing dei pacchetti che deve essere assegnato alla connessione.</span><span class="sxs-lookup"><span data-stu-id="7799d-134">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="7799d-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7799d-135">-Confirm</span></span>
<span data-ttu-id="7799d-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7799d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7799d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7799d-137">-WhatIf</span></span>
<span data-ttu-id="7799d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7799d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7799d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7799d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7799d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7799d-140">CommonParameters</span></span>
<span data-ttu-id="7799d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7799d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7799d-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7799d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7799d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7799d-143">INPUTS</span></span>

### <span data-ttu-id="7799d-144">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7799d-144">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="7799d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7799d-145">System.String</span></span>

## <span data-ttu-id="7799d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7799d-146">OUTPUTS</span></span>

### <span data-ttu-id="7799d-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7799d-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7799d-148">Note</span><span class="sxs-lookup"><span data-stu-id="7799d-148">NOTES</span></span>

## <span data-ttu-id="7799d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7799d-149">RELATED LINKS</span></span>
