---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032297"
---
# <span data-ttu-id="2d7f5-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f5-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2d7f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7f5-103">Aggiorna una configurazione di probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="2d7f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d7f5-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d7f5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7f5-106">Il cmdlet **set-AzLoadBalancerProbeConfig** aggiorna una configurazione di probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="2d7f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d7f5-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7f5-108">Esempio 1: modificare la configurazione del probe in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="2d7f5-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="2d7f5-109">Il primo comando ottiene il LoadBalancer denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2d7f5-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerProbeConfig, che aggiunge una nuova configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="2d7f5-111">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerProbeConfig** , che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="2d7f5-112">Tieni presente che è necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="2d7f5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d7f5-113">PARAMETERS</span></span>

### <span data-ttu-id="2d7f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7f5-114">-DefaultProfile</span></span>
<span data-ttu-id="2d7f5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d7f5-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2d7f5-116">-IntervalInSeconds</span></span>
<span data-ttu-id="2d7f5-117">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="2d7f5-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d7f5-118">-LoadBalancer</span></span>
<span data-ttu-id="2d7f5-119">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-119">Specifies a load balancer.</span></span>
<span data-ttu-id="2d7f5-120">Questo cmdlet aggiorna una configurazione di probe per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d7f5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d7f5-121">-Name</span></span>
<span data-ttu-id="2d7f5-122">Specifica il nome della configurazione Probe impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2d7f5-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="2d7f5-123">-Port</span></span>
<span data-ttu-id="2d7f5-124">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="2d7f5-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="2d7f5-125">-ProbeCount</span></span>
<span data-ttu-id="2d7f5-126">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="2d7f5-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="2d7f5-127">-Protocol</span></span>
<span data-ttu-id="2d7f5-128">Specifica il protocollo da usare per il sondaggio.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="2d7f5-129">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="2d7f5-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="2d7f5-130">-RequestPath</span></span>
<span data-ttu-id="2d7f5-131">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="2d7f5-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d7f5-132">-Confirm</span></span>
<span data-ttu-id="2d7f5-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7f5-134">-WhatIf</span></span>
<span data-ttu-id="2d7f5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d7f5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7f5-137">CommonParameters</span></span>
<span data-ttu-id="2d7f5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7f5-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7f5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7f5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d7f5-140">INPUTS</span></span>

### <span data-ttu-id="2d7f5-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d7f5-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2d7f5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7f5-142">System.String</span></span>

### <span data-ttu-id="2d7f5-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2d7f5-143">System.Int32</span></span>

## <span data-ttu-id="2d7f5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d7f5-144">OUTPUTS</span></span>

### <span data-ttu-id="2d7f5-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d7f5-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2d7f5-146">Note</span><span class="sxs-lookup"><span data-stu-id="2d7f5-146">NOTES</span></span>

## <span data-ttu-id="2d7f5-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d7f5-147">RELATED LINKS</span></span>

[<span data-ttu-id="2d7f5-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f5-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2d7f5-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d7f5-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2d7f5-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f5-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2d7f5-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f5-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2d7f5-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f5-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


