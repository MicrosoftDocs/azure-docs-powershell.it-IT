---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 742f1341401a5dab75f9cbf2f15f3698009589a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513576"
---
# <span data-ttu-id="5353e-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="5353e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5353e-102">SYNOPSIS</span></span>
<span data-ttu-id="5353e-103">Configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5353e-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5353e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5353e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5353e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5353e-105">DESCRIPTION</span></span>
<span data-ttu-id="5353e-106">Il cmdlet **set-AzureRmVirtualNetworkPeering** configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5353e-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="5353e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5353e-107">EXAMPLES</span></span>

### <span data-ttu-id="5353e-108">Esempio 1: modificare la configurazione del traffico inoltrato di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5353e-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="5353e-109">Esempio 2: modificare l'accesso alla rete virtuale di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5353e-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="5353e-110">Esempio 3: modificare la configurazione delle proprietà di transito gateway di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5353e-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="5353e-111">Esempio 4: usare gateway remoti in peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5353e-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="5353e-112">Modificando questa proprietà in $True, è possibile usare il gateway VNet del peer.</span><span class="sxs-lookup"><span data-stu-id="5353e-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="5353e-113">Tuttavia, il VNet peer deve avere un gateway configurato e **AllowGatewayTransit** deve avere un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="5353e-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="5353e-114">Questa proprietà non può essere usata se è già stato configurato un gateway.</span><span class="sxs-lookup"><span data-stu-id="5353e-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="5353e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5353e-115">PARAMETERS</span></span>

### <span data-ttu-id="5353e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5353e-116">-AsJob</span></span>
<span data-ttu-id="5353e-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5353e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5353e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5353e-118">-DefaultProfile</span></span>
<span data-ttu-id="5353e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5353e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5353e-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="5353e-121">Specifica il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5353e-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="5353e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5353e-122">CommonParameters</span></span>
<span data-ttu-id="5353e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5353e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5353e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5353e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5353e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5353e-125">INPUTS</span></span>

### <span data-ttu-id="5353e-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>
<span data-ttu-id="5353e-127">Parametri: VirtualNetworkPeering (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5353e-127">Parameters: VirtualNetworkPeering (ByValue)</span></span>

## <span data-ttu-id="5353e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5353e-128">OUTPUTS</span></span>

### <span data-ttu-id="5353e-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="5353e-130">Note</span><span class="sxs-lookup"><span data-stu-id="5353e-130">NOTES</span></span>

## <span data-ttu-id="5353e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5353e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5353e-132">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5353e-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5353e-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5353e-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


