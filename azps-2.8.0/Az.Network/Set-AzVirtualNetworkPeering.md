---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: bbe047def99ef2300c2002a2e8d5beedef26fd4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855162"
---
# <span data-ttu-id="8cf79-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="8cf79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cf79-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf79-103">Configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cf79-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="8cf79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf79-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cf79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf79-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf79-106">Il cmdlet **set-AzVirtualNetworkPeering** configura un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cf79-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="8cf79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf79-107">EXAMPLES</span></span>

### <span data-ttu-id="8cf79-108">Esempio 1: modificare la configurazione del traffico inoltrato di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8cf79-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="8cf79-109">Esempio 2: modificare l'accesso alla rete virtuale di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8cf79-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="8cf79-110">Esempio 3: modificare la configurazione delle proprietà di transito gateway di un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8cf79-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="8cf79-111">Esempio 4: usare gateway remoti in peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8cf79-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="8cf79-112">Modificando questa proprietà in $True, è possibile usare il gateway VNet del peer.</span><span class="sxs-lookup"><span data-stu-id="8cf79-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="8cf79-113">Tuttavia, il VNet peer deve avere un gateway configurato e **AllowGatewayTransit** deve avere un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="8cf79-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="8cf79-114">Questa proprietà non può essere usata se è già stato configurato un gateway.</span><span class="sxs-lookup"><span data-stu-id="8cf79-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="8cf79-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cf79-115">PARAMETERS</span></span>

### <span data-ttu-id="8cf79-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cf79-116">-AsJob</span></span>
<span data-ttu-id="8cf79-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8cf79-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cf79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf79-118">-DefaultProfile</span></span>
<span data-ttu-id="8cf79-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cf79-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="8cf79-121">Specifica il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cf79-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="8cf79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf79-122">CommonParameters</span></span>
<span data-ttu-id="8cf79-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf79-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf79-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cf79-125">INPUTS</span></span>

### <span data-ttu-id="8cf79-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="8cf79-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf79-127">OUTPUTS</span></span>

### <span data-ttu-id="8cf79-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="8cf79-129">Note</span><span class="sxs-lookup"><span data-stu-id="8cf79-129">NOTES</span></span>

## <span data-ttu-id="8cf79-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf79-130">RELATED LINKS</span></span>

[<span data-ttu-id="8cf79-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="8cf79-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="8cf79-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cf79-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
