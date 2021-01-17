---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367247"
---
# <span data-ttu-id="833af-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="833af-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="833af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="833af-102">SYNOPSIS</span></span>
<span data-ttu-id="833af-103">Ottiene una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="833af-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="833af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="833af-104">SYNTAX</span></span>

### <span data-ttu-id="833af-105">GetByVirtualNetwork (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="833af-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="833af-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="833af-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="833af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="833af-107">DESCRIPTION</span></span>
<span data-ttu-id="833af-108">Il cmdlet **Get-AzVirtualNetworkSubnetConfig** ottiene una o più configurazioni di subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="833af-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="833af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="833af-109">EXAMPLES</span></span>

### <span data-ttu-id="833af-110">1: ottenere una subnet in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="833af-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="833af-111">Questo esempio crea un gruppo di risorse e una rete virtuale con una singola subnet in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="833af-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="833af-112">Recupera quindi i dati relativi alla subnet.</span><span class="sxs-lookup"><span data-stu-id="833af-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="833af-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="833af-113">PARAMETERS</span></span>

### <span data-ttu-id="833af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833af-114">-DefaultProfile</span></span>
<span data-ttu-id="833af-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="833af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="833af-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="833af-116">-Name</span></span>
<span data-ttu-id="833af-117">Specifica il nome della configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833af-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833af-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="833af-118">-ResourceId</span></span>
<span data-ttu-id="833af-119">Specifica l'ID risorsa della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833af-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="833af-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="833af-120">-VirtualNetwork</span></span>
<span data-ttu-id="833af-121">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833af-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="833af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833af-122">CommonParameters</span></span>
<span data-ttu-id="833af-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="833af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833af-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="833af-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833af-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="833af-125">INPUTS</span></span>

### <span data-ttu-id="833af-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="833af-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="833af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="833af-127">System.String</span></span>

## <span data-ttu-id="833af-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="833af-128">OUTPUTS</span></span>

### <span data-ttu-id="833af-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="833af-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="833af-130">Note</span><span class="sxs-lookup"><span data-stu-id="833af-130">NOTES</span></span>

## <span data-ttu-id="833af-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="833af-131">RELATED LINKS</span></span>

[<span data-ttu-id="833af-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="833af-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="833af-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="833af-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="833af-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="833af-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="833af-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="833af-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
