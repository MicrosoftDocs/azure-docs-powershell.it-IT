---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517451"
---
# <span data-ttu-id="084a9-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="084a9-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="084a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="084a9-102">SYNOPSIS</span></span>
<span data-ttu-id="084a9-103">Rimuove una configurazione della regola in uscita da un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="084a9-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="084a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="084a9-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084a9-105">DESCRIPTION</span></span>
<span data-ttu-id="084a9-106">Il cmdlet **Remove-AzureRmLoadBalancerOutboundRuleConfig** rimuove una configurazione della regola in uscita da un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="084a9-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="084a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="084a9-107">EXAMPLES</span></span>

### <span data-ttu-id="084a9-108">Esempio 1: eliminare una regola in uscita da un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="084a9-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="084a9-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione della regola in uscita che si vuole rimuovere e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="084a9-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="084a9-110">Il secondo comando rimuove la configurazione della regola in uscita associata dal bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="084a9-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="084a9-111">Il terzo comando Aggiorna il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="084a9-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="084a9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="084a9-112">PARAMETERS</span></span>

### <span data-ttu-id="084a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084a9-113">-DefaultProfile</span></span>
<span data-ttu-id="084a9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="084a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084a9-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="084a9-115">-LoadBalancer</span></span>
<span data-ttu-id="084a9-116">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="084a9-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="084a9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="084a9-117">-Name</span></span>
<span data-ttu-id="084a9-118">Nome della regola in uscita</span><span class="sxs-lookup"><span data-stu-id="084a9-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084a9-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="084a9-119">-Confirm</span></span>
<span data-ttu-id="084a9-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084a9-121">-WhatIf</span></span>
<span data-ttu-id="084a9-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084a9-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084a9-124">CommonParameters</span></span>
<span data-ttu-id="084a9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084a9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084a9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084a9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="084a9-127">INPUTS</span></span>

### <span data-ttu-id="084a9-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="084a9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="084a9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="084a9-129">OUTPUTS</span></span>

### <span data-ttu-id="084a9-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="084a9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="084a9-131">Note</span><span class="sxs-lookup"><span data-stu-id="084a9-131">NOTES</span></span>

## <span data-ttu-id="084a9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="084a9-132">RELATED LINKS</span></span>
