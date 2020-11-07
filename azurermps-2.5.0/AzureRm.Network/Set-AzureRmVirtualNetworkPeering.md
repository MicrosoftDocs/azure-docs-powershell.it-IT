---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: d6f258bf15ac89dc0321c61ab592ef9fc6e58a7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865733"
---
# <span data-ttu-id="c9028-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="c9028-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9028-102">SYNOPSIS</span></span>
<span data-ttu-id="c9028-103">Configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9028-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9028-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9028-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9028-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9028-105">DESCRIPTION</span></span>
<span data-ttu-id="c9028-106">Il cmdlet **set-AzureRmVirtualNetworkPeering** configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9028-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="c9028-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9028-107">EXAMPLES</span></span>

### <span data-ttu-id="c9028-108">Esempio 1: modificare la configurazione del traffico inoltrato di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c9028-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="c9028-109">Esempio 2: modificare l'accesso alla rete virtuale di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c9028-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="c9028-110">Esempio 3: modificare la configurazione delle proprietà di transito gateway di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c9028-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="c9028-111">Esempio 4: usare gateway remoti in peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c9028-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="c9028-112">Modificando questa proprietà in $True, è possibile usare il gateway VNet del peer.</span><span class="sxs-lookup"><span data-stu-id="c9028-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="c9028-113">Tuttavia, il VNet peer deve avere un gateway configurato e **AllowGatewayTransit** deve avere un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="c9028-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="c9028-114">Questa proprietà non può essere usata se è già stato configurato un gateway.</span><span class="sxs-lookup"><span data-stu-id="c9028-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="c9028-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9028-115">PARAMETERS</span></span>

### <span data-ttu-id="c9028-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9028-116">-AsJob</span></span>
<span data-ttu-id="c9028-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c9028-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9028-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9028-118">-DefaultProfile</span></span>
<span data-ttu-id="c9028-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9028-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9028-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="c9028-121">Specifica il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9028-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9028-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9028-122">CommonParameters</span></span>
<span data-ttu-id="c9028-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9028-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9028-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9028-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9028-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9028-125">INPUTS</span></span>

### <span data-ttu-id="c9028-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="c9028-127">Il parametro ' VirtualNetworkPeering ' accetta il valore di tipo ' PSVirtualNetworkPeering ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c9028-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="c9028-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9028-128">OUTPUTS</span></span>

### <span data-ttu-id="c9028-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="c9028-130">Note</span><span class="sxs-lookup"><span data-stu-id="c9028-130">NOTES</span></span>

## <span data-ttu-id="c9028-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9028-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9028-132">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="c9028-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="c9028-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c9028-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


