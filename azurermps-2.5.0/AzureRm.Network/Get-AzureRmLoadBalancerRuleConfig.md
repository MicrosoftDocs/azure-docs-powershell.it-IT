---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bd834351322f3141685538ea80a89e689d70c74f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867046"
---
# <span data-ttu-id="33fac-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33fac-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="33fac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33fac-102">SYNOPSIS</span></span>
<span data-ttu-id="33fac-103">Ottiene la configurazione della regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="33fac-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33fac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33fac-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33fac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33fac-105">DESCRIPTION</span></span>
<span data-ttu-id="33fac-106">Il cmdlet **Get-AzureRmLoadBalancerRuleConfig** ottiene una o più configurazioni di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="33fac-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="33fac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33fac-107">EXAMPLES</span></span>

### <span data-ttu-id="33fac-108">Esempio 1: ottenere la configurazione della regola di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="33fac-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="33fac-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="33fac-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="33fac-110">Il secondo comando ottiene la configurazione di regola associata denominata MyLBrulename dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="33fac-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="33fac-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33fac-111">PARAMETERS</span></span>

### <span data-ttu-id="33fac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fac-112">-DefaultProfile</span></span>
<span data-ttu-id="33fac-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33fac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33fac-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33fac-114">-LoadBalancer</span></span>
<span data-ttu-id="33fac-115">Specifica il bilanciamento del carico associato alla configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="33fac-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="33fac-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="33fac-116">-Name</span></span>
<span data-ttu-id="33fac-117">Specifica il nome della configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="33fac-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="33fac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fac-118">CommonParameters</span></span>
<span data-ttu-id="33fac-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33fac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fac-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fac-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fac-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33fac-121">INPUTS</span></span>

### <span data-ttu-id="33fac-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33fac-122">PSLoadBalancer</span></span>
<span data-ttu-id="33fac-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="33fac-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="33fac-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33fac-124">OUTPUTS</span></span>

### <span data-ttu-id="33fac-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="33fac-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="33fac-126">Note</span><span class="sxs-lookup"><span data-stu-id="33fac-126">NOTES</span></span>

## <span data-ttu-id="33fac-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33fac-127">RELATED LINKS</span></span>

[<span data-ttu-id="33fac-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33fac-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="33fac-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33fac-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="33fac-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33fac-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="33fac-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33fac-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


