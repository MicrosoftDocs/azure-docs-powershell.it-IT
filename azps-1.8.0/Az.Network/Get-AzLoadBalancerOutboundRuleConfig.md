---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678508"
---
# <span data-ttu-id="6b9f8-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b9f8-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="6b9f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9f8-103">Ottiene una configurazione della regola in uscita in un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="6b9f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b9f8-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9f8-106">Il cmdlet **Get-AzLoadBalancerOutboundRuleConfig** ottiene una configurazione della regola in uscita o un elenco di configurazioni di regole in uscita in un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="6b9f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="6b9f8-108">Esempio 1: ottenere una configurazione della regola in uscita in un programma di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6b9f8-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="6b9f8-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6b9f8-110">Il secondo comando ottiene la configurazione della regola in uscita denominata regola associata al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="6b9f8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b9f8-111">PARAMETERS</span></span>

### <span data-ttu-id="6b9f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9f8-112">-DefaultProfile</span></span>
<span data-ttu-id="6b9f8-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9f8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b9f8-114">-LoadBalancer</span></span>
<span data-ttu-id="6b9f8-115">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="6b9f8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b9f8-116">-Name</span></span>
<span data-ttu-id="6b9f8-117">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="6b9f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9f8-118">CommonParameters</span></span>
<span data-ttu-id="6b9f8-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9f8-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b9f8-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9f8-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b9f8-121">INPUTS</span></span>

### <span data-ttu-id="6b9f8-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b9f8-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6b9f8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b9f8-123">OUTPUTS</span></span>

### <span data-ttu-id="6b9f8-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="6b9f8-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="6b9f8-125">Note</span><span class="sxs-lookup"><span data-stu-id="6b9f8-125">NOTES</span></span>

## <span data-ttu-id="6b9f8-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b9f8-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b9f8-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b9f8-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b9f8-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b9f8-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b9f8-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b9f8-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b9f8-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b9f8-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)