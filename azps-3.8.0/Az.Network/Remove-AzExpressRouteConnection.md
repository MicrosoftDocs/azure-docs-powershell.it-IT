---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022016"
---
# <span data-ttu-id="5c12d-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="5c12d-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="5c12d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c12d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c12d-103">Rimuove un ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="5c12d-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="5c12d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c12d-104">SYNTAX</span></span>

### <span data-ttu-id="5c12d-105">ByExpressRouteConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c12d-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c12d-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="5c12d-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c12d-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5c12d-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c12d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c12d-108">DESCRIPTION</span></span>
<span data-ttu-id="5c12d-109">Rimuove un ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="5c12d-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="5c12d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c12d-110">EXAMPLES</span></span>

### <span data-ttu-id="5c12d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c12d-111">Example 1</span></span>
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
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="5c12d-112">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="5c12d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5c12d-113">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="5c12d-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5c12d-114">Dopo aver creato il gateway, viene collegato al ExpressRouteSite usando il comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="5c12d-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="5c12d-115">Viene quindi rimossa la connessione usando il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="5c12d-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="5c12d-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5c12d-116">Example 2</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="5c12d-117">Come l'esempio 1, ma ora rimuove la connessione usando l'oggetto piped da Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="5c12d-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="5c12d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c12d-118">PARAMETERS</span></span>

### <span data-ttu-id="5c12d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c12d-119">-DefaultProfile</span></span>
<span data-ttu-id="5c12d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c12d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c12d-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="5c12d-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="5c12d-122">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5c12d-122">The parent resource name.</span></span>

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

### <span data-ttu-id="5c12d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5c12d-123">-Force</span></span>
<span data-ttu-id="5c12d-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5c12d-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c12d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c12d-125">-InputObject</span></span>
<span data-ttu-id="5c12d-126">L'oggetto ExpressRouteConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5c12d-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="5c12d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c12d-127">-Name</span></span>
<span data-ttu-id="5c12d-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c12d-128">The resource name.</span></span>

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

### <span data-ttu-id="5c12d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c12d-129">-PassThru</span></span>
<span data-ttu-id="5c12d-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5c12d-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c12d-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5c12d-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c12d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c12d-132">-ResourceGroupName</span></span>
<span data-ttu-id="5c12d-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c12d-133">The resource group name.</span></span>

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

### <span data-ttu-id="5c12d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c12d-134">-ResourceId</span></span>
<span data-ttu-id="5c12d-135">ID risorsa dell'oggetto ExpressRouteConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5c12d-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="5c12d-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c12d-136">-Confirm</span></span>
<span data-ttu-id="5c12d-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c12d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c12d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c12d-138">-WhatIf</span></span>
<span data-ttu-id="5c12d-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c12d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c12d-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c12d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c12d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c12d-141">CommonParameters</span></span>
<span data-ttu-id="5c12d-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c12d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c12d-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c12d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c12d-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c12d-144">INPUTS</span></span>

### <span data-ttu-id="5c12d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5c12d-145">System.String</span></span>

### <span data-ttu-id="5c12d-146">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="5c12d-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="5c12d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c12d-147">OUTPUTS</span></span>

### <span data-ttu-id="5c12d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c12d-148">System.Boolean</span></span>

## <span data-ttu-id="5c12d-149">Note</span><span class="sxs-lookup"><span data-stu-id="5c12d-149">NOTES</span></span>

## <span data-ttu-id="5c12d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c12d-150">RELATED LINKS</span></span>
