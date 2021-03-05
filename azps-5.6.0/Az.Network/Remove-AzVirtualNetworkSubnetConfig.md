---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c820d44ed8c3d32feb3f1d63d2b52a487c27f0dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005966"
---
# <span data-ttu-id="70eaa-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="70eaa-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="70eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="70eaa-103">Rimuove una configurazione subnet da una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="70eaa-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="70eaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70eaa-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70eaa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="70eaa-106">Il cmdlet **Remove-AzVirtualNetworkSubnetConfig** rimuove una subnet da una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="70eaa-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="70eaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="70eaa-108">1: Rimuovere una subnet da una rete virtuale e aggiornare la rete virtuale</span><span class="sxs-lookup"><span data-stu-id="70eaa-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="70eaa-109">Questo esempio crea un gruppo di risorse e una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="70eaa-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="70eaa-110">Usa quindi il comando Remove-AzVirtualNetworkSubnetConfig per rimuovere la subnet back-end dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="70eaa-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="70eaa-111">Set-AzVirtualNetwork viene quindi chiamata per modificare la rete virtuale sul lato server.</span><span class="sxs-lookup"><span data-stu-id="70eaa-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="70eaa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70eaa-112">PARAMETERS</span></span>

### <span data-ttu-id="70eaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70eaa-113">-DefaultProfile</span></span>
<span data-ttu-id="70eaa-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70eaa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70eaa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="70eaa-115">-Name</span></span>
<span data-ttu-id="70eaa-116">Specifica il nome della configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="70eaa-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70eaa-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70eaa-117">-VirtualNetwork</span></span>
<span data-ttu-id="70eaa-118">Specifica **l'oggetto VirtualNetwork** che contiene la configurazione della subnet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="70eaa-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="70eaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70eaa-119">CommonParameters</span></span>
<span data-ttu-id="70eaa-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70eaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70eaa-121">Per altre informazioni, vedere [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70eaa-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70eaa-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="70eaa-122">INPUTS</span></span>

### <span data-ttu-id="70eaa-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70eaa-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="70eaa-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70eaa-124">OUTPUTS</span></span>

### <span data-ttu-id="70eaa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70eaa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="70eaa-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="70eaa-126">NOTES</span></span>

## <span data-ttu-id="70eaa-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70eaa-127">RELATED LINKS</span></span>

[<span data-ttu-id="70eaa-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="70eaa-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="70eaa-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="70eaa-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="70eaa-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="70eaa-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="70eaa-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="70eaa-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


