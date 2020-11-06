---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510419"
---
# <span data-ttu-id="37f47-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="37f47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37f47-102">SYNOPSIS</span></span>
<span data-ttu-id="37f47-103">Configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37f47-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37f47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37f47-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37f47-105">DESCRIPTION</span></span>
<span data-ttu-id="37f47-106">Il cmdlet **set-AzureRmVirtualNetworkPeering** configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37f47-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="37f47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37f47-107">EXAMPLES</span></span>

### <span data-ttu-id="37f47-108">Esempio 1: modificare la configurazione del traffico inoltrato di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="37f47-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="37f47-109">Esempio 2: modificare l'accesso alla rete virtuale di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="37f47-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="37f47-110">Esempio 3: modificare la configurazione delle proprietà di transito gateway di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="37f47-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="37f47-111">Esempio 4: usare gateway remoti in peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="37f47-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="37f47-112">Modificando questa proprietà in $True, è possibile usare il gateway VNet del peer.</span><span class="sxs-lookup"><span data-stu-id="37f47-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="37f47-113">Tuttavia, il VNet peer deve avere un gateway configurato e **AllowGatewayTransit** deve avere un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="37f47-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="37f47-114">Questa proprietà non può essere usata se è già stato configurato un gateway.</span><span class="sxs-lookup"><span data-stu-id="37f47-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="37f47-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37f47-115">PARAMETERS</span></span>

### <span data-ttu-id="37f47-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="37f47-117">Specifica il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37f47-117">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="37f47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f47-118">-DefaultProfile</span></span>
<span data-ttu-id="37f47-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37f47-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f47-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f47-120">CommonParameters</span></span>
<span data-ttu-id="37f47-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f47-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f47-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f47-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f47-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37f47-123">INPUTS</span></span>

### <span data-ttu-id="37f47-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="37f47-125">Il parametro ' VirtualNetworkPeering ' accetta il valore di tipo ' PSVirtualNetworkPeering ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="37f47-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="37f47-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37f47-126">OUTPUTS</span></span>

### <span data-ttu-id="37f47-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="37f47-128">Note</span><span class="sxs-lookup"><span data-stu-id="37f47-128">NOTES</span></span>

## <span data-ttu-id="37f47-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37f47-129">RELATED LINKS</span></span>

[<span data-ttu-id="37f47-130">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="37f47-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="37f47-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="37f47-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


