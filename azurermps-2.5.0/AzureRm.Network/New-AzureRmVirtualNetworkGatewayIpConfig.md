---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867013"
---
# <span data-ttu-id="bbab5-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbab5-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="bbab5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbab5-102">SYNOPSIS</span></span>
<span data-ttu-id="bbab5-103">Crea una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bbab5-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbab5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbab5-104">SYNTAX</span></span>

### <span data-ttu-id="bbab5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbab5-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbab5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bbab5-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbab5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbab5-107">DESCRIPTION</span></span>
<span data-ttu-id="bbab5-108">Il cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) basato sull'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="bbab5-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="bbab5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbab5-109">EXAMPLES</span></span>

### <span data-ttu-id="bbab5-110">1: creare una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bbab5-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="bbab5-111">Configura un gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="bbab5-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="bbab5-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** su "GatewaySubnet" all'interno della rete virtuale che si intende creare un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bbab5-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="bbab5-113">La variabile $myGWpip viene ottenuta usando il cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="bbab5-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="bbab5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbab5-114">PARAMETERS</span></span>

### <span data-ttu-id="bbab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbab5-115">-DefaultProfile</span></span>
<span data-ttu-id="bbab5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbab5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbab5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbab5-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbab5-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbab5-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bbab5-120">-PublicIpAddressId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bbab5-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bbab5-122">-SubnetId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbab5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbab5-123">CommonParameters</span></span>
<span data-ttu-id="bbab5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbab5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbab5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbab5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbab5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbab5-126">INPUTS</span></span>

## <span data-ttu-id="bbab5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbab5-127">OUTPUTS</span></span>

### <span data-ttu-id="bbab5-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbab5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="bbab5-129">Note</span><span class="sxs-lookup"><span data-stu-id="bbab5-129">NOTES</span></span>

## <span data-ttu-id="bbab5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbab5-130">RELATED LINKS</span></span>

