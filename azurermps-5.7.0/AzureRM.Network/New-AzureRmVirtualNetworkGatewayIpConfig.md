---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: eba8cd39c621cd2e7b959e54cf20a26ec3434af0
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688669"
---
# <span data-ttu-id="69f16-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="69f16-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="69f16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69f16-102">SYNOPSIS</span></span>
<span data-ttu-id="69f16-103">Crea una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="69f16-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69f16-104">SYNTAX</span></span>

### <span data-ttu-id="69f16-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69f16-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69f16-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="69f16-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f16-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69f16-107">DESCRIPTION</span></span>
<span data-ttu-id="69f16-108">Il cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** crea una configurazione assegnata a un gateway di rete virtuale con un indirizzo IP pubblico (creato in precedenza) basato sull'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="69f16-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="69f16-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69f16-109">EXAMPLES</span></span>

### <span data-ttu-id="69f16-110">1: creare una configurazione IP per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="69f16-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="69f16-111">Configura un gateway di rete virtuale con un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="69f16-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="69f16-112">La variabile $myGWsubnet viene ottenuta usando il cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** su "GatewaySubnet" all'interno della rete virtuale che si intende creare un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="69f16-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="69f16-113">La variabile $myGWpip viene ottenuta usando il cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="69f16-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="69f16-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69f16-114">PARAMETERS</span></span>

### <span data-ttu-id="69f16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f16-115">-DefaultProfile</span></span>
<span data-ttu-id="69f16-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69f16-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f16-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="69f16-117">-Name</span></span>
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

### <span data-ttu-id="69f16-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="69f16-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="69f16-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="69f16-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="69f16-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="69f16-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="69f16-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="69f16-121">-Subnet</span></span>
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

### <span data-ttu-id="69f16-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="69f16-122">-SubnetId</span></span>
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

### <span data-ttu-id="69f16-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f16-123">CommonParameters</span></span>
<span data-ttu-id="69f16-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f16-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f16-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f16-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f16-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69f16-126">INPUTS</span></span>

### <span data-ttu-id="69f16-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="69f16-127">None</span></span>
<span data-ttu-id="69f16-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="69f16-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69f16-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69f16-129">OUTPUTS</span></span>

### <span data-ttu-id="69f16-130">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="69f16-130">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="69f16-131">Note</span><span class="sxs-lookup"><span data-stu-id="69f16-131">NOTES</span></span>

## <span data-ttu-id="69f16-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69f16-132">RELATED LINKS</span></span>

