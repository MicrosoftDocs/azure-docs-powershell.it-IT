---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 475a85353e4731a1bdb8f95a88328ffa27f99cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677960"
---
# <span data-ttu-id="051b1-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="051b1-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="051b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="051b1-102">SYNOPSIS</span></span>
<span data-ttu-id="051b1-103">Aggiorna una configurazione di probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="051b1-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="051b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="051b1-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="051b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="051b1-105">DESCRIPTION</span></span>
<span data-ttu-id="051b1-106">Il cmdlet **set-AzLoadBalancerProbeConfig** aggiorna una configurazione di probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="051b1-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="051b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="051b1-107">EXAMPLES</span></span>

### <span data-ttu-id="051b1-108">Esempio 1: modificare la configurazione del probe in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="051b1-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="051b1-109">Il primo comando ottiene il LoadBalancer denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="051b1-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="051b1-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerProbeConfig, che aggiunge una nuova configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="051b1-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="051b1-111">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerProbeConfig** , che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="051b1-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="051b1-112">Tieni presente che è necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="051b1-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="051b1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="051b1-113">PARAMETERS</span></span>

### <span data-ttu-id="051b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051b1-114">-DefaultProfile</span></span>
<span data-ttu-id="051b1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="051b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="051b1-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="051b1-116">-IntervalInSeconds</span></span>
<span data-ttu-id="051b1-117">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="051b1-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="051b1-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="051b1-118">-LoadBalancer</span></span>
<span data-ttu-id="051b1-119">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="051b1-119">Specifies a load balancer.</span></span>
<span data-ttu-id="051b1-120">Questo cmdlet aggiorna una configurazione di probe per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="051b1-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="051b1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="051b1-121">-Name</span></span>
<span data-ttu-id="051b1-122">Specifica il nome della configurazione Probe impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="051b1-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="051b1-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="051b1-123">-Port</span></span>
<span data-ttu-id="051b1-124">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="051b1-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="051b1-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="051b1-125">-ProbeCount</span></span>
<span data-ttu-id="051b1-126">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="051b1-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="051b1-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="051b1-127">-Protocol</span></span>
<span data-ttu-id="051b1-128">Specifica il protocollo da usare per il sondaggio.</span><span class="sxs-lookup"><span data-stu-id="051b1-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="051b1-129">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="051b1-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="051b1-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="051b1-130">-RequestPath</span></span>
<span data-ttu-id="051b1-131">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="051b1-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="051b1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="051b1-132">-Confirm</span></span>
<span data-ttu-id="051b1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="051b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="051b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="051b1-134">-WhatIf</span></span>
<span data-ttu-id="051b1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="051b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="051b1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="051b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="051b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051b1-137">CommonParameters</span></span>
<span data-ttu-id="051b1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="051b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051b1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="051b1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051b1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="051b1-140">INPUTS</span></span>

### <span data-ttu-id="051b1-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="051b1-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="051b1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="051b1-142">System.String</span></span>

### <span data-ttu-id="051b1-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="051b1-143">System.Int32</span></span>

## <span data-ttu-id="051b1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="051b1-144">OUTPUTS</span></span>

### <span data-ttu-id="051b1-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="051b1-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="051b1-146">Note</span><span class="sxs-lookup"><span data-stu-id="051b1-146">NOTES</span></span>

## <span data-ttu-id="051b1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="051b1-147">RELATED LINKS</span></span>

[<span data-ttu-id="051b1-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="051b1-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="051b1-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="051b1-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="051b1-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="051b1-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="051b1-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="051b1-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="051b1-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="051b1-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

