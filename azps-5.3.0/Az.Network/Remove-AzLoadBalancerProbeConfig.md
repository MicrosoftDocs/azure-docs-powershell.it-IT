---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475861"
---
# <span data-ttu-id="42725-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="42725-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="42725-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42725-102">SYNOPSIS</span></span>
<span data-ttu-id="42725-103">Rimuove la configurazione di una sonda da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="42725-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="42725-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42725-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42725-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42725-105">DESCRIPTION</span></span>
<span data-ttu-id="42725-106">Il cmdlet **Remove-AzLoadBalancerProbeConfig** rimuove una configurazione di probe da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="42725-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="42725-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42725-107">EXAMPLES</span></span>

### <span data-ttu-id="42725-108">Esempio 1: rimuovere una configurazione di una sonda da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="42725-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="42725-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="42725-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="42725-110">Il secondo comando Elimina la configurazione denominata Probe dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="42725-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="42725-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42725-111">PARAMETERS</span></span>

### <span data-ttu-id="42725-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42725-112">-DefaultProfile</span></span>
<span data-ttu-id="42725-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42725-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42725-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42725-114">-LoadBalancer</span></span>
<span data-ttu-id="42725-115">Specifica il bilanciamento del carico che contiene la configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42725-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="42725-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="42725-116">-Name</span></span>
<span data-ttu-id="42725-117">Specifica il nome della configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42725-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="42725-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42725-118">-Confirm</span></span>
<span data-ttu-id="42725-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42725-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42725-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42725-120">-WhatIf</span></span>
<span data-ttu-id="42725-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42725-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42725-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42725-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42725-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42725-123">CommonParameters</span></span>
<span data-ttu-id="42725-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42725-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42725-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42725-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42725-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42725-126">INPUTS</span></span>

### <span data-ttu-id="42725-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42725-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42725-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42725-128">OUTPUTS</span></span>

### <span data-ttu-id="42725-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42725-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42725-130">Note</span><span class="sxs-lookup"><span data-stu-id="42725-130">NOTES</span></span>

## <span data-ttu-id="42725-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42725-131">RELATED LINKS</span></span>

[<span data-ttu-id="42725-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="42725-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="42725-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42725-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="42725-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="42725-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="42725-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="42725-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="42725-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="42725-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


