---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: faf242ea76e5985b0b8544e889fdc3240c87afb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510467"
---
# <span data-ttu-id="d3e4d-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d3e4d-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d3e4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e4d-103">Crea una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d3e4d-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3e4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3e4d-104">SYNTAX</span></span>

### <span data-ttu-id="d3e4d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e4d-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3e4d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d3e4d-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3e4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3e4d-107">DESCRIPTION</span></span>
<span data-ttu-id="d3e4d-108">Il cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) basato sull'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="d3e4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3e4d-109">EXAMPLES</span></span>

### <span data-ttu-id="d3e4d-110">1: creare una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d3e4d-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="d3e4d-111">Configura un gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="d3e4d-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** su "GatewaySubnet" all'interno della rete virtuale che si intende creare un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="d3e4d-113">La variabile $myGWpip viene ottenuta usando il cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="d3e4d-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="d3e4d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3e4d-114">PARAMETERS</span></span>

### <span data-ttu-id="d3e4d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3e4d-115">-Name</span></span>
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

### <span data-ttu-id="d3e4d-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3e4d-116">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="d3e4d-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3e4d-117">-PublicIpAddress</span></span>
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

### <span data-ttu-id="d3e4d-118">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d3e4d-118">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="d3e4d-119">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d3e4d-119">-Subnet</span></span>
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

### <span data-ttu-id="d3e4d-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d3e4d-120">-SubnetId</span></span>
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

### <span data-ttu-id="d3e4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e4d-121">-DefaultProfile</span></span>
<span data-ttu-id="d3e4d-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3e4d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e4d-123">CommonParameters</span></span>
<span data-ttu-id="d3e4d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e4d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e4d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e4d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3e4d-126">INPUTS</span></span>

## <span data-ttu-id="d3e4d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3e4d-127">OUTPUTS</span></span>

### <span data-ttu-id="d3e4d-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3e4d-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="d3e4d-129">Note</span><span class="sxs-lookup"><span data-stu-id="d3e4d-129">NOTES</span></span>

## <span data-ttu-id="d3e4d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3e4d-130">RELATED LINKS</span></span>

