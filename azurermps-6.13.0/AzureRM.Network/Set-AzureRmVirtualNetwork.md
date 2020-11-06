---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513584"
---
# <span data-ttu-id="ffd11-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="ffd11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffd11-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd11-103">Imposta lo stato obiettivo per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffd11-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffd11-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffd11-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd11-106">Il cmdlet **set-AzureRmVirtualNetwork** imposta lo stato dell'obiettivo per una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd11-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="ffd11-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffd11-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd11-108">1: crea una rete virtuale e rimuove una delle relative subnet</span><span class="sxs-lookup"><span data-stu-id="ffd11-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="ffd11-109">Questo esempio crea una rete virtuale denominata TestResourceGroup con due subnet: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="ffd11-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="ffd11-110">Viene quindi rimossa la subnet backendSubnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffd11-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ffd11-111">Il cmdlet Set-AzureRmVirtualNetwork viene quindi usato per scrivere lo stato di rete virtuale modificata sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="ffd11-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="ffd11-112">Quando viene eseguito il cmdlet Set-AzureRmVirtualNetwork, il backendSubnet viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="ffd11-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="ffd11-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffd11-113">PARAMETERS</span></span>

### <span data-ttu-id="ffd11-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffd11-114">-AsJob</span></span>
<span data-ttu-id="ffd11-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ffd11-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffd11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd11-116">-DefaultProfile</span></span>
<span data-ttu-id="ffd11-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd11-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffd11-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-118">-VirtualNetwork</span></span>
<span data-ttu-id="ffd11-119">Specifica un oggetto **virtualnetwork** che rappresenta lo stato dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="ffd11-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="ffd11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd11-120">CommonParameters</span></span>
<span data-ttu-id="ffd11-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd11-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd11-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd11-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffd11-123">INPUTS</span></span>

### <span data-ttu-id="ffd11-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="ffd11-125">Parametri: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffd11-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="ffd11-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffd11-126">OUTPUTS</span></span>

### <span data-ttu-id="ffd11-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ffd11-128">Note</span><span class="sxs-lookup"><span data-stu-id="ffd11-128">NOTES</span></span>

## <span data-ttu-id="ffd11-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffd11-129">RELATED LINKS</span></span>

[<span data-ttu-id="ffd11-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ffd11-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ffd11-132">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ffd11-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffd11-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


