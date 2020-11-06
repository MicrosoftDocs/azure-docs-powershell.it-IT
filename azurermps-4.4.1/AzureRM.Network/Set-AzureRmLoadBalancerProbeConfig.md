---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9a6999dc379a5a39acea9b17107cabf2cae5ee25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513235"
---
# <span data-ttu-id="7f1dd-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7f1dd-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7f1dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1dd-103">Imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f1dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f1dd-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f1dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1dd-106">Il cmdlet **set-AzureRmLoadBalancerProbeConfig** imposta lo stato dell'obiettivo per una configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="7f1dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f1dd-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1dd-108">Esempio 1: modificare la configurazione del probe in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="7f1dd-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="7f1dd-109">Il primo comando ottiene il LoadBalancer denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="7f1dd-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzureRmLoadBalancerProbeConfig, che aggiunge una nuova configurazione di probe.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="7f1dd-111">Il terzo comando passa il bilanciamento del carico a **set-AzureRmLoadBalancerProbeConfig** , che imposta la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="7f1dd-112">Tieni presente che è necessario specificare diversi degli stessi parametri specificati nel comando precedente perché sono necessari per il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="7f1dd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f1dd-113">PARAMETERS</span></span>

### <span data-ttu-id="7f1dd-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7f1dd-114">-IntervalInSeconds</span></span>
<span data-ttu-id="7f1dd-115">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-115">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1dd-116">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f1dd-116">-LoadBalancer</span></span>
<span data-ttu-id="7f1dd-117">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-117">Specifies a load balancer.</span></span>
<span data-ttu-id="7f1dd-118">Questo cmdlet imposta lo stato obiettivo per una configurazione Probe per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-118">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f1dd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f1dd-119">-Name</span></span>
<span data-ttu-id="7f1dd-120">Specifica il nome della configurazione Probe impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-120">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="7f1dd-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="7f1dd-121">-Port</span></span>
<span data-ttu-id="7f1dd-122">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-122">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1dd-123">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="7f1dd-123">-ProbeCount</span></span>
<span data-ttu-id="7f1dd-124">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-124">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1dd-125">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7f1dd-125">-Protocol</span></span>
<span data-ttu-id="7f1dd-126">Specifica il protocollo da usare per il sondaggio.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-126">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="7f1dd-127">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-127">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1dd-128">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="7f1dd-128">-RequestPath</span></span>
<span data-ttu-id="7f1dd-129">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-129">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="7f1dd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1dd-130">-DefaultProfile</span></span>
<span data-ttu-id="7f1dd-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f1dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1dd-132">CommonParameters</span></span>
<span data-ttu-id="7f1dd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1dd-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1dd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1dd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f1dd-135">INPUTS</span></span>

### <span data-ttu-id="7f1dd-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f1dd-136">PSLoadBalancer</span></span>
<span data-ttu-id="7f1dd-137">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7f1dd-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7f1dd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f1dd-138">OUTPUTS</span></span>

### <span data-ttu-id="7f1dd-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f1dd-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7f1dd-140">Note</span><span class="sxs-lookup"><span data-stu-id="7f1dd-140">NOTES</span></span>

## <span data-ttu-id="7f1dd-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f1dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="7f1dd-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7f1dd-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7f1dd-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f1dd-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="7f1dd-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7f1dd-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7f1dd-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7f1dd-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7f1dd-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7f1dd-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


