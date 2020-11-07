---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 3d3667e73988b50e5c7cab09d07c6ba1a32d072b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855178"
---
# <span data-ttu-id="33a3a-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="33a3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="33a3a-103">Aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33a3a-103">Updates a virtual network.</span></span>

## <span data-ttu-id="33a3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33a3a-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33a3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="33a3a-106">Il cmdlet **set-AzVirtualNetwork** aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33a3a-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="33a3a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="33a3a-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="33a3a-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="33a3a-109">Questo esempio crea una rete virtuale denominata TestResourceGroup con due subnet: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="33a3a-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="33a3a-110">Viene quindi rimossa la subnet backendSubnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33a3a-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="33a3a-111">Il cmdlet Set-AzVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="33a3a-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="33a3a-112">Quando viene eseguito il cmdlet Set-AzVirtualNetwork, il backendSubnet viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="33a3a-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="33a3a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33a3a-113">PARAMETERS</span></span>

### <span data-ttu-id="33a3a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33a3a-114">-AsJob</span></span>
<span data-ttu-id="33a3a-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="33a3a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33a3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a3a-116">-DefaultProfile</span></span>
<span data-ttu-id="33a3a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33a3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a3a-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-118">-VirtualNetwork</span></span>
<span data-ttu-id="33a3a-119">Specifica un oggetto di rete virtuale che rappresenta lo stato in cui deve essere impostata la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33a3a-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="33a3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a3a-120">CommonParameters</span></span>
<span data-ttu-id="33a3a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a3a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a3a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a3a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33a3a-123">INPUTS</span></span>

### <span data-ttu-id="33a3a-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="33a3a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33a3a-125">OUTPUTS</span></span>

### <span data-ttu-id="33a3a-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="33a3a-127">Note</span><span class="sxs-lookup"><span data-stu-id="33a3a-127">NOTES</span></span>

## <span data-ttu-id="33a3a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33a3a-128">RELATED LINKS</span></span>

[<span data-ttu-id="33a3a-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="33a3a-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="33a3a-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="33a3a-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33a3a-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


