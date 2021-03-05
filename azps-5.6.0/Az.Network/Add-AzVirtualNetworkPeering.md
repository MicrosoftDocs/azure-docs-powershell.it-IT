---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 511ff37071767c9e28164fcf93e985eb773297f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976718"
---
# <span data-ttu-id="d480a-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d480a-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="d480a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d480a-102">SYNOPSIS</span></span>
<span data-ttu-id="d480a-103">Crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="d480a-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="d480a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d480a-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d480a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d480a-105">DESCRIPTION</span></span>
<span data-ttu-id="d480a-106">Il cmdlet **Add-AzVirtualNetworkEndoing** crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="d480a-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="d480a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d480a-107">EXAMPLES</span></span>

### <span data-ttu-id="d480a-108">Esempio 1: Creare un peering tra due reti virtuali nella stessa area geografica</span><span class="sxs-lookup"><span data-stu-id="d480a-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="d480a-109">Si noti che per il funzionamento del peering è necessario creare un collegamento di peering da vnet1 a vnet2 e viceversa.</span><span class="sxs-lookup"><span data-stu-id="d480a-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="d480a-110">Esempio 2: Creare un peering tra due reti virtuali in aree geografiche diverse</span><span class="sxs-lookup"><span data-stu-id="d480a-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="d480a-111">Qui "myVnet1" negli Stati Uniti centro-ovest è associato a "myVnet2" in Canada centrale.</span><span class="sxs-lookup"><span data-stu-id="d480a-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="d480a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d480a-112">PARAMETERS</span></span>

### <span data-ttu-id="d480a-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="d480a-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="d480a-114">Indica che questo cmdlet consente il traffico inoltrato dalle macchine virtuali nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="d480a-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="d480a-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="d480a-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="d480a-116">Flag per consentire l'uso di GatewayLinks nel collegamento della rete virtuale remota a questa rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d480a-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="d480a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d480a-117">-AsJob</span></span>
<span data-ttu-id="d480a-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d480a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d480a-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d480a-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="d480a-120">Indica che questo cmdlet blocca le macchine virtuali nello spazio di rete virtuale collegato per accedere a tutte le macchine virtuali nello spazio di rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="d480a-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="d480a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d480a-121">-DefaultProfile</span></span>
<span data-ttu-id="d480a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d480a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d480a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d480a-123">-Name</span></span>
<span data-ttu-id="d480a-124">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d480a-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="d480a-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d480a-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="d480a-126">Specifica l'ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="d480a-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d480a-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="d480a-127">-UseRemoteGateways</span></span>
<span data-ttu-id="d480a-128">Indica che questo cmdlet consente i gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d480a-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="d480a-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d480a-129">-VirtualNetwork</span></span>
<span data-ttu-id="d480a-130">Specifica la rete virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="d480a-130">Specifies the parent virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d480a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d480a-131">CommonParameters</span></span>
<span data-ttu-id="d480a-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d480a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d480a-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d480a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d480a-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="d480a-134">INPUTS</span></span>

### <span data-ttu-id="d480a-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d480a-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d480a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d480a-136">System.String</span></span>

## <span data-ttu-id="d480a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d480a-137">OUTPUTS</span></span>

### <span data-ttu-id="d480a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkCollectioning</span><span class="sxs-lookup"><span data-stu-id="d480a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="d480a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d480a-139">NOTES</span></span>

## <span data-ttu-id="d480a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d480a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d480a-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d480a-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="d480a-142">Get-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="d480a-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d480a-143">Remove-AzVirtualNetworkCollectioning</span><span class="sxs-lookup"><span data-stu-id="d480a-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d480a-144">Set-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="d480a-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
