---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860762"
---
# <span data-ttu-id="bc66a-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc66a-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="bc66a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc66a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc66a-103">Ottiene la configurazione della regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bc66a-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="bc66a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc66a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc66a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc66a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc66a-106">Il cmdlet **Get-AzLoadBalancerRuleConfig** ottiene una o più configurazioni di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bc66a-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="bc66a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc66a-107">EXAMPLES</span></span>

### <span data-ttu-id="bc66a-108">Esempio 1: ottenere la configurazione della regola di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="bc66a-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="bc66a-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="bc66a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="bc66a-110">Il secondo comando ottiene la configurazione di regola associata denominata MyLBrulename dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="bc66a-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="bc66a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc66a-111">PARAMETERS</span></span>

### <span data-ttu-id="bc66a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc66a-112">-DefaultProfile</span></span>
<span data-ttu-id="bc66a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc66a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc66a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bc66a-114">-LoadBalancer</span></span>
<span data-ttu-id="bc66a-115">Specifica il bilanciamento del carico associato alla configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc66a-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc66a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc66a-116">-Name</span></span>
<span data-ttu-id="bc66a-117">Specifica il nome della configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc66a-117">Specifies the name of the rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc66a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc66a-118">CommonParameters</span></span>
<span data-ttu-id="bc66a-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc66a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc66a-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc66a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc66a-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc66a-121">INPUTS</span></span>

### <span data-ttu-id="bc66a-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bc66a-122">PSLoadBalancer</span></span>
<span data-ttu-id="bc66a-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bc66a-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bc66a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc66a-124">OUTPUTS</span></span>

### <span data-ttu-id="bc66a-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="bc66a-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="bc66a-126">Note</span><span class="sxs-lookup"><span data-stu-id="bc66a-126">NOTES</span></span>

## <span data-ttu-id="bc66a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc66a-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc66a-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc66a-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc66a-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bc66a-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="bc66a-130">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc66a-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc66a-131">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc66a-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


