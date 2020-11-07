---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867025"
---
# <span data-ttu-id="00c4d-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00c4d-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="00c4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="00c4d-103">Ottiene una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00c4d-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00c4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00c4d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="00c4d-106">Il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** ottiene una o più configurazioni di subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="00c4d-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="00c4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="00c4d-108">1: ottenere una subnet in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="00c4d-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="00c4d-109">Questo esempio crea un gruppo di risorse e una rete virtuale con una singola subnet in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00c4d-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="00c4d-110">Recupera quindi i dati relativi alla subnet.</span><span class="sxs-lookup"><span data-stu-id="00c4d-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="00c4d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00c4d-111">PARAMETERS</span></span>

### <span data-ttu-id="00c4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c4d-112">-DefaultProfile</span></span>
<span data-ttu-id="00c4d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00c4d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c4d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c4d-114">-Name</span></span>
<span data-ttu-id="00c4d-115">Specifica il nome della configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c4d-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00c4d-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00c4d-116">-VirtualNetwork</span></span>
<span data-ttu-id="00c4d-117">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c4d-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00c4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c4d-118">CommonParameters</span></span>
<span data-ttu-id="00c4d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c4d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c4d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c4d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00c4d-121">INPUTS</span></span>

### <span data-ttu-id="00c4d-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00c4d-122">PSVirtualNetwork</span></span>
<span data-ttu-id="00c4d-123">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="00c4d-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="00c4d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00c4d-124">OUTPUTS</span></span>

### <span data-ttu-id="00c4d-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="00c4d-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="00c4d-126">Note</span><span class="sxs-lookup"><span data-stu-id="00c4d-126">NOTES</span></span>

## <span data-ttu-id="00c4d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00c4d-127">RELATED LINKS</span></span>

[<span data-ttu-id="00c4d-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00c4d-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="00c4d-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00c4d-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="00c4d-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00c4d-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="00c4d-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00c4d-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


