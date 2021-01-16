---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357447"
---
# <span data-ttu-id="194d2-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="194d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="194d2-102">SYNOPSIS</span></span>
<span data-ttu-id="194d2-103">Aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="194d2-103">Updates a virtual network.</span></span>

## <span data-ttu-id="194d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="194d2-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="194d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194d2-105">DESCRIPTION</span></span>
<span data-ttu-id="194d2-106">Il cmdlet **set-AzVirtualNetwork** aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="194d2-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="194d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="194d2-107">EXAMPLES</span></span>

### <span data-ttu-id="194d2-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="194d2-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="194d2-109">Questo esempio crea una rete virtuale denominata TestResourceGroup con due subnet: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="194d2-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="194d2-110">Viene quindi rimossa la subnet backendSubnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="194d2-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="194d2-111">Il cmdlet Set-AzVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="194d2-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="194d2-112">Quando viene eseguito il cmdlet Set-AzVirtualNetwork, il backendSubnet viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="194d2-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="194d2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="194d2-113">PARAMETERS</span></span>

### <span data-ttu-id="194d2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="194d2-114">-AsJob</span></span>
<span data-ttu-id="194d2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="194d2-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194d2-116">-DefaultProfile</span></span>
<span data-ttu-id="194d2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="194d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="194d2-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-118">-VirtualNetwork</span></span>
<span data-ttu-id="194d2-119">Specifica un oggetto di rete virtuale che rappresenta lo stato in cui deve essere impostata la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="194d2-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="194d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194d2-120">CommonParameters</span></span>
<span data-ttu-id="194d2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194d2-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="194d2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194d2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="194d2-123">INPUTS</span></span>

### <span data-ttu-id="194d2-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="194d2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="194d2-125">OUTPUTS</span></span>

### <span data-ttu-id="194d2-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="194d2-127">Note</span><span class="sxs-lookup"><span data-stu-id="194d2-127">NOTES</span></span>

## <span data-ttu-id="194d2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="194d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="194d2-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="194d2-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="194d2-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="194d2-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="194d2-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


