---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200368"
---
# <span data-ttu-id="b9470-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="b9470-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="b9470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9470-102">SYNOPSIS</span></span>
<span data-ttu-id="b9470-103">Elenca le route apprese da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="b9470-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="b9470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9470-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9470-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9470-105">DESCRIPTION</span></span>
<span data-ttu-id="b9470-106">Enumera le route apprese da un gateway di rete virtuale di Azure da varie origini.</span><span class="sxs-lookup"><span data-stu-id="b9470-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="b9470-107">Questo include le route acquisite su BGP, nonché le route statiche.</span><span class="sxs-lookup"><span data-stu-id="b9470-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="b9470-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9470-108">EXAMPLES</span></span>

### <span data-ttu-id="b9470-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9470-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="b9470-110">Per il gateway di rete virtuale di Azure denominato GatewayName nel gruppo di risorse resourceGroup, recupera le route che il gateway di Azure conosce.</span><span class="sxs-lookup"><span data-stu-id="b9470-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="b9470-111">Il gateway di rete virtuale di Azure in questo caso include due route statiche (10.1.0.0/16 e 10.0.0.254/32), oltre a una route learned over BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="b9470-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="b9470-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9470-112">PARAMETERS</span></span>

### <span data-ttu-id="b9470-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9470-113">-AsJob</span></span>
<span data-ttu-id="b9470-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b9470-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9470-115">-DefaultProfile</span></span>
<span data-ttu-id="b9470-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9470-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9470-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9470-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9470-118">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="b9470-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="b9470-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b9470-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b9470-120">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b9470-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="b9470-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9470-121">CommonParameters</span></span>
<span data-ttu-id="b9470-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9470-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9470-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9470-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9470-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9470-124">INPUTS</span></span>

### <span data-ttu-id="b9470-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b9470-125">System.String</span></span>

## <span data-ttu-id="b9470-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9470-126">OUTPUTS</span></span>

### <span data-ttu-id="b9470-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="b9470-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="b9470-128">Note</span><span class="sxs-lookup"><span data-stu-id="b9470-128">NOTES</span></span>

## <span data-ttu-id="b9470-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9470-129">RELATED LINKS</span></span>
