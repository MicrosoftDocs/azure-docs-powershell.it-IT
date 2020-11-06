---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510852"
---
# <span data-ttu-id="a7865-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7865-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a7865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7865-102">SYNOPSIS</span></span>
<span data-ttu-id="a7865-103">Rimuove una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a7865-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7865-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7865-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7865-105">DESCRIPTION</span></span>
<span data-ttu-id="a7865-106">Il cmdlet **Remove-AzureRmLoadBalancerRuleConfig** rimuove una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7865-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a7865-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7865-107">EXAMPLES</span></span>

### <span data-ttu-id="a7865-108">Esempio 1: rimuovere una configurazione di una regola da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a7865-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a7865-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a7865-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a7865-110">Il secondo comando rimuove la configurazione della regola denominata MyLBruleName dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a7865-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a7865-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7865-111">PARAMETERS</span></span>

### <span data-ttu-id="a7865-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7865-112">-DefaultProfile</span></span>
<span data-ttu-id="a7865-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7865-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7865-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7865-114">-LoadBalancer</span></span>
<span data-ttu-id="a7865-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7865-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7865-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7865-116">-Name</span></span>
<span data-ttu-id="a7865-117">Specifica il nome della configurazione della regola di bilanciamento del carico rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7865-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7865-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7865-118">-Confirm</span></span>
<span data-ttu-id="a7865-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7865-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7865-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7865-120">-WhatIf</span></span>
<span data-ttu-id="a7865-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7865-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7865-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7865-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7865-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7865-123">CommonParameters</span></span>
<span data-ttu-id="a7865-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7865-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7865-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7865-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7865-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7865-126">INPUTS</span></span>

### <span data-ttu-id="a7865-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7865-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a7865-128">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7865-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a7865-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7865-129">OUTPUTS</span></span>

### <span data-ttu-id="a7865-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7865-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a7865-131">Note</span><span class="sxs-lookup"><span data-stu-id="a7865-131">NOTES</span></span>

## <span data-ttu-id="a7865-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7865-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7865-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7865-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a7865-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7865-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a7865-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7865-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a7865-136">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7865-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a7865-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7865-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


