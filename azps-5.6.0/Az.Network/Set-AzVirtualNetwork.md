---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 1c5a5bc119c481c47c865ca72896b832f3a82b2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997666"
---
# <span data-ttu-id="b6a79-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="b6a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a79-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a79-103">Aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6a79-103">Updates a virtual network.</span></span>

## <span data-ttu-id="b6a79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6a79-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a79-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6a79-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a79-106">Il cmdlet **Set-AzVirtualNetwork** aggiorna una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6a79-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="b6a79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6a79-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a79-108">1: crea una rete virtuale e rimuove una delle sue subnet</span><span class="sxs-lookup"><span data-stu-id="b6a79-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="b6a79-109">Questo esempio crea una rete virtuale denominata TestResourceGroup con due subnet: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="b6a79-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="b6a79-110">Rimuove quindi la subnet BackendSubnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6a79-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b6a79-111">Il Set-AzVirtualNetwork cmdlet di configurazione viene quindi usato per scrivere lo stato modificato della rete virtuale sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="b6a79-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="b6a79-112">Quando il cmdlet Set-AzVirtualNetwork viene eseguito, il backendSubnet viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="b6a79-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="b6a79-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6a79-113">PARAMETERS</span></span>

### <span data-ttu-id="b6a79-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6a79-114">-AsJob</span></span>
<span data-ttu-id="b6a79-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b6a79-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6a79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a79-116">-DefaultProfile</span></span>
<span data-ttu-id="b6a79-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a79-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a79-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-118">-VirtualNetwork</span></span>
<span data-ttu-id="b6a79-119">Specifica un oggetto rete virtuale che rappresenta lo stato su cui deve essere impostata la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6a79-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="b6a79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a79-120">CommonParameters</span></span>
<span data-ttu-id="b6a79-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a79-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a79-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a79-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6a79-123">INPUTS</span></span>

### <span data-ttu-id="b6a79-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b6a79-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6a79-125">OUTPUTS</span></span>

### <span data-ttu-id="b6a79-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b6a79-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6a79-127">NOTES</span></span>

## <span data-ttu-id="b6a79-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6a79-128">RELATED LINKS</span></span>

[<span data-ttu-id="b6a79-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b6a79-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b6a79-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="b6a79-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6a79-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


