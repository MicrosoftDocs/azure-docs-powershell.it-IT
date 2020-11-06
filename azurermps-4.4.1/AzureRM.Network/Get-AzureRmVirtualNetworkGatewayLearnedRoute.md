---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516924"
---
# <span data-ttu-id="8fcfc-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="8fcfc-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="8fcfc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="8fcfc-103">Elenca le route apprese da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="8fcfc-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fcfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fcfc-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fcfc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fcfc-105">DESCRIPTION</span></span>
<span data-ttu-id="8fcfc-106">Enumera le route apprese da un gateway di rete virtuale di Azure da varie origini.</span><span class="sxs-lookup"><span data-stu-id="8fcfc-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="8fcfc-107">Questo include le route acquisite su BGP, nonché le route statiche.</span><span class="sxs-lookup"><span data-stu-id="8fcfc-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="8fcfc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fcfc-108">EXAMPLES</span></span>

### <span data-ttu-id="8fcfc-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8fcfc-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="8fcfc-110">Per il gateway di rete virtuale di Azure denominato GatewayName nel gruppo di risorse resourceGroup, recupera le route che il gateway di Azure conosce.</span><span class="sxs-lookup"><span data-stu-id="8fcfc-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="8fcfc-111">Il gateway di rete virtuale di Azure in questo caso include due route statiche (10.1.0.0/16 e 10.0.0.254/32), oltre a una route learned over BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="8fcfc-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="8fcfc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fcfc-112">PARAMETERS</span></span>

### <span data-ttu-id="8fcfc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fcfc-113">-ResourceGroupName</span></span>
<span data-ttu-id="8fcfc-114">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="8fcfc-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fcfc-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8fcfc-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8fcfc-116">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8fcfc-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fcfc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fcfc-117">-DefaultProfile</span></span>
<span data-ttu-id="8fcfc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fcfc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fcfc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fcfc-119">CommonParameters</span></span>
<span data-ttu-id="8fcfc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fcfc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fcfc-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fcfc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fcfc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fcfc-122">INPUTS</span></span>

### <span data-ttu-id="8fcfc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8fcfc-123">System.String</span></span>

## <span data-ttu-id="8fcfc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fcfc-124">OUTPUTS</span></span>

### <span data-ttu-id="8fcfc-125">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="8fcfc-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="8fcfc-126">Note</span><span class="sxs-lookup"><span data-stu-id="8fcfc-126">NOTES</span></span>

## <span data-ttu-id="8fcfc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fcfc-127">RELATED LINKS</span></span>

