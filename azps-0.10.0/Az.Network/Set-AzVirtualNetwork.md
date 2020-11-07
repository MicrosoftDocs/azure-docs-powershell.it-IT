---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862718"
---
# <span data-ttu-id="7e8ed-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="7e8ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8ed-103">Imposta lo stato obiettivo per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="7e8ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e8ed-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e8ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="7e8ed-106">Il cmdlet **set-AzVirtualNetwork** imposta lo stato dell'obiettivo per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="7e8ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="7e8ed-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="7e8ed-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="7e8ed-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="7e8ed-110">Viene quindi rimossa una subnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7e8ed-111">Il cmdlet Set-AzVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="7e8ed-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e8ed-112">PARAMETERS</span></span>

### <span data-ttu-id="7e8ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e8ed-113">-AsJob</span></span>
<span data-ttu-id="7e8ed-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e8ed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e8ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8ed-115">-DefaultProfile</span></span>
<span data-ttu-id="7e8ed-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e8ed-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-117">-VirtualNetwork</span></span>
<span data-ttu-id="7e8ed-118">Specifica un oggetto **virtualnetwork** che rappresenta lo stato dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="7e8ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8ed-119">CommonParameters</span></span>
<span data-ttu-id="7e8ed-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8ed-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8ed-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8ed-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e8ed-122">INPUTS</span></span>

### <span data-ttu-id="7e8ed-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-123">PSVirtualNetwork</span></span>
<span data-ttu-id="7e8ed-124">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7e8ed-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="7e8ed-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e8ed-125">OUTPUTS</span></span>

### <span data-ttu-id="7e8ed-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7e8ed-127">Note</span><span class="sxs-lookup"><span data-stu-id="7e8ed-127">NOTES</span></span>

## <span data-ttu-id="7e8ed-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e8ed-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e8ed-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7e8ed-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7e8ed-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7e8ed-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e8ed-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


