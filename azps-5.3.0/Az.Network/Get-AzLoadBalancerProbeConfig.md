---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380082"
---
# <span data-ttu-id="e3a7f-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3a7f-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e3a7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a7f-103">Ottiene una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e3a7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a7f-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a7f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a7f-106">Il cmdlet **Get-AzLoadBalancerProbeConfig** ottiene una o più configurazioni di sonde per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="e3a7f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a7f-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a7f-108">Esempio 1: ottenere la configurazione Probe di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e3a7f-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="e3a7f-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e3a7f-110">Il secondo comando ottiene la configurazione di probe associata denominata Probe dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="e3a7f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3a7f-111">PARAMETERS</span></span>

### <span data-ttu-id="e3a7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a7f-112">-DefaultProfile</span></span>
<span data-ttu-id="e3a7f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a7f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3a7f-114">-LoadBalancer</span></span>
<span data-ttu-id="e3a7f-115">Specifica il bilanciamento del carico associato alla configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="e3a7f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3a7f-116">-Name</span></span>
<span data-ttu-id="e3a7f-117">Specifica il nome della configurazione della sonda da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="e3a7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a7f-118">CommonParameters</span></span>
<span data-ttu-id="e3a7f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a7f-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3a7f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a7f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3a7f-121">INPUTS</span></span>

### <span data-ttu-id="e3a7f-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3a7f-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e3a7f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a7f-123">OUTPUTS</span></span>

### <span data-ttu-id="e3a7f-124">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="e3a7f-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="e3a7f-125">Note</span><span class="sxs-lookup"><span data-stu-id="e3a7f-125">NOTES</span></span>

## <span data-ttu-id="e3a7f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a7f-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3a7f-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3a7f-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3a7f-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3a7f-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e3a7f-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3a7f-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3a7f-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3a7f-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3a7f-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3a7f-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


