---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 7c356a3f27959ccb0dd3160b8b984b304eac647d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515079"
---
# <span data-ttu-id="24b65-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="24b65-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="24b65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24b65-102">SYNOPSIS</span></span>
<span data-ttu-id="24b65-103">Elenca le route apprese da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="24b65-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24b65-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24b65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24b65-105">DESCRIPTION</span></span>
<span data-ttu-id="24b65-106">Enumera le route apprese da un gateway di rete virtuale di Azure da varie origini.</span><span class="sxs-lookup"><span data-stu-id="24b65-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="24b65-107">Questo include le route acquisite su BGP, nonché le route statiche.</span><span class="sxs-lookup"><span data-stu-id="24b65-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="24b65-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24b65-108">EXAMPLES</span></span>

### <span data-ttu-id="24b65-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24b65-109">Example 1</span></span>
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

<span data-ttu-id="24b65-110">Per il gateway di rete virtuale di Azure denominato GatewayName nel gruppo di risorse resourceGroup, recupera le route che il gateway di Azure conosce.</span><span class="sxs-lookup"><span data-stu-id="24b65-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="24b65-111">Il gateway di rete virtuale di Azure in questo caso include due route statiche (10.1.0.0/16 e 10.0.0.254/32), oltre a una route learned over BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="24b65-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="24b65-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24b65-112">PARAMETERS</span></span>

### <span data-ttu-id="24b65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24b65-113">-AsJob</span></span>
<span data-ttu-id="24b65-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="24b65-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24b65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b65-115">-DefaultProfile</span></span>
<span data-ttu-id="24b65-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24b65-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24b65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b65-117">-ResourceGroupName</span></span>
<span data-ttu-id="24b65-118">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="24b65-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="24b65-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="24b65-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="24b65-120">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="24b65-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="24b65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b65-121">CommonParameters</span></span>
<span data-ttu-id="24b65-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b65-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b65-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b65-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24b65-124">INPUTS</span></span>

### <span data-ttu-id="24b65-125">System. String</span><span class="sxs-lookup"><span data-stu-id="24b65-125">System.String</span></span>

## <span data-ttu-id="24b65-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24b65-126">OUTPUTS</span></span>

### <span data-ttu-id="24b65-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="24b65-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="24b65-128">Note</span><span class="sxs-lookup"><span data-stu-id="24b65-128">NOTES</span></span>

## <span data-ttu-id="24b65-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24b65-129">RELATED LINKS</span></span>
