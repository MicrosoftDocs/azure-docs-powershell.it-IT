---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188538"
---
# <span data-ttu-id="38eba-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38eba-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="38eba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38eba-102">SYNOPSIS</span></span>
<span data-ttu-id="38eba-103">Ottiene una configurazione IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38eba-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="38eba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38eba-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38eba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38eba-105">DESCRIPTION</span></span>
<span data-ttu-id="38eba-106">Il cmdlet **Get-AzLoadBalancerFrontendIpConfig** ottiene una configurazione IP front-end o un elenco di configurazioni IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38eba-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="38eba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38eba-107">EXAMPLES</span></span>

### <span data-ttu-id="38eba-108">Esempio 1: ottenere una configurazione IP front-end in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="38eba-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="38eba-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="38eba-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="38eba-110">Il secondo comando consente di ottenere la configurazione IP front-end associata a tale bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38eba-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="38eba-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38eba-111">PARAMETERS</span></span>

### <span data-ttu-id="38eba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38eba-112">-DefaultProfile</span></span>
<span data-ttu-id="38eba-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38eba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38eba-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38eba-114">-LoadBalancer</span></span>
<span data-ttu-id="38eba-115">Specifica il bilanciamento del carico associato alla configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="38eba-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="38eba-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="38eba-116">-Name</span></span>
<span data-ttu-id="38eba-117">Specifica il nome del bilanciamento del carico che contiene la configurazione IP front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="38eba-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="38eba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38eba-118">CommonParameters</span></span>
<span data-ttu-id="38eba-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38eba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38eba-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38eba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38eba-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38eba-121">INPUTS</span></span>

### <span data-ttu-id="38eba-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38eba-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="38eba-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38eba-123">OUTPUTS</span></span>

### <span data-ttu-id="38eba-124">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38eba-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="38eba-125">Note</span><span class="sxs-lookup"><span data-stu-id="38eba-125">NOTES</span></span>

## <span data-ttu-id="38eba-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38eba-126">RELATED LINKS</span></span>

[<span data-ttu-id="38eba-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38eba-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38eba-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38eba-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="38eba-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38eba-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38eba-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38eba-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38eba-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38eba-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

