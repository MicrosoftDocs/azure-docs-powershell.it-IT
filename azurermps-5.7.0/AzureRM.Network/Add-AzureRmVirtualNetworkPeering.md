---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 1a27b43a7767fab6fee7cc89098ef045dde8529c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685722"
---
# <span data-ttu-id="97f00-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="97f00-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="97f00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97f00-102">SYNOPSIS</span></span>
<span data-ttu-id="97f00-103">Crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="97f00-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97f00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97f00-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97f00-105">DESCRIPTION</span></span>
<span data-ttu-id="97f00-106">Il cmdlet **Add-AzureRmVirtualNetworkPeering** crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="97f00-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="97f00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97f00-107">EXAMPLES</span></span>

### <span data-ttu-id="97f00-108">Esempio 1: creare un peering tra due reti virtuali nella stessa area geografica</span><span class="sxs-lookup"><span data-stu-id="97f00-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="97f00-109">Tieni presente che è necessario creare un collegamento di peering da vnet1 a vnet2 e viceversa per consentire il peering al lavoro.</span><span class="sxs-lookup"><span data-stu-id="97f00-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="97f00-110">Esempio 2: creare un peering tra due reti virtuali in aree geografiche diverse</span><span class="sxs-lookup"><span data-stu-id="97f00-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="97f00-111">Qui ' myVnet1' in US West Central è peered with ' myVnet2' in Canada Central.</span><span class="sxs-lookup"><span data-stu-id="97f00-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="97f00-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97f00-112">PARAMETERS</span></span>

### <span data-ttu-id="97f00-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="97f00-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="97f00-114">Indica che questo cmdlet consente il traffico inoltrato dalle macchine virtuali nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="97f00-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="97f00-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="97f00-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="97f00-116">Contrassegno per consentire l'utilizzo di gatewayLinks nel collegamento alla rete virtuale remota della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="97f00-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="97f00-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97f00-117">-AsJob</span></span>
<span data-ttu-id="97f00-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="97f00-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97f00-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="97f00-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="97f00-120">Indica che questo cmdlet blocca le macchine virtuali nello spazio di rete virtuale collegato per accedere a tutte le macchine virtuali nello spazio di rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="97f00-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="97f00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f00-121">-DefaultProfile</span></span>
<span data-ttu-id="97f00-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97f00-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97f00-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="97f00-123">-Name</span></span>
<span data-ttu-id="97f00-124">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="97f00-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="97f00-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="97f00-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="97f00-126">Specifica l'ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="97f00-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="97f00-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="97f00-127">-UseRemoteGateways</span></span>
<span data-ttu-id="97f00-128">Indica che questo cmdlet consente i gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="97f00-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="97f00-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97f00-129">-VirtualNetwork</span></span>
<span data-ttu-id="97f00-130">Specifica la rete virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="97f00-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="97f00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f00-131">CommonParameters</span></span>
<span data-ttu-id="97f00-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f00-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f00-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f00-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97f00-134">INPUTS</span></span>

### <span data-ttu-id="97f00-135">Stringa</span><span class="sxs-lookup"><span data-stu-id="97f00-135">String</span></span>
<span data-ttu-id="97f00-136">Il parametro ' RemoteVirtualNetworkId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="97f00-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="97f00-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97f00-137">PSVirtualNetwork</span></span>
<span data-ttu-id="97f00-138">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="97f00-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="97f00-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97f00-139">OUTPUTS</span></span>

### <span data-ttu-id="97f00-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="97f00-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="97f00-141">Note</span><span class="sxs-lookup"><span data-stu-id="97f00-141">NOTES</span></span>

## <span data-ttu-id="97f00-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97f00-142">RELATED LINKS</span></span>

[<span data-ttu-id="97f00-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97f00-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="97f00-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="97f00-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="97f00-145">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="97f00-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="97f00-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="97f00-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


