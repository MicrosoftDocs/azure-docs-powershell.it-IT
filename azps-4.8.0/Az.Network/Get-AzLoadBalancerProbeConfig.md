---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032385"
---
# <span data-ttu-id="dee00-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dee00-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="dee00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dee00-102">SYNOPSIS</span></span>
<span data-ttu-id="dee00-103">Ottiene una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="dee00-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="dee00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dee00-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dee00-105">DESCRIPTION</span></span>
<span data-ttu-id="dee00-106">Il cmdlet **Get-AzLoadBalancerProbeConfig** ottiene una o più configurazioni di sonde per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="dee00-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="dee00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dee00-107">EXAMPLES</span></span>

### <span data-ttu-id="dee00-108">Esempio 1: ottenere la configurazione Probe di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="dee00-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="dee00-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="dee00-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="dee00-110">Il secondo comando ottiene la configurazione di probe associata denominata Probe dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="dee00-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="dee00-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dee00-111">PARAMETERS</span></span>

### <span data-ttu-id="dee00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee00-112">-DefaultProfile</span></span>
<span data-ttu-id="dee00-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dee00-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee00-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee00-114">-LoadBalancer</span></span>
<span data-ttu-id="dee00-115">Specifica il bilanciamento del carico associato alla configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="dee00-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="dee00-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dee00-116">-Name</span></span>
<span data-ttu-id="dee00-117">Specifica il nome della configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="dee00-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="dee00-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee00-118">CommonParameters</span></span>
<span data-ttu-id="dee00-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee00-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee00-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dee00-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee00-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dee00-121">INPUTS</span></span>

### <span data-ttu-id="dee00-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee00-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dee00-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dee00-123">OUTPUTS</span></span>

### <span data-ttu-id="dee00-124">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="dee00-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="dee00-125">Note</span><span class="sxs-lookup"><span data-stu-id="dee00-125">NOTES</span></span>

## <span data-ttu-id="dee00-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dee00-126">RELATED LINKS</span></span>

[<span data-ttu-id="dee00-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dee00-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dee00-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee00-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dee00-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dee00-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dee00-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dee00-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dee00-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dee00-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


