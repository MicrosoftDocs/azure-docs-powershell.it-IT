---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678424"
---
# <span data-ttu-id="4b595-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4b595-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4b595-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b595-102">SYNOPSIS</span></span>
<span data-ttu-id="4b595-103">Ottiene una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4b595-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="4b595-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b595-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b595-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b595-105">DESCRIPTION</span></span>
<span data-ttu-id="4b595-106">Il cmdlet **Get-AzVirtualNetworkSubnetConfig** ottiene una o più configurazioni di subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b595-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="4b595-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b595-107">EXAMPLES</span></span>

### <span data-ttu-id="4b595-108">1: ottenere una subnet in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4b595-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="4b595-109">Questo esempio crea un gruppo di risorse e una rete virtuale con una singola subnet in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b595-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="4b595-110">Recupera quindi i dati relativi alla subnet.</span><span class="sxs-lookup"><span data-stu-id="4b595-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="4b595-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b595-111">PARAMETERS</span></span>

### <span data-ttu-id="4b595-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b595-112">-DefaultProfile</span></span>
<span data-ttu-id="4b595-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b595-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b595-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b595-114">-Name</span></span>
<span data-ttu-id="4b595-115">Specifica il nome della configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b595-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b595-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4b595-116">-VirtualNetwork</span></span>
<span data-ttu-id="4b595-117">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b595-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4b595-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b595-118">CommonParameters</span></span>
<span data-ttu-id="4b595-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b595-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b595-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b595-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b595-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b595-121">INPUTS</span></span>

### <span data-ttu-id="4b595-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4b595-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4b595-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b595-123">OUTPUTS</span></span>

### <span data-ttu-id="4b595-124">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4b595-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4b595-125">Note</span><span class="sxs-lookup"><span data-stu-id="4b595-125">NOTES</span></span>

## <span data-ttu-id="4b595-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b595-126">RELATED LINKS</span></span>

[<span data-ttu-id="4b595-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4b595-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4b595-128">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4b595-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4b595-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4b595-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4b595-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4b595-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


