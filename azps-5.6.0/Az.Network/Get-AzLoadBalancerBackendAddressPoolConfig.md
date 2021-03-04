---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a337446238807f3a6408d0c9b68034e4a245eb48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956813"
---
# <span data-ttu-id="4ca0c-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ca0c-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4ca0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ca0c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca0c-103">Ottiene una configurazione del pool di indirizzi back-end per un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4ca0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ca0c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca0c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ca0c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca0c-106">Il cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** ottiene un singolo pool di indirizzi back-end o un elenco di pool di indirizzi back-end in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="4ca0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ca0c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca0c-108">Esempio 1: Ottenere il pool di indirizzi back-end</span><span class="sxs-lookup"><span data-stu-id="4ca0c-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4ca0c-109">Il primo comando ottiene una bilanciamento del carico esistente denominata MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup e quindi la archivia nella $loadbalancer variabile.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="4ca0c-110">Il secondo comando ottiene la configurazione del pool di indirizzi back-end associata denominata BackendAddressPool02 per la bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4ca0c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ca0c-111">PARAMETERS</span></span>

### <span data-ttu-id="4ca0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca0c-112">-DefaultProfile</span></span>
<span data-ttu-id="4ca0c-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca0c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ca0c-114">-LoadBalancer</span></span>
<span data-ttu-id="4ca0c-115">Specifica la bilanciamento del carico associata al pool di indirizzi back-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="4ca0c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4ca0c-116">-Name</span></span>
<span data-ttu-id="4ca0c-117">Specifica il nome della bilanciamento del carico che contiene il pool di indirizzi back-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="4ca0c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca0c-118">CommonParameters</span></span>
<span data-ttu-id="4ca0c-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca0c-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ca0c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca0c-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ca0c-121">INPUTS</span></span>

### <span data-ttu-id="4ca0c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ca0c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ca0c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ca0c-123">OUTPUTS</span></span>

### <span data-ttu-id="4ca0c-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ca0c-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="4ca0c-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ca0c-125">NOTES</span></span>

## <span data-ttu-id="4ca0c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ca0c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ca0c-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ca0c-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4ca0c-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ca0c-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4ca0c-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ca0c-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4ca0c-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ca0c-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


