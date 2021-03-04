---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 1f24dd8cff058b49c9661da1d2f5f2ae927e1a0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952030"
---
# <span data-ttu-id="ea7cb-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ea7cb-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="ea7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7cb-103">Configura il peering di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="ea7cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea7cb-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7cb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7cb-106">Il cmdlet **Set-AzVirtualNetworkIng configura** il peering di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="ea7cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea7cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7cb-108">Esempio 1: Modificare la configurazione del traffico inoltrato di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ea7cb-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="ea7cb-109">Esempio 2: Modificare l'accesso alla rete virtuale di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ea7cb-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="ea7cb-110">Esempio 3: Modificare la configurazione della proprietà di transito del gateway di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ea7cb-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="ea7cb-111">Esempio 4: Usare gateway remoti nel peering della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ea7cb-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="ea7cb-112">Impostando questa proprietà su $True, è possibile usare il gateway VNet del peer.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="ea7cb-113">Tuttavia, la rete vNet peer deve avere un gateway configurato e **AllowGatewayTransit** deve avere un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="ea7cb-114">Questa proprietà non può essere usata se un gateway è già stato configurato.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="ea7cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea7cb-115">PARAMETERS</span></span>

### <span data-ttu-id="ea7cb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea7cb-116">-AsJob</span></span>
<span data-ttu-id="ea7cb-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea7cb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea7cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7cb-118">-DefaultProfile</span></span>
<span data-ttu-id="ea7cb-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7cb-120">-VirtualNetwork Colleghiing</span><span class="sxs-lookup"><span data-stu-id="ea7cb-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="ea7cb-121">Specifica il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-121">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7cb-122">CommonParameters</span></span>
<span data-ttu-id="ea7cb-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7cb-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7cb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7cb-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea7cb-125">INPUTS</span></span>

### <span data-ttu-id="ea7cb-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkIng</span><span class="sxs-lookup"><span data-stu-id="ea7cb-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ea7cb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea7cb-127">OUTPUTS</span></span>

### <span data-ttu-id="ea7cb-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkIng</span><span class="sxs-lookup"><span data-stu-id="ea7cb-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ea7cb-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea7cb-129">NOTES</span></span>

## <span data-ttu-id="ea7cb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea7cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ea7cb-131">Add-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="ea7cb-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ea7cb-132">Get-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="ea7cb-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ea7cb-133">Remove-AzVirtualNetworkCollectioning</span><span class="sxs-lookup"><span data-stu-id="ea7cb-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
