---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b5d8bbba6416e20ffd29180f8d0a2f211dc88270
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686564"
---
# <span data-ttu-id="abb91-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abb91-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="abb91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abb91-102">SYNOPSIS</span></span>
<span data-ttu-id="abb91-103">Ottiene la configurazione della regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="abb91-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abb91-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abb91-105">DESCRIPTION</span></span>
<span data-ttu-id="abb91-106">Il cmdlet **Get-AzureRmLoadBalancerRuleConfig** ottiene una o più configurazioni di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="abb91-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="abb91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abb91-107">EXAMPLES</span></span>

### <span data-ttu-id="abb91-108">Esempio 1: ottenere la configurazione della regola di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="abb91-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="abb91-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="abb91-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="abb91-110">Il secondo comando ottiene la configurazione di regola associata denominata MyLBrulename dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="abb91-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="abb91-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abb91-111">PARAMETERS</span></span>

### <span data-ttu-id="abb91-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb91-112">-LoadBalancer</span></span>
<span data-ttu-id="abb91-113">Specifica il bilanciamento del carico associato alla configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="abb91-113">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb91-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="abb91-114">-Name</span></span>
<span data-ttu-id="abb91-115">Specifica il nome della configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="abb91-115">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="abb91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb91-116">-DefaultProfile</span></span>
<span data-ttu-id="abb91-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abb91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb91-118">CommonParameters</span></span>
<span data-ttu-id="abb91-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb91-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb91-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb91-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abb91-121">INPUTS</span></span>

### <span data-ttu-id="abb91-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb91-122">PSLoadBalancer</span></span>
<span data-ttu-id="abb91-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="abb91-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="abb91-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abb91-124">OUTPUTS</span></span>

### <span data-ttu-id="abb91-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="abb91-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="abb91-126">Note</span><span class="sxs-lookup"><span data-stu-id="abb91-126">NOTES</span></span>

## <span data-ttu-id="abb91-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abb91-127">RELATED LINKS</span></span>

[<span data-ttu-id="abb91-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abb91-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="abb91-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb91-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="abb91-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abb91-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="abb91-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abb91-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


