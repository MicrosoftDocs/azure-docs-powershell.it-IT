---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5beb3e7c2c010570089dfd0667eca48e5d1c6728
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687035"
---
# <span data-ttu-id="4f7a3-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f7a3-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="4f7a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f7a3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f7a3-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f7a3-103">SYNTAX</span></span>

### <span data-ttu-id="4f7a3-104">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f7a3-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f7a3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f7a3-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f7a3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f7a3-106">DESCRIPTION</span></span>

## <span data-ttu-id="4f7a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f7a3-107">EXAMPLES</span></span>

### <span data-ttu-id="4f7a3-108">1:</span><span class="sxs-lookup"><span data-stu-id="4f7a3-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="4f7a3-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f7a3-109">PARAMETERS</span></span>

### <span data-ttu-id="4f7a3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f7a3-110">-AsJob</span></span>
<span data-ttu-id="4f7a3-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4f7a3-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f7a3-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4f7a3-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="4f7a3-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7a3-114">-DefaultProfile</span></span>
<span data-ttu-id="4f7a3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4f7a3-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f7a3-117">-Force</span></span>
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

### <span data-ttu-id="4f7a3-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="4f7a3-118">-IpsecPolicies</span></span>
<span data-ttu-id="4f7a3-119">Elenco di criteri IPSec.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="4f7a3-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="4f7a3-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4f7a3-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f7a3-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="4f7a3-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="4f7a3-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7a3-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="4f7a3-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4f7a3-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f7a3-128">-Tag</span></span>
<span data-ttu-id="4f7a3-129">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f7a3-130">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="4f7a3-130">For example:</span></span>

<span data-ttu-id="4f7a3-131">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4f7a3-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="4f7a3-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="4f7a3-133">Usare i selettori del traffico basati su criteri per una connessione S2S</span><span class="sxs-lookup"><span data-stu-id="4f7a3-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="4f7a3-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="4f7a3-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f7a3-136">-Confirm</span></span>
<span data-ttu-id="4f7a3-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7a3-138">-WhatIf</span></span>
<span data-ttu-id="4f7a3-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f7a3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7a3-141">CommonParameters</span></span>
<span data-ttu-id="4f7a3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7a3-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7a3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7a3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f7a3-144">INPUTS</span></span>

### <span data-ttu-id="4f7a3-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f7a3-145">None</span></span>
<span data-ttu-id="4f7a3-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f7a3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f7a3-147">OUTPUTS</span></span>

### <span data-ttu-id="4f7a3-148">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f7a3-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="4f7a3-149">Note</span><span class="sxs-lookup"><span data-stu-id="4f7a3-149">NOTES</span></span>

## <span data-ttu-id="4f7a3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f7a3-150">RELATED LINKS</span></span>

[<span data-ttu-id="4f7a3-151">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f7a3-151">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4f7a3-152">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f7a3-152">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4f7a3-153">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4f7a3-153">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
