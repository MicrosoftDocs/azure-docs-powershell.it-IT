---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c25b311a4f99814c718ce825d61433d7c2fee192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854377"
---
# <span data-ttu-id="18d3f-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18d3f-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="18d3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="18d3f-103">Crea la connessione VPN da sito a sito tra il gateway di rete virtuale e il dispositivo VPN On-Prem.</span><span class="sxs-lookup"><span data-stu-id="18d3f-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="18d3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18d3f-104">SYNTAX</span></span>

### <span data-ttu-id="18d3f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18d3f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18d3f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="18d3f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18d3f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18d3f-107">DESCRIPTION</span></span>
<span data-ttu-id="18d3f-108">Crea la connessione VPN da sito a sito tra il gateway di rete virtuale e il dispositivo VPN On-Prem.</span><span class="sxs-lookup"><span data-stu-id="18d3f-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="18d3f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18d3f-109">EXAMPLES</span></span>

### <span data-ttu-id="18d3f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18d3f-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="18d3f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18d3f-111">PARAMETERS</span></span>

### <span data-ttu-id="18d3f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18d3f-112">-AsJob</span></span>
<span data-ttu-id="18d3f-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="18d3f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18d3f-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="18d3f-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="18d3f-115">-ConnectionProtocol</span></span>
<span data-ttu-id="18d3f-116">Protocollo di connessione gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="18d3f-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="18d3f-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d3f-118">-DefaultProfile</span></span>
<span data-ttu-id="18d3f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18d3f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18d3f-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="18d3f-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="18d3f-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="18d3f-122">-Force</span></span>

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

### <span data-ttu-id="18d3f-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="18d3f-123">-IpsecPolicies</span></span>
<span data-ttu-id="18d3f-124">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="18d3f-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-125">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="18d3f-125">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="18d3f-126">Elenco dei criteri del selettore del traffico.</span><span class="sxs-lookup"><span data-stu-id="18d3f-126">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-127">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="18d3f-127">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="18d3f-128">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="18d3f-129">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-130">-Peer</span><span class="sxs-lookup"><span data-stu-id="18d3f-130">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-131">-PeerId</span><span class="sxs-lookup"><span data-stu-id="18d3f-131">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d3f-132">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="18d3f-133">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="18d3f-134">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="18d3f-135">-Tag</span></span>
<span data-ttu-id="18d3f-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18d3f-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18d3f-137">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="18d3f-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-138">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="18d3f-138">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="18d3f-139">Usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="18d3f-139">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-140">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="18d3f-140">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-141">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="18d3f-141">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18d3f-142">-Confirm</span></span>
<span data-ttu-id="18d3f-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18d3f-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18d3f-144">-WhatIf</span></span>
<span data-ttu-id="18d3f-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18d3f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18d3f-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18d3f-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d3f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d3f-147">CommonParameters</span></span>
<span data-ttu-id="18d3f-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d3f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d3f-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d3f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d3f-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18d3f-150">INPUTS</span></span>

### <span data-ttu-id="18d3f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="18d3f-151">System.String</span></span>

### <span data-ttu-id="18d3f-152">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18d3f-152">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="18d3f-153">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18d3f-153">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="18d3f-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="18d3f-154">System.Int32</span></span>

### <span data-ttu-id="18d3f-155">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="18d3f-155">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="18d3f-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18d3f-156">System.Boolean</span></span>

### <span data-ttu-id="18d3f-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18d3f-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18d3f-158">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="18d3f-158">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="18d3f-159">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="18d3f-159">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="18d3f-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18d3f-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18d3f-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18d3f-161">OUTPUTS</span></span>

### <span data-ttu-id="18d3f-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18d3f-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="18d3f-163">Note</span><span class="sxs-lookup"><span data-stu-id="18d3f-163">NOTES</span></span>

## <span data-ttu-id="18d3f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18d3f-164">RELATED LINKS</span></span>

[<span data-ttu-id="18d3f-165">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18d3f-165">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="18d3f-166">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18d3f-166">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="18d3f-167">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18d3f-167">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
