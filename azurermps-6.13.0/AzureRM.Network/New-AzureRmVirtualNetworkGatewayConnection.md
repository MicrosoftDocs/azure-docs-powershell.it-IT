---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: a9ad0933ce42dc0d031d9ca44d9b5ff7b84d6b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519252"
---
# <span data-ttu-id="79309-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="79309-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="79309-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79309-102">SYNOPSIS</span></span>
<span data-ttu-id="79309-103">Crea la connessione VPN da sito a sito tra il gateway di rete virtuale e il dispositivo VPN On-Prem.</span><span class="sxs-lookup"><span data-stu-id="79309-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79309-104">SYNTAX</span></span>

### <span data-ttu-id="79309-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79309-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79309-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79309-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79309-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79309-107">DESCRIPTION</span></span>
<span data-ttu-id="79309-108">Crea la connessione VPN da sito a sito tra il gateway di rete virtuale e il dispositivo VPN On-Prem.</span><span class="sxs-lookup"><span data-stu-id="79309-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="79309-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79309-109">EXAMPLES</span></span>

### <span data-ttu-id="79309-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79309-110">Example 1</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="79309-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79309-111">PARAMETERS</span></span>

### <span data-ttu-id="79309-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79309-112">-AsJob</span></span>
<span data-ttu-id="79309-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="79309-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79309-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="79309-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="79309-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="79309-115">-ConnectionType</span></span>

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

### <span data-ttu-id="79309-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79309-116">-DefaultProfile</span></span>
<span data-ttu-id="79309-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79309-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79309-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="79309-118">-EnableBgp</span></span>

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

### <span data-ttu-id="79309-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="79309-119">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input:  True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79309-120">-Force</span><span class="sxs-lookup"><span data-stu-id="79309-120">-Force</span></span>

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

### <span data-ttu-id="79309-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="79309-121">-IpsecPolicies</span></span>
<span data-ttu-id="79309-122">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="79309-122">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79309-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="79309-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="79309-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79309-124">-Location</span></span>

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

### <span data-ttu-id="79309-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="79309-125">-Name</span></span>

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

### <span data-ttu-id="79309-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="79309-126">-Peer</span></span>

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

### <span data-ttu-id="79309-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="79309-127">-PeerId</span></span>

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

### <span data-ttu-id="79309-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79309-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="79309-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="79309-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="79309-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="79309-130">-SharedKey</span></span>

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

### <span data-ttu-id="79309-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="79309-131">-Tag</span></span>
<span data-ttu-id="79309-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="79309-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79309-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="79309-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79309-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="79309-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="79309-135">Usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="79309-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="79309-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="79309-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="79309-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="79309-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="79309-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79309-138">-Confirm</span></span>
<span data-ttu-id="79309-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79309-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79309-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79309-140">-WhatIf</span></span>
<span data-ttu-id="79309-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79309-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79309-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79309-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79309-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79309-143">CommonParameters</span></span>
<span data-ttu-id="79309-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79309-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79309-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79309-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79309-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79309-146">INPUTS</span></span>

### <span data-ttu-id="79309-147">System. String</span><span class="sxs-lookup"><span data-stu-id="79309-147">System.String</span></span>

### <span data-ttu-id="79309-148">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79309-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="79309-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79309-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="79309-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="79309-150">System.Int32</span></span>

### <span data-ttu-id="79309-151">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="79309-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="79309-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79309-152">System.Boolean</span></span>

### <span data-ttu-id="79309-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79309-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="79309-154">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79309-154">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79309-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79309-155">OUTPUTS</span></span>

### <span data-ttu-id="79309-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="79309-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="79309-157">Note</span><span class="sxs-lookup"><span data-stu-id="79309-157">NOTES</span></span>

## <span data-ttu-id="79309-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79309-158">RELATED LINKS</span></span>

[<span data-ttu-id="79309-159">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="79309-159">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="79309-160">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="79309-160">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="79309-161">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="79309-161">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
