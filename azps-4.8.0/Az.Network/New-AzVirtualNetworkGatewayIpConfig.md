---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188460"
---
# <span data-ttu-id="752c4-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="752c4-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="752c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="752c4-102">SYNOPSIS</span></span>
<span data-ttu-id="752c4-103">Crea una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="752c4-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="752c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="752c4-104">SYNTAX</span></span>

### <span data-ttu-id="752c4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="752c4-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="752c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="752c4-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="752c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="752c4-107">DESCRIPTION</span></span>
<span data-ttu-id="752c4-108">Il cmdlet **New-AzVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) basato sull'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="752c4-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="752c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="752c4-109">EXAMPLES</span></span>

### <span data-ttu-id="752c4-110">1: creare una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="752c4-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="752c4-111">Configura un gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="752c4-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="752c4-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzVirtualNetworkSubnetConfig** su "GatewaySubnet" all'interno della rete virtuale che si intende creare un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="752c4-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="752c4-113">La variabile $myGWpip viene ottenuta usando il cmdlet **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="752c4-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="752c4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="752c4-114">PARAMETERS</span></span>

### <span data-ttu-id="752c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752c4-115">-DefaultProfile</span></span>
<span data-ttu-id="752c4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="752c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752c4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="752c4-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c4-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="752c4-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="752c4-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="752c4-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c4-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="752c4-120">-PublicIpAddressId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c4-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="752c4-121">-Subnet</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c4-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="752c4-122">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752c4-123">CommonParameters</span></span>
<span data-ttu-id="752c4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752c4-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752c4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752c4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="752c4-126">INPUTS</span></span>

### <span data-ttu-id="752c4-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="752c4-127">None</span></span>

## <span data-ttu-id="752c4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="752c4-128">OUTPUTS</span></span>

### <span data-ttu-id="752c4-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="752c4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="752c4-130">Note</span><span class="sxs-lookup"><span data-stu-id="752c4-130">NOTES</span></span>

## <span data-ttu-id="752c4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="752c4-131">RELATED LINKS</span></span>

[<span data-ttu-id="752c4-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="752c4-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="752c4-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="752c4-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)