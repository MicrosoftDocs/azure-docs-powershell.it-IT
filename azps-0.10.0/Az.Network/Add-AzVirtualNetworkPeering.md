---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 440c1395c30f396ff1ae2430828cac7aae675734
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860953"
---
# <span data-ttu-id="a1cac-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1cac-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="a1cac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1cac-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cac-103">Crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="a1cac-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="a1cac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1cac-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1cac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1cac-105">DESCRIPTION</span></span>
<span data-ttu-id="a1cac-106">Il cmdlet **Add-AzVirtualNetworkPeering** crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="a1cac-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="a1cac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1cac-107">EXAMPLES</span></span>

### <span data-ttu-id="a1cac-108">Esempio 1: creare un peering tra due reti virtuali nella stessa area geografica</span><span class="sxs-lookup"><span data-stu-id="a1cac-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="a1cac-109">Tieni presente che è necessario creare un collegamento di peering da vnet1 a vnet2 e viceversa per consentire il peering al lavoro.</span><span class="sxs-lookup"><span data-stu-id="a1cac-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="a1cac-110">Esempio 2: creare un peering tra due reti virtuali in aree geografiche diverse</span><span class="sxs-lookup"><span data-stu-id="a1cac-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="a1cac-111">Qui ' myVnet1' in US West Central è peered with ' myVnet2' in Canada Central.</span><span class="sxs-lookup"><span data-stu-id="a1cac-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="a1cac-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1cac-112">PARAMETERS</span></span>

### <span data-ttu-id="a1cac-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="a1cac-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="a1cac-114">Indica che questo cmdlet consente il traffico inoltrato dalle macchine virtuali nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="a1cac-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="a1cac-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="a1cac-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="a1cac-116">Contrassegno per consentire l'utilizzo di gatewayLinks nel collegamento alla rete virtuale remota della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a1cac-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1cac-117">-AsJob</span></span>
<span data-ttu-id="a1cac-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a1cac-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1cac-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a1cac-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="a1cac-120">Indica che questo cmdlet blocca le macchine virtuali nello spazio di rete virtuale collegato per accedere a tutte le macchine virtuali nello spazio di rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="a1cac-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="a1cac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cac-121">-DefaultProfile</span></span>
<span data-ttu-id="a1cac-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1cac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1cac-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1cac-123">-Name</span></span>
<span data-ttu-id="a1cac-124">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1cac-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cac-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a1cac-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="a1cac-126">Specifica l'ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="a1cac-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cac-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="a1cac-127">-UseRemoteGateways</span></span>
<span data-ttu-id="a1cac-128">Indica che questo cmdlet consente i gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1cac-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="a1cac-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1cac-129">-VirtualNetwork</span></span>
<span data-ttu-id="a1cac-130">Specifica la rete virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="a1cac-130">Specifies the parent virtual network.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cac-131">CommonParameters</span></span>
<span data-ttu-id="a1cac-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1cac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cac-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1cac-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cac-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1cac-134">INPUTS</span></span>

### <span data-ttu-id="a1cac-135">Stringa</span><span class="sxs-lookup"><span data-stu-id="a1cac-135">String</span></span>
<span data-ttu-id="a1cac-136">Il parametro ' RemoteVirtualNetworkId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a1cac-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a1cac-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1cac-137">PSVirtualNetwork</span></span>
<span data-ttu-id="a1cac-138">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a1cac-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a1cac-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1cac-139">OUTPUTS</span></span>

### <span data-ttu-id="a1cac-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1cac-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="a1cac-141">Note</span><span class="sxs-lookup"><span data-stu-id="a1cac-141">NOTES</span></span>

## <span data-ttu-id="a1cac-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1cac-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1cac-143">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1cac-143">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="a1cac-144">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1cac-144">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a1cac-145">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1cac-145">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a1cac-146">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1cac-146">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


