---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5f05672c5fd3f0866652507fd0f61f7a8b6e0fcc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862893"
---
# <span data-ttu-id="9e3c7-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e3c7-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9e3c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3c7-103">Rimuove una configurazione della subnet da una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="9e3c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e3c7-105">DESCRIPTION</span></span>
<span data-ttu-id="9e3c7-106">Il cmdlet **Remove-AzVirtualNetworkSubnetConfig** consente di rimuovere una subnet da una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="9e3c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-107">EXAMPLES</span></span>

### <span data-ttu-id="9e3c7-108">1: rimuovere una subnet da una rete virtuale e aggiornare la rete virtuale</span><span class="sxs-lookup"><span data-stu-id="9e3c7-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9e3c7-109">Questo esempio crea un gruppo di risorse e una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="9e3c7-110">Viene quindi usato il comando Remove-AzVirtualNetworkSubnetConfig per rimuovere la subnet backend dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9e3c7-111">Set-AzVirtualNetwork viene quindi chiamato per modificare la rete virtuale sul lato server.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="9e3c7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3c7-113">-DefaultProfile</span></span>
<span data-ttu-id="9e3c7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3c7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e3c7-115">-Name</span></span>
<span data-ttu-id="9e3c7-116">Specifica il nome della configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9e3c7-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e3c7-117">-VirtualNetwork</span></span>
<span data-ttu-id="9e3c7-118">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9e3c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3c7-119">CommonParameters</span></span>
<span data-ttu-id="9e3c7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3c7-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3c7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3c7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-122">INPUTS</span></span>

### <span data-ttu-id="9e3c7-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e3c7-123">PSVirtualNetwork</span></span>
<span data-ttu-id="9e3c7-124">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9e3c7-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="9e3c7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e3c7-125">OUTPUTS</span></span>

### <span data-ttu-id="9e3c7-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e3c7-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9e3c7-127">Note</span><span class="sxs-lookup"><span data-stu-id="9e3c7-127">NOTES</span></span>

## <span data-ttu-id="9e3c7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-128">RELATED LINKS</span></span>

[<span data-ttu-id="9e3c7-129">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e3c7-129">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e3c7-130">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e3c7-130">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e3c7-131">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e3c7-131">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e3c7-132">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e3c7-132">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


