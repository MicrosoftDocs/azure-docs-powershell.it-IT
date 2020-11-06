---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 531eab9d8b1405b34a4676cd3e06430cfeda0680
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515576"
---
# <span data-ttu-id="44911-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44911-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="44911-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44911-102">SYNOPSIS</span></span>
<span data-ttu-id="44911-103">Ottiene una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="44911-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44911-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44911-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44911-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44911-105">DESCRIPTION</span></span>
<span data-ttu-id="44911-106">Il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** ottiene una o più configurazioni di subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="44911-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="44911-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44911-107">EXAMPLES</span></span>

### <span data-ttu-id="44911-108">1: ottenere una subnet in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="44911-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="44911-109">Questo esempio crea un gruppo di risorse e una rete virtuale con una singola subnet in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44911-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="44911-110">Recupera quindi i dati relativi alla subnet.</span><span class="sxs-lookup"><span data-stu-id="44911-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="44911-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44911-111">PARAMETERS</span></span>

### <span data-ttu-id="44911-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44911-112">-DefaultProfile</span></span>
<span data-ttu-id="44911-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44911-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44911-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="44911-114">-Name</span></span>
<span data-ttu-id="44911-115">Specifica il nome della configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44911-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="44911-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44911-116">-VirtualNetwork</span></span>
<span data-ttu-id="44911-117">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44911-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="44911-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44911-118">CommonParameters</span></span>
<span data-ttu-id="44911-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44911-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44911-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44911-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44911-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44911-121">INPUTS</span></span>

### <span data-ttu-id="44911-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44911-122">PSVirtualNetwork</span></span>
<span data-ttu-id="44911-123">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="44911-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="44911-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44911-124">OUTPUTS</span></span>

### <span data-ttu-id="44911-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="44911-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="44911-126">Note</span><span class="sxs-lookup"><span data-stu-id="44911-126">NOTES</span></span>

## <span data-ttu-id="44911-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44911-127">RELATED LINKS</span></span>

[<span data-ttu-id="44911-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44911-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44911-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44911-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44911-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44911-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44911-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44911-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


