---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020492"
---
# <span data-ttu-id="82aa3-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="82aa3-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="82aa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="82aa3-103">Crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="82aa3-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="82aa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82aa3-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82aa3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="82aa3-106">Il cmdlet **Add-AzVirtualNetworkPeering** crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="82aa3-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="82aa3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="82aa3-108">Esempio 1: creare un peering tra due reti virtuali nella stessa area geografica</span><span class="sxs-lookup"><span data-stu-id="82aa3-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="82aa3-109">Tieni presente che è necessario creare un collegamento di peering da vnet1 a vnet2 e viceversa per consentire il peering al lavoro.</span><span class="sxs-lookup"><span data-stu-id="82aa3-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="82aa3-110">Esempio 2: creare un peering tra due reti virtuali in aree geografiche diverse</span><span class="sxs-lookup"><span data-stu-id="82aa3-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="82aa3-111">Qui ' myVnet1' in US West Central è peered with ' myVnet2' in Canada Central.</span><span class="sxs-lookup"><span data-stu-id="82aa3-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="82aa3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82aa3-112">PARAMETERS</span></span>

### <span data-ttu-id="82aa3-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="82aa3-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="82aa3-114">Indica che questo cmdlet consente il traffico inoltrato dalle macchine virtuali nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="82aa3-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="82aa3-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="82aa3-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="82aa3-116">Contrassegno per consentire l'utilizzo di gatewayLinks nel collegamento alla rete virtuale remota della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="82aa3-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="82aa3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82aa3-117">-AsJob</span></span>
<span data-ttu-id="82aa3-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="82aa3-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82aa3-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="82aa3-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="82aa3-120">Indica che questo cmdlet blocca le macchine virtuali nello spazio di rete virtuale collegato per accedere a tutte le macchine virtuali nello spazio di rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="82aa3-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="82aa3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82aa3-121">-DefaultProfile</span></span>
<span data-ttu-id="82aa3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82aa3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82aa3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="82aa3-123">-Name</span></span>
<span data-ttu-id="82aa3-124">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="82aa3-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="82aa3-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="82aa3-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="82aa3-126">Specifica l'ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="82aa3-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="82aa3-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="82aa3-127">-UseRemoteGateways</span></span>
<span data-ttu-id="82aa3-128">Indica che questo cmdlet consente i gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="82aa3-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="82aa3-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82aa3-129">-VirtualNetwork</span></span>
<span data-ttu-id="82aa3-130">Specifica la rete virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="82aa3-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="82aa3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82aa3-131">CommonParameters</span></span>
<span data-ttu-id="82aa3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82aa3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82aa3-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82aa3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82aa3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82aa3-134">INPUTS</span></span>

### <span data-ttu-id="82aa3-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82aa3-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="82aa3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="82aa3-136">System.String</span></span>

## <span data-ttu-id="82aa3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82aa3-137">OUTPUTS</span></span>

### <span data-ttu-id="82aa3-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="82aa3-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="82aa3-139">Note</span><span class="sxs-lookup"><span data-stu-id="82aa3-139">NOTES</span></span>

## <span data-ttu-id="82aa3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82aa3-140">RELATED LINKS</span></span>

[<span data-ttu-id="82aa3-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82aa3-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="82aa3-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="82aa3-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="82aa3-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="82aa3-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="82aa3-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="82aa3-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
