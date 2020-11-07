---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b00c3950140c0ebf158170a8ddd2396e62c2b2c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686608"
---
# <span data-ttu-id="47a9f-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="47a9f-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="47a9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="47a9f-103">Crea una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="47a9f-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47a9f-104">SYNTAX</span></span>

### <span data-ttu-id="47a9f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47a9f-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a9f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47a9f-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a9f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47a9f-107">DESCRIPTION</span></span>
<span data-ttu-id="47a9f-108">Il cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) basato sull'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="47a9f-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="47a9f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47a9f-109">EXAMPLES</span></span>

### <span data-ttu-id="47a9f-110">1: creare una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="47a9f-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="47a9f-111">Configura un gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47a9f-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="47a9f-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** su "GatewaySubnet" all'interno della rete virtuale che si intende creare un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="47a9f-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="47a9f-113">La variabile $myGWpip viene ottenuta usando il cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="47a9f-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="47a9f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47a9f-114">PARAMETERS</span></span>

### <span data-ttu-id="47a9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a9f-115">-DefaultProfile</span></span>
<span data-ttu-id="47a9f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47a9f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a9f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="47a9f-117">-Name</span></span>
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

### <span data-ttu-id="47a9f-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="47a9f-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="47a9f-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="47a9f-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="47a9f-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="47a9f-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="47a9f-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="47a9f-121">-Subnet</span></span>
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

### <span data-ttu-id="47a9f-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="47a9f-122">-SubnetId</span></span>
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

### <span data-ttu-id="47a9f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a9f-123">CommonParameters</span></span>
<span data-ttu-id="47a9f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a9f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a9f-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a9f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a9f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47a9f-126">INPUTS</span></span>

### <span data-ttu-id="47a9f-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47a9f-127">None</span></span>

## <span data-ttu-id="47a9f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47a9f-128">OUTPUTS</span></span>

### <span data-ttu-id="47a9f-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="47a9f-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="47a9f-130">Note</span><span class="sxs-lookup"><span data-stu-id="47a9f-130">NOTES</span></span>

## <span data-ttu-id="47a9f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47a9f-131">RELATED LINKS</span></span>
