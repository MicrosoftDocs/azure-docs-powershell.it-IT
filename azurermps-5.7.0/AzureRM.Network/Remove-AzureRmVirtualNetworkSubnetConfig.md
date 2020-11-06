---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 42765b56f0376466acb51e04d8ab6ce4a2eee1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515540"
---
# <span data-ttu-id="a238b-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a238b-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a238b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a238b-102">SYNOPSIS</span></span>
<span data-ttu-id="a238b-103">Rimuove una configurazione della subnet da una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a238b-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a238b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a238b-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a238b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a238b-105">DESCRIPTION</span></span>
<span data-ttu-id="a238b-106">Il cmdlet **Remove-AzureRmVirtualNetworkSubnetConfig** consente di rimuovere una subnet da una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a238b-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="a238b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a238b-107">EXAMPLES</span></span>

### <span data-ttu-id="a238b-108">1: rimuovere una subnet da una rete virtuale e aggiornare la rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a238b-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="a238b-109">Questo esempio crea un gruppo di risorse e una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="a238b-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="a238b-110">Viene quindi usato il comando Remove-AzureRmVirtualNetworkSubnetConfig per rimuovere la subnet backend dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a238b-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a238b-111">Set-AzureRmVirtualNetwork viene quindi chiamato per modificare la rete virtuale sul lato server.</span><span class="sxs-lookup"><span data-stu-id="a238b-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="a238b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a238b-112">PARAMETERS</span></span>

### <span data-ttu-id="a238b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a238b-113">-DefaultProfile</span></span>
<span data-ttu-id="a238b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a238b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a238b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a238b-115">-Name</span></span>
<span data-ttu-id="a238b-116">Specifica il nome della configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a238b-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="a238b-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a238b-117">-VirtualNetwork</span></span>
<span data-ttu-id="a238b-118">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a238b-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="a238b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a238b-119">CommonParameters</span></span>
<span data-ttu-id="a238b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a238b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a238b-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a238b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a238b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a238b-122">INPUTS</span></span>

### <span data-ttu-id="a238b-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a238b-123">PSVirtualNetwork</span></span>
<span data-ttu-id="a238b-124">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a238b-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a238b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a238b-125">OUTPUTS</span></span>

### <span data-ttu-id="a238b-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a238b-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a238b-127">Note</span><span class="sxs-lookup"><span data-stu-id="a238b-127">NOTES</span></span>

## <span data-ttu-id="a238b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a238b-128">RELATED LINKS</span></span>

[<span data-ttu-id="a238b-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a238b-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a238b-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a238b-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a238b-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a238b-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a238b-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a238b-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


