---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862797"
---
# <span data-ttu-id="5c7ea-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="5c7ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7ea-103">Imposta lo stato obiettivo per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="5c7ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c7ea-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c7ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c7ea-105">DESCRIPTION</span></span>
<span data-ttu-id="5c7ea-106">Il cmdlet **set-AzLoadBalancer** imposta lo stato dell'obiettivo per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="5c7ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c7ea-107">EXAMPLES</span></span>

### <span data-ttu-id="5c7ea-108">Esempio 1: modificare un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="5c7ea-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="5c7ea-109">Il primo comando ottiene il bilanciamento del carico denominato NRPLB e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="5c7ea-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una regola di NAT in ingresso denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="5c7ea-111">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancer** , che aggiorna la configurazione del bilanciamento del carico e la Salva.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="5c7ea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c7ea-112">PARAMETERS</span></span>

### <span data-ttu-id="5c7ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c7ea-113">-AsJob</span></span>
<span data-ttu-id="5c7ea-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5c7ea-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7ea-115">-DefaultProfile</span></span>
<span data-ttu-id="5c7ea-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c7ea-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-117">-LoadBalancer</span></span>
<span data-ttu-id="5c7ea-118">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-118">Specifies a load balancer.</span></span>
<span data-ttu-id="5c7ea-119">Questo cmdlet imposta lo stato obiettivo per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c7ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7ea-120">CommonParameters</span></span>
<span data-ttu-id="5c7ea-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c7ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7ea-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c7ea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7ea-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c7ea-123">INPUTS</span></span>

### <span data-ttu-id="5c7ea-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-124">PSLoadBalancer</span></span>
<span data-ttu-id="5c7ea-125">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5c7ea-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5c7ea-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c7ea-126">OUTPUTS</span></span>

### <span data-ttu-id="5c7ea-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5c7ea-128">Note</span><span class="sxs-lookup"><span data-stu-id="5c7ea-128">NOTES</span></span>

## <span data-ttu-id="5c7ea-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c7ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c7ea-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5c7ea-131">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5c7ea-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c7ea-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


