---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860633"
---
# <span data-ttu-id="4ca37-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4ca37-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4ca37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ca37-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca37-103">Ottiene una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ca37-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="4ca37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ca37-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ca37-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca37-106">Il cmdlet **Get-AzVirtualNetworkSubnetConfig** ottiene una o più configurazioni di subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca37-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="4ca37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ca37-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca37-108">1: ottenere una subnet in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4ca37-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="4ca37-109">Questo esempio crea un gruppo di risorse e una rete virtuale con una singola subnet in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ca37-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="4ca37-110">Recupera quindi i dati relativi alla subnet.</span><span class="sxs-lookup"><span data-stu-id="4ca37-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="4ca37-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ca37-111">PARAMETERS</span></span>

### <span data-ttu-id="4ca37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca37-112">-DefaultProfile</span></span>
<span data-ttu-id="4ca37-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca37-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca37-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ca37-114">-Name</span></span>
<span data-ttu-id="4ca37-115">Specifica il nome della configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca37-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca37-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ca37-116">-VirtualNetwork</span></span>
<span data-ttu-id="4ca37-117">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca37-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4ca37-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca37-118">CommonParameters</span></span>
<span data-ttu-id="4ca37-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca37-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca37-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca37-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca37-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ca37-121">INPUTS</span></span>

### <span data-ttu-id="4ca37-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ca37-122">PSVirtualNetwork</span></span>
<span data-ttu-id="4ca37-123">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4ca37-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4ca37-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ca37-124">OUTPUTS</span></span>

### <span data-ttu-id="4ca37-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4ca37-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4ca37-126">Note</span><span class="sxs-lookup"><span data-stu-id="4ca37-126">NOTES</span></span>

## <span data-ttu-id="4ca37-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ca37-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ca37-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4ca37-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4ca37-129">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4ca37-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4ca37-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4ca37-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4ca37-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4ca37-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


