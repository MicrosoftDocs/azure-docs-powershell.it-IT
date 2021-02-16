---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179878"
---
# <span data-ttu-id="b9b09-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9b09-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b9b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9b09-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b09-103">Ottiene una configurazione IP front-end in un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b9b09-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="b9b09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9b09-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9b09-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9b09-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b09-106">Il cmdlet **Get-AzLoadBalancerFrontendIpConfig** ottiene una configurazione IP front-end o un elenco di configurazioni IP front-end in una soluzione di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b9b09-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="b9b09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9b09-107">EXAMPLES</span></span>

### <span data-ttu-id="b9b09-108">Esempio 1: Ottenere una configurazione IP front-end in un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="b9b09-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="b9b09-109">Il primo comando ottiene la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="b9b09-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b9b09-110">Il secondo comando ottiene la configurazione IP front-end associata a questa bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b9b09-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="b9b09-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9b09-111">PARAMETERS</span></span>

### <span data-ttu-id="b9b09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b09-112">-DefaultProfile</span></span>
<span data-ttu-id="b9b09-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b09-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9b09-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9b09-114">-LoadBalancer</span></span>
<span data-ttu-id="b9b09-115">Specifica la bilanciamento del carico associata alla configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b9b09-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b09-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b9b09-116">-Name</span></span>
<span data-ttu-id="b9b09-117">Specifica il nome della bilanciamento del carico che contiene la configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b9b09-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="b9b09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b09-118">CommonParameters</span></span>
<span data-ttu-id="b9b09-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b09-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9b09-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b09-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9b09-121">INPUTS</span></span>

### <span data-ttu-id="b9b09-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9b09-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b9b09-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9b09-123">OUTPUTS</span></span>

### <span data-ttu-id="b9b09-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9b09-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b9b09-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9b09-125">NOTES</span></span>

## <span data-ttu-id="b9b09-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9b09-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9b09-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9b09-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b9b09-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9b09-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b9b09-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9b09-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b9b09-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9b09-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b9b09-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9b09-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


