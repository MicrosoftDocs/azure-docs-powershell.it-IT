---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 3e9bd0022215f353388e19edb4f5cc6944acbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993788"
---
# <span data-ttu-id="77fdf-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="77fdf-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="77fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="77fdf-103">Rimuove una expressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="77fdf-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="77fdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77fdf-104">SYNTAX</span></span>

### <span data-ttu-id="77fdf-105">ByExpressRouteConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77fdf-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fdf-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="77fdf-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fdf-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="77fdf-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77fdf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77fdf-108">DESCRIPTION</span></span>
<span data-ttu-id="77fdf-109">Rimuove una expressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="77fdf-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="77fdf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77fdf-110">EXAMPLES</span></span>

### <span data-ttu-id="77fdf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77fdf-111">Example 1</span></span>
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

<span data-ttu-id="77fdf-112">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="77fdf-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="77fdf-113">Successivamente verrà creato un gateway ExpressRoute nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="77fdf-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="77fdf-114">Una volta creato, il gateway viene connesso al sito ExpressRoute usando il comando New-AzExpressRouteConnection></span><span class="sxs-lookup"><span data-stu-id="77fdf-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="77fdf-115">La connessione viene quindi rimossa con il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="77fdf-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="77fdf-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="77fdf-116">Example 2</span></span>

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

<span data-ttu-id="77fdf-117">Come l'esempio 1, ma ora rimuove la connessione con l'oggetto pipe da Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="77fdf-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="77fdf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77fdf-118">PARAMETERS</span></span>

### <span data-ttu-id="77fdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fdf-119">-DefaultProfile</span></span>
<span data-ttu-id="77fdf-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77fdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77fdf-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="77fdf-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="77fdf-122">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="77fdf-122">The parent resource name.</span></span>

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

### <span data-ttu-id="77fdf-123">-Force</span><span class="sxs-lookup"><span data-stu-id="77fdf-123">-Force</span></span>
<span data-ttu-id="77fdf-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="77fdf-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="77fdf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77fdf-125">-InputObject</span></span>
<span data-ttu-id="77fdf-126">Oggetto ExpressRouteConnection da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="77fdf-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="77fdf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="77fdf-127">-Name</span></span>
<span data-ttu-id="77fdf-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="77fdf-128">The resource name.</span></span>

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

### <span data-ttu-id="77fdf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77fdf-129">-PassThru</span></span>
<span data-ttu-id="77fdf-130">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="77fdf-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77fdf-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="77fdf-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77fdf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fdf-132">-ResourceGroupName</span></span>
<span data-ttu-id="77fdf-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77fdf-133">The resource group name.</span></span>

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

### <span data-ttu-id="77fdf-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77fdf-134">-ResourceId</span></span>
<span data-ttu-id="77fdf-135">ID risorsa dell'oggetto ExpressRouteConnection da eliminare.</span><span class="sxs-lookup"><span data-stu-id="77fdf-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="77fdf-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77fdf-136">-Confirm</span></span>
<span data-ttu-id="77fdf-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77fdf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77fdf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77fdf-138">-WhatIf</span></span>
<span data-ttu-id="77fdf-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77fdf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77fdf-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77fdf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77fdf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fdf-141">CommonParameters</span></span>
<span data-ttu-id="77fdf-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77fdf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fdf-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77fdf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fdf-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="77fdf-144">INPUTS</span></span>

### <span data-ttu-id="77fdf-145">System.String</span><span class="sxs-lookup"><span data-stu-id="77fdf-145">System.String</span></span>

### <span data-ttu-id="77fdf-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="77fdf-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="77fdf-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77fdf-147">OUTPUTS</span></span>

### <span data-ttu-id="77fdf-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77fdf-148">System.Boolean</span></span>

## <span data-ttu-id="77fdf-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="77fdf-149">NOTES</span></span>

## <span data-ttu-id="77fdf-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77fdf-150">RELATED LINKS</span></span>
