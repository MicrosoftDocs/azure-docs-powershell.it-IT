---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 8dbc1ad62d11ac6b14897c27b11ebdb7f6fb8cc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960461"
---
# <span data-ttu-id="f9e17-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="f9e17-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="f9e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e17-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e17-103">Elenca le route apprese da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="f9e17-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="f9e17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9e17-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9e17-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9e17-105">DESCRIPTION</span></span>
<span data-ttu-id="f9e17-106">Enumera le route acquisite da un gateway di rete virtuale di Azure da varie origini.</span><span class="sxs-lookup"><span data-stu-id="f9e17-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="f9e17-107">Sono incluse le route acquisite tramite BGP, nonché le route statiche.</span><span class="sxs-lookup"><span data-stu-id="f9e17-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="f9e17-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9e17-108">EXAMPLES</span></span>

### <span data-ttu-id="f9e17-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9e17-109">Example 1</span></span>
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

<span data-ttu-id="f9e17-110">Per il gateway di rete virtuale di Azure denominato nome gateway nel gruppo di risorse ResourceGroup, recupera le route che il gateway di Azure riconosce.</span><span class="sxs-lookup"><span data-stu-id="f9e17-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="f9e17-111">Il gateway di rete virtuale di Azure in questo caso ha due route statiche (10.1.0.0/16 e 10.0.0.254/32) e una route appresa tramite BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="f9e17-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="f9e17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9e17-112">PARAMETERS</span></span>

### <span data-ttu-id="f9e17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9e17-113">-AsJob</span></span>
<span data-ttu-id="f9e17-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f9e17-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9e17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e17-115">-DefaultProfile</span></span>
<span data-ttu-id="f9e17-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9e17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e17-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9e17-118">Nome del gruppo di risorse del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f9e17-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f9e17-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f9e17-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f9e17-120">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f9e17-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f9e17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e17-121">CommonParameters</span></span>
<span data-ttu-id="f9e17-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e17-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9e17-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e17-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9e17-124">INPUTS</span></span>

### <span data-ttu-id="f9e17-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f9e17-125">System.String</span></span>

## <span data-ttu-id="f9e17-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9e17-126">OUTPUTS</span></span>

### <span data-ttu-id="f9e17-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="f9e17-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="f9e17-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9e17-128">NOTES</span></span>

## <span data-ttu-id="f9e17-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9e17-129">RELATED LINKS</span></span>
