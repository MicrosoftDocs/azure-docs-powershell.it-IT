---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512511"
---
# <span data-ttu-id="aea9b-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="aea9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aea9b-102">SYNOPSIS</span></span>
<span data-ttu-id="aea9b-103">Imposta lo stato obiettivo per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="aea9b-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aea9b-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aea9b-105">DESCRIPTION</span></span>
<span data-ttu-id="aea9b-106">Il cmdlet **set-AzureRmLoadBalancer** imposta lo stato dell'obiettivo per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea9b-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="aea9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aea9b-107">EXAMPLES</span></span>

### <span data-ttu-id="aea9b-108">Esempio 1: modificare un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="aea9b-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="aea9b-109">Il primo comando ottiene il bilanciamento del carico denominato NRPLB e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="aea9b-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="aea9b-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzureRmLoadBalancerInboundNatRuleConfig, che aggiunge una regola di NAT in ingresso denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="aea9b-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="aea9b-111">Il terzo comando passa il bilanciamento del carico a **set-AzureRmLoadBalancer** , che aggiorna la configurazione del bilanciamento del carico e la Salva.</span><span class="sxs-lookup"><span data-stu-id="aea9b-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="aea9b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aea9b-112">PARAMETERS</span></span>

### <span data-ttu-id="aea9b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aea9b-113">-AsJob</span></span>
<span data-ttu-id="aea9b-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="aea9b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aea9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea9b-115">-DefaultProfile</span></span>
<span data-ttu-id="aea9b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aea9b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea9b-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-117">-LoadBalancer</span></span>
<span data-ttu-id="aea9b-118">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="aea9b-118">Specifies a load balancer.</span></span>
<span data-ttu-id="aea9b-119">Questo cmdlet imposta lo stato obiettivo per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="aea9b-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="aea9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea9b-120">CommonParameters</span></span>
<span data-ttu-id="aea9b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea9b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea9b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea9b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aea9b-123">INPUTS</span></span>

### <span data-ttu-id="aea9b-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-124">PSLoadBalancer</span></span>
<span data-ttu-id="aea9b-125">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="aea9b-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="aea9b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aea9b-126">OUTPUTS</span></span>

### <span data-ttu-id="aea9b-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aea9b-128">Note</span><span class="sxs-lookup"><span data-stu-id="aea9b-128">NOTES</span></span>

## <span data-ttu-id="aea9b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aea9b-129">RELATED LINKS</span></span>

[<span data-ttu-id="aea9b-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="aea9b-131">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="aea9b-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aea9b-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


