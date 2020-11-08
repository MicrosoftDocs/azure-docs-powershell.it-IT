---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200349"
---
# <span data-ttu-id="1b244-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b244-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1b244-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b244-102">SYNOPSIS</span></span>
<span data-ttu-id="1b244-103">Rimuove una configurazione IP front-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1b244-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="1b244-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b244-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b244-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b244-105">DESCRIPTION</span></span>
<span data-ttu-id="1b244-106">Il cmdlet **Remove-AzLoadBalancerFrontendIpConfig** rimuove una configurazione IP front-end da un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b244-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="1b244-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b244-107">EXAMPLES</span></span>

### <span data-ttu-id="1b244-108">Esempio 1: rimuovere una configurazione IP front-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="1b244-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1b244-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione IP front-end che si vuole rimuovere, quindi lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="1b244-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="1b244-110">Il secondo comando rimuove la configurazione IP di frontend associata dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="1b244-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1b244-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b244-111">PARAMETERS</span></span>

### <span data-ttu-id="1b244-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b244-112">-DefaultProfile</span></span>
<span data-ttu-id="1b244-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b244-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b244-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b244-114">-LoadBalancer</span></span>
<span data-ttu-id="1b244-115">Specifica il bilanciamento del carico che contiene la configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1b244-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="1b244-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b244-116">-Name</span></span>
<span data-ttu-id="1b244-117">Specifica il nome della configurazione dell'indirizzo IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1b244-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="1b244-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b244-118">-Confirm</span></span>
<span data-ttu-id="1b244-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b244-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b244-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b244-120">-WhatIf</span></span>
<span data-ttu-id="1b244-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b244-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b244-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b244-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b244-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b244-123">CommonParameters</span></span>
<span data-ttu-id="1b244-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b244-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b244-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b244-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b244-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b244-126">INPUTS</span></span>

### <span data-ttu-id="1b244-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b244-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b244-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b244-128">OUTPUTS</span></span>

### <span data-ttu-id="1b244-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b244-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b244-130">Note</span><span class="sxs-lookup"><span data-stu-id="1b244-130">NOTES</span></span>

## <span data-ttu-id="1b244-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b244-131">RELATED LINKS</span></span>

[<span data-ttu-id="1b244-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b244-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1b244-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b244-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1b244-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b244-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1b244-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b244-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1b244-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1b244-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


