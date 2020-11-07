---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860282"
---
# <span data-ttu-id="5cbe0-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe0-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5cbe0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbe0-103">Rimuove una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="5cbe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cbe0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cbe0-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbe0-106">Il cmdlet **Remove-AzLoadBalancerRuleConfig** rimuove una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5cbe0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbe0-108">Esempio 1: rimuovere una configurazione di una regola da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="5cbe0-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="5cbe0-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="5cbe0-110">Il secondo comando rimuove la configurazione della regola denominata MyLBruleName dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="5cbe0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-111">PARAMETERS</span></span>

### <span data-ttu-id="5cbe0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbe0-112">-DefaultProfile</span></span>
<span data-ttu-id="5cbe0-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbe0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe0-114">-LoadBalancer</span></span>
<span data-ttu-id="5cbe0-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5cbe0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cbe0-116">-Name</span></span>
<span data-ttu-id="5cbe0-117">Specifica il nome della configurazione della regola di bilanciamento del carico rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5cbe0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbe0-118">CommonParameters</span></span>
<span data-ttu-id="5cbe0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbe0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbe0-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbe0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbe0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-121">INPUTS</span></span>

### <span data-ttu-id="5cbe0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe0-122">PSLoadBalancer</span></span>
<span data-ttu-id="5cbe0-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5cbe0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5cbe0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cbe0-124">OUTPUTS</span></span>

### <span data-ttu-id="5cbe0-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe0-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5cbe0-126">Note</span><span class="sxs-lookup"><span data-stu-id="5cbe0-126">NOTES</span></span>

## <span data-ttu-id="5cbe0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cbe0-127">RELATED LINKS</span></span>

[<span data-ttu-id="5cbe0-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe0-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5cbe0-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe0-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5cbe0-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe0-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5cbe0-131">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe0-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5cbe0-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe0-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


