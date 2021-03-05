---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964141"
---
# <span data-ttu-id="4cfbb-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4cfbb-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="4cfbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfbb-103">Crea una configurazione IP per un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4cfbb-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="4cfbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cfbb-104">SYNTAX</span></span>

### <span data-ttu-id="4cfbb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cfbb-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cfbb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4cfbb-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cfbb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cfbb-107">DESCRIPTION</span></span>
<span data-ttu-id="4cfbb-108">Il cmdlet **New-AzVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un Gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) in base all'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="4cfbb-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="4cfbb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cfbb-109">EXAMPLES</span></span>

### <span data-ttu-id="4cfbb-110">1: Creare una configurazione IP per un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4cfbb-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="4cfbb-111">Configura un Gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="4cfbb-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="4cfbb-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzVirtualNetworkSubnetConfig** nella "GatewaySubnet" all'interno della rete virtuale che si intende creare un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cfbb-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="4cfbb-113">La variabile $myGWpip viene ottenuta con il cmdlet **New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="4cfbb-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="4cfbb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cfbb-114">PARAMETERS</span></span>

### <span data-ttu-id="4cfbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfbb-115">-DefaultProfile</span></span>
<span data-ttu-id="4cfbb-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cfbb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cfbb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4cfbb-117">-Name</span></span>
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

### <span data-ttu-id="4cfbb-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4cfbb-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="4cfbb-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4cfbb-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="4cfbb-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4cfbb-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="4cfbb-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4cfbb-121">-Subnet</span></span>
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

### <span data-ttu-id="4cfbb-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4cfbb-122">-SubnetId</span></span>
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

### <span data-ttu-id="4cfbb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfbb-123">CommonParameters</span></span>
<span data-ttu-id="4cfbb-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfbb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfbb-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cfbb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfbb-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cfbb-126">INPUTS</span></span>

### <span data-ttu-id="4cfbb-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4cfbb-127">None</span></span>

## <span data-ttu-id="4cfbb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cfbb-128">OUTPUTS</span></span>

### <span data-ttu-id="4cfbb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cfbb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="4cfbb-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cfbb-130">NOTES</span></span>

## <span data-ttu-id="4cfbb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cfbb-131">RELATED LINKS</span></span>

[<span data-ttu-id="4cfbb-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4cfbb-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="4cfbb-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4cfbb-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
