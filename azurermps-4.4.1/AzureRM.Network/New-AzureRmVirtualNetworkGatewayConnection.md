---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0c619b306d6dece23006d351f666637afe9f852a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510471"
---
# <span data-ttu-id="31e6c-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e6c-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31e6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31e6c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e6c-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31e6c-103">SYNTAX</span></span>

### <span data-ttu-id="31e6c-104">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31e6c-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e6c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31e6c-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e6c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31e6c-106">DESCRIPTION</span></span>

## <span data-ttu-id="31e6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="31e6c-108">1:</span><span class="sxs-lookup"><span data-stu-id="31e6c-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="31e6c-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31e6c-109">PARAMETERS</span></span>

### <span data-ttu-id="31e6c-110">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="31e6c-110">-AuthorizationKey</span></span>
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

### <span data-ttu-id="31e6c-111">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="31e6c-111">-ConnectionType</span></span>
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

### <span data-ttu-id="31e6c-112">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="31e6c-112">-EnableBgp</span></span>
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

### <span data-ttu-id="31e6c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="31e6c-113">-Force</span></span>
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

### <span data-ttu-id="31e6c-114">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="31e6c-114">-IpsecPolicies</span></span>
<span data-ttu-id="31e6c-115">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="31e6c-115">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="31e6c-116">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31e6c-116">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="31e6c-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="31e6c-117">-Location</span></span>
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

### <span data-ttu-id="31e6c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="31e6c-118">-Name</span></span>
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

### <span data-ttu-id="31e6c-119">-Peer</span><span class="sxs-lookup"><span data-stu-id="31e6c-119">-Peer</span></span>
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

### <span data-ttu-id="31e6c-120">-PeerId</span><span class="sxs-lookup"><span data-stu-id="31e6c-120">-PeerId</span></span>
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

### <span data-ttu-id="31e6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e6c-121">-ResourceGroupName</span></span>
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

### <span data-ttu-id="31e6c-122">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="31e6c-122">-RoutingWeight</span></span>
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

### <span data-ttu-id="31e6c-123">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="31e6c-123">-SharedKey</span></span>
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

### <span data-ttu-id="31e6c-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="31e6c-124">-Tag</span></span>
<span data-ttu-id="31e6c-125">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="31e6c-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31e6c-126">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="31e6c-126">For example:</span></span>

<span data-ttu-id="31e6c-127">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="31e6c-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31e6c-128">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="31e6c-128">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="31e6c-129">Usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="31e6c-129">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="31e6c-130">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="31e6c-130">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="31e6c-131">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31e6c-131">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="31e6c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31e6c-132">-Confirm</span></span>
<span data-ttu-id="31e6c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e6c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e6c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e6c-134">-WhatIf</span></span>
<span data-ttu-id="31e6c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e6c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e6c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e6c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e6c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e6c-137">-DefaultProfile</span></span>
<span data-ttu-id="31e6c-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31e6c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e6c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e6c-139">CommonParameters</span></span>
<span data-ttu-id="31e6c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e6c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e6c-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e6c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e6c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31e6c-142">INPUTS</span></span>

## <span data-ttu-id="31e6c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31e6c-143">OUTPUTS</span></span>

### <span data-ttu-id="31e6c-144">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e6c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31e6c-145">Note</span><span class="sxs-lookup"><span data-stu-id="31e6c-145">NOTES</span></span>

## <span data-ttu-id="31e6c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31e6c-146">RELATED LINKS</span></span>

[<span data-ttu-id="31e6c-147">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e6c-147">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31e6c-148">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e6c-148">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31e6c-149">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e6c-149">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
