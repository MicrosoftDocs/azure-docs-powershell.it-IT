---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 40f84388caed0d332c36ee398e842ae00f2f353f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866032"
---
# <span data-ttu-id="59129-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="59129-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59129-102">SYNOPSIS</span></span>
<span data-ttu-id="59129-103">Imposta lo stato obiettivo per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59129-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59129-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59129-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59129-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59129-105">DESCRIPTION</span></span>
<span data-ttu-id="59129-106">Il cmdlet **set-AzureRmVirtualNetwork** imposta lo stato dell'obiettivo per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="59129-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="59129-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59129-107">EXAMPLES</span></span>

### <span data-ttu-id="59129-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="59129-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="59129-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="59129-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="59129-110">Viene quindi rimossa una subnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59129-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="59129-111">Il cmdlet Set-AzureRmVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="59129-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="59129-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59129-112">PARAMETERS</span></span>

### <span data-ttu-id="59129-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59129-113">-AsJob</span></span>
<span data-ttu-id="59129-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="59129-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59129-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59129-115">-DefaultProfile</span></span>
<span data-ttu-id="59129-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59129-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59129-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-117">-VirtualNetwork</span></span>
<span data-ttu-id="59129-118">Specifica un oggetto **virtualnetwork** che rappresenta lo stato dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="59129-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="59129-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59129-119">CommonParameters</span></span>
<span data-ttu-id="59129-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59129-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59129-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59129-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59129-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59129-122">INPUTS</span></span>

### <span data-ttu-id="59129-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-123">PSVirtualNetwork</span></span>
<span data-ttu-id="59129-124">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="59129-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="59129-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59129-125">OUTPUTS</span></span>

### <span data-ttu-id="59129-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="59129-127">Note</span><span class="sxs-lookup"><span data-stu-id="59129-127">NOTES</span></span>

## <span data-ttu-id="59129-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59129-128">RELATED LINKS</span></span>

[<span data-ttu-id="59129-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="59129-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="59129-131">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="59129-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59129-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


