---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862777"
---
# <span data-ttu-id="7887c-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7887c-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7887c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7887c-102">SYNOPSIS</span></span>
<span data-ttu-id="7887c-103">Imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7887c-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="7887c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7887c-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7887c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7887c-105">DESCRIPTION</span></span>
<span data-ttu-id="7887c-106">Il cmdlet **set-AzLoadBalancerProbeConfig** imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7887c-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="7887c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7887c-107">EXAMPLES</span></span>

### <span data-ttu-id="7887c-108">Esempio 1: modificare la configurazione del probe in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="7887c-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="7887c-109">Il primo comando ottiene il LoadBalancer denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="7887c-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="7887c-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerProbeConfig, che aggiunge una nuova configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7887c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="7887c-111">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerProbeConfig** , che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="7887c-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="7887c-112">Tieni presente che è necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="7887c-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="7887c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7887c-113">PARAMETERS</span></span>

### <span data-ttu-id="7887c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7887c-114">-DefaultProfile</span></span>
<span data-ttu-id="7887c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7887c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7887c-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7887c-116">-IntervalInSeconds</span></span>
<span data-ttu-id="7887c-117">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7887c-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7887c-118">-LoadBalancer</span></span>
<span data-ttu-id="7887c-119">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7887c-119">Specifies a load balancer.</span></span>
<span data-ttu-id="7887c-120">Questo cmdlet imposta lo stato obiettivo per una configurazione Probe per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7887c-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7887c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7887c-121">-Name</span></span>
<span data-ttu-id="7887c-122">Specifica il nome della configurazione Probe impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7887c-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="7887c-123">-Port</span></span>
<span data-ttu-id="7887c-124">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7887c-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="7887c-125">-ProbeCount</span></span>
<span data-ttu-id="7887c-126">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="7887c-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7887c-127">-Protocol</span></span>
<span data-ttu-id="7887c-128">Specifica il protocollo da usare per il sondaggio.</span><span class="sxs-lookup"><span data-stu-id="7887c-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="7887c-129">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="7887c-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="7887c-130">-RequestPath</span></span>
<span data-ttu-id="7887c-131">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="7887c-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7887c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7887c-132">CommonParameters</span></span>
<span data-ttu-id="7887c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7887c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7887c-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7887c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7887c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7887c-135">INPUTS</span></span>

### <span data-ttu-id="7887c-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7887c-136">PSLoadBalancer</span></span>
<span data-ttu-id="7887c-137">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7887c-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7887c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7887c-138">OUTPUTS</span></span>

### <span data-ttu-id="7887c-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7887c-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7887c-140">Note</span><span class="sxs-lookup"><span data-stu-id="7887c-140">NOTES</span></span>

## <span data-ttu-id="7887c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7887c-141">RELATED LINKS</span></span>

[<span data-ttu-id="7887c-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7887c-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7887c-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7887c-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7887c-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7887c-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7887c-145">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7887c-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="7887c-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7887c-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


