---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521573"
---
# <span data-ttu-id="ff061-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="ff061-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff061-102">SYNOPSIS</span></span>
<span data-ttu-id="ff061-103">Imposta lo stato obiettivo per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff061-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff061-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff061-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff061-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff061-105">DESCRIPTION</span></span>
<span data-ttu-id="ff061-106">Il cmdlet **set-AzureRmVirtualNetwork** imposta lo stato dell'obiettivo per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff061-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="ff061-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff061-107">EXAMPLES</span></span>

### <span data-ttu-id="ff061-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="ff061-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="ff061-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="ff061-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="ff061-110">Viene quindi rimossa una subnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff061-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ff061-111">Il cmdlet Set-AzureRmVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="ff061-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="ff061-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff061-112">PARAMETERS</span></span>

### <span data-ttu-id="ff061-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-113">-VirtualNetwork</span></span>
<span data-ttu-id="ff061-114">Specifica un oggetto **virtualnetwork** che rappresenta lo stato dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="ff061-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="ff061-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff061-115">-DefaultProfile</span></span>
<span data-ttu-id="ff061-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff061-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff061-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff061-117">CommonParameters</span></span>
<span data-ttu-id="ff061-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff061-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff061-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff061-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff061-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff061-120">INPUTS</span></span>

### <span data-ttu-id="ff061-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-121">PSVirtualNetwork</span></span>
<span data-ttu-id="ff061-122">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ff061-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ff061-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff061-123">OUTPUTS</span></span>

### <span data-ttu-id="ff061-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ff061-125">Note</span><span class="sxs-lookup"><span data-stu-id="ff061-125">NOTES</span></span>

## <span data-ttu-id="ff061-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff061-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff061-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ff061-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ff061-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ff061-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff061-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


