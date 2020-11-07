---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686256"
---
# <span data-ttu-id="2f82c-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f82c-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2f82c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f82c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f82c-103">Imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="2f82c-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f82c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f82c-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f82c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f82c-105">DESCRIPTION</span></span>
<span data-ttu-id="2f82c-106">Il cmdlet **set-AzureRmLoadBalancerProbeConfig** imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="2f82c-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="2f82c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f82c-107">EXAMPLES</span></span>

### <span data-ttu-id="2f82c-108">Esempio 1: modificare la configurazione del probe in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="2f82c-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="2f82c-109">Il primo comando ottiene il LoadBalancer denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="2f82c-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2f82c-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzureRmLoadBalancerProbeConfig, che aggiunge una nuova configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="2f82c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="2f82c-111">Il terzo comando passa il bilanciamento del carico a **set-AzureRmLoadBalancerProbeConfig** , che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="2f82c-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="2f82c-112">Tieni presente che è necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="2f82c-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="2f82c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f82c-113">PARAMETERS</span></span>

### <span data-ttu-id="2f82c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f82c-114">-DefaultProfile</span></span>
<span data-ttu-id="2f82c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f82c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f82c-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2f82c-116">-IntervalInSeconds</span></span>
<span data-ttu-id="2f82c-117">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2f82c-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="2f82c-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f82c-118">-LoadBalancer</span></span>
<span data-ttu-id="2f82c-119">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2f82c-119">Specifies a load balancer.</span></span>
<span data-ttu-id="2f82c-120">Questo cmdlet imposta lo stato obiettivo per una configurazione Probe per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2f82c-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f82c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f82c-121">-Name</span></span>
<span data-ttu-id="2f82c-122">Specifica il nome della configurazione Probe impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f82c-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2f82c-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="2f82c-123">-Port</span></span>
<span data-ttu-id="2f82c-124">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2f82c-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="2f82c-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="2f82c-125">-ProbeCount</span></span>
<span data-ttu-id="2f82c-126">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="2f82c-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="2f82c-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="2f82c-127">-Protocol</span></span>
<span data-ttu-id="2f82c-128">Specifica il protocollo da usare per il sondaggio.</span><span class="sxs-lookup"><span data-stu-id="2f82c-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="2f82c-129">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="2f82c-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="2f82c-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="2f82c-130">-RequestPath</span></span>
<span data-ttu-id="2f82c-131">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="2f82c-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="2f82c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f82c-132">-Confirm</span></span>
<span data-ttu-id="2f82c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f82c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f82c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f82c-134">-WhatIf</span></span>
<span data-ttu-id="2f82c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f82c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f82c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f82c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f82c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f82c-137">CommonParameters</span></span>
<span data-ttu-id="2f82c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f82c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f82c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f82c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f82c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f82c-140">INPUTS</span></span>

### <span data-ttu-id="2f82c-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f82c-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="2f82c-142">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f82c-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="2f82c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f82c-143">OUTPUTS</span></span>

### <span data-ttu-id="2f82c-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f82c-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2f82c-145">Note</span><span class="sxs-lookup"><span data-stu-id="2f82c-145">NOTES</span></span>

## <span data-ttu-id="2f82c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f82c-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f82c-147">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f82c-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2f82c-148">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f82c-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2f82c-149">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f82c-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2f82c-150">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f82c-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="2f82c-151">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f82c-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


