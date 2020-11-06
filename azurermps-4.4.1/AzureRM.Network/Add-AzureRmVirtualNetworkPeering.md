---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7a26e563c8416f31178855acb2d97f318001f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520035"
---
# <span data-ttu-id="1ba7f-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1ba7f-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="1ba7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ba7f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba7f-103">Crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ba7f-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ba7f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ba7f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba7f-106">Il cmdlet **Add-AzureRmVirtualNetworkPeering** crea un peering tra due reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="1ba7f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ba7f-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba7f-108">Esempio 1: creare un peering tra due reti virtuali nella stessa area geografica</span><span class="sxs-lookup"><span data-stu-id="1ba7f-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="1ba7f-109">Tieni presente che è necessario creare un collegamento di peering da vnet1 a vnet2 e viceversa per consentire il peering al lavoro.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="1ba7f-110">Esempio 2: creare un peering tra due reti virtuali in aree geografiche diverse</span><span class="sxs-lookup"><span data-stu-id="1ba7f-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="1ba7f-111">Qui ' myVnet1' in US West Central è peered with ' myVnet2' in Canada Central.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="1ba7f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ba7f-112">PARAMETERS</span></span>

### <span data-ttu-id="1ba7f-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="1ba7f-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="1ba7f-114">Indica che questo cmdlet consente il traffico inoltrato dalle macchine virtuali nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="1ba7f-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="1ba7f-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="1ba7f-116">Contrassegno per consentire l'utilizzo di gatewayLinks nel collegamento alla rete virtuale remota della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1ba7f-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba7f-117">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1ba7f-117">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="1ba7f-118">Indica che questo cmdlet blocca le macchine virtuali nello spazio di rete virtuale collegato per accedere a tutte le macchine virtuali nello spazio di rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-118">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="1ba7f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ba7f-119">-Name</span></span>
<span data-ttu-id="1ba7f-120">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-120">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="1ba7f-121">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1ba7f-121">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="1ba7f-122">Specifica l'ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-122">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="1ba7f-123">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="1ba7f-123">-UseRemoteGateways</span></span>
<span data-ttu-id="1ba7f-124">Indica che questo cmdlet consente i gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-124">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="1ba7f-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba7f-125">-VirtualNetwork</span></span>
<span data-ttu-id="1ba7f-126">Specifica la rete virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-126">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="1ba7f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba7f-127">-DefaultProfile</span></span>
<span data-ttu-id="1ba7f-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ba7f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba7f-129">CommonParameters</span></span>
<span data-ttu-id="1ba7f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba7f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba7f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba7f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ba7f-132">INPUTS</span></span>

### <span data-ttu-id="1ba7f-133">Stringa</span><span class="sxs-lookup"><span data-stu-id="1ba7f-133">String</span></span>
<span data-ttu-id="1ba7f-134">Il parametro ' RemoteVirtualNetworkId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1ba7f-134">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1ba7f-135">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba7f-135">PSVirtualNetwork</span></span>
<span data-ttu-id="1ba7f-136">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1ba7f-136">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1ba7f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ba7f-137">OUTPUTS</span></span>

### <span data-ttu-id="1ba7f-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1ba7f-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="1ba7f-139">Note</span><span class="sxs-lookup"><span data-stu-id="1ba7f-139">NOTES</span></span>

## <span data-ttu-id="1ba7f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ba7f-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ba7f-141">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba7f-141">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="1ba7f-142">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1ba7f-142">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1ba7f-143">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1ba7f-143">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1ba7f-144">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1ba7f-144">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


