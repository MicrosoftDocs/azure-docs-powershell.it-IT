---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189478"
---
# <span data-ttu-id="858c3-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="858c3-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="858c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858c3-102">SYNOPSIS</span></span>
<span data-ttu-id="858c3-103">Aggiorna una configurazione di configurazione per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="858c3-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="858c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="858c3-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858c3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="858c3-105">DESCRIPTION</span></span>
<span data-ttu-id="858c3-106">Il cmdlet **Set-AzLoadBalancerProbeConfig** aggiorna una configurazione di configurazione per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="858c3-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="858c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="858c3-107">EXAMPLES</span></span>

### <span data-ttu-id="858c3-108">Esempio 1: Modificare la configurazione di un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="858c3-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="858c3-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e quindi lo archivia nella $slb variabile.</span><span class="sxs-lookup"><span data-stu-id="858c3-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="858c3-110">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb ad Add-AzLoadBalancerProbeConfig, che aggiunge una nuova configurazione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="858c3-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="858c3-111">Il terzo comando passa la bilanciamento del carico **a Set-AzLoadBalancerProbeConfig,** che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="858c3-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="858c3-112">È necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="858c3-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="858c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858c3-113">PARAMETERS</span></span>

### <span data-ttu-id="858c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858c3-114">-DefaultProfile</span></span>
<span data-ttu-id="858c3-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="858c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858c3-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="858c3-116">-IntervalInSeconds</span></span>
<span data-ttu-id="858c3-117">Specifica l'intervallo, in secondi, tra le due istanze del servizio con carico bilanciato.</span><span class="sxs-lookup"><span data-stu-id="858c3-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="858c3-118">-LoadBalancer</span></span>
<span data-ttu-id="858c3-119">Specifica una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="858c3-119">Specifies a load balancer.</span></span>
<span data-ttu-id="858c3-120">Questo cmdlet aggiorna una configurazione di configurazione per la bilanciamento del carico specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="858c3-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="858c3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="858c3-121">-Name</span></span>
<span data-ttu-id="858c3-122">Specifica il nome della configurazione di configurazione configurazione impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="858c3-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="858c3-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="858c3-123">-Port</span></span>
<span data-ttu-id="858c3-124">Specifica la porta in cui le applicazioni devono connettersi a un servizio con carico bilanciato.</span><span class="sxs-lookup"><span data-stu-id="858c3-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-125">-Count</span><span class="sxs-lookup"><span data-stu-id="858c3-125">-ProbeCount</span></span>
<span data-ttu-id="858c3-126">Specifica il numero di errori consecutivi per istanza perché un'istanza sia considerata non integra.</span><span class="sxs-lookup"><span data-stu-id="858c3-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="858c3-127">-Protocol</span></span>
<span data-ttu-id="858c3-128">Specifica il protocollo da usare per la probabilità.</span><span class="sxs-lookup"><span data-stu-id="858c3-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="858c3-129">I valori accettabili per questo parametro sono: Tcp o Http.</span><span class="sxs-lookup"><span data-stu-id="858c3-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="858c3-130">-RequestPath</span></span>
<span data-ttu-id="858c3-131">Specifica il percorso nel servizio con carico bilanciato per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="858c3-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="858c3-132">-Confirm</span></span>
<span data-ttu-id="858c3-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="858c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858c3-134">-WhatIf</span></span>
<span data-ttu-id="858c3-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="858c3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="858c3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="858c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858c3-137">CommonParameters</span></span>
<span data-ttu-id="858c3-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858c3-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858c3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858c3-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="858c3-140">INPUTS</span></span>

### <span data-ttu-id="858c3-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="858c3-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="858c3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="858c3-142">System.String</span></span>

### <span data-ttu-id="858c3-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="858c3-143">System.Int32</span></span>

## <span data-ttu-id="858c3-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="858c3-144">OUTPUTS</span></span>

### <span data-ttu-id="858c3-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="858c3-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="858c3-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="858c3-146">NOTES</span></span>

## <span data-ttu-id="858c3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="858c3-147">RELATED LINKS</span></span>

[<span data-ttu-id="858c3-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="858c3-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="858c3-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="858c3-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="858c3-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="858c3-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="858c3-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="858c3-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="858c3-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="858c3-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


