---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 9abff0880be98c01b4953957e719fc4e6553f6ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860974"
---
# <span data-ttu-id="19f0a-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19f0a-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="19f0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="19f0a-103">Aggiunge una configurazione di probe a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="19f0a-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="19f0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19f0a-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19f0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="19f0a-106">Il cmdlet **Add-AzLoadBalancerProbeConfig** aggiunge una configurazione di probe a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="19f0a-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="19f0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19f0a-107">EXAMPLES</span></span>

### <span data-ttu-id="19f0a-108">Esempio 1 aggiungere una configurazione di probe a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="19f0a-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="19f0a-109">Questo comando ottiene il bilanciamento del carico denominato myLb, aggiunge la configurazione di probe specificata e quindi usa il cmdlet **set-AzLoadBalancer** per aggiornare il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="19f0a-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="19f0a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19f0a-110">PARAMETERS</span></span>

### <span data-ttu-id="19f0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f0a-111">-DefaultProfile</span></span>
<span data-ttu-id="19f0a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19f0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19f0a-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="19f0a-113">-IntervalInSeconds</span></span>
<span data-ttu-id="19f0a-114">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="19f0a-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="19f0a-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19f0a-115">-LoadBalancer</span></span>
<span data-ttu-id="19f0a-116">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="19f0a-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="19f0a-117">Questo cmdlet aggiunge una configurazione probe al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="19f0a-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="19f0a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="19f0a-118">-Name</span></span>
<span data-ttu-id="19f0a-119">Specifica il nome della configurazione del Probe da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="19f0a-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="19f0a-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="19f0a-120">-Port</span></span>
<span data-ttu-id="19f0a-121">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="19f0a-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="19f0a-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="19f0a-122">-ProbeCount</span></span>
<span data-ttu-id="19f0a-123">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="19f0a-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="19f0a-124">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="19f0a-124">-Protocol</span></span>
<span data-ttu-id="19f0a-125">Specifica il protocollo da usare per il probe.</span><span class="sxs-lookup"><span data-stu-id="19f0a-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="19f0a-126">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="19f0a-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="19f0a-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="19f0a-127">-RequestPath</span></span>
<span data-ttu-id="19f0a-128">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="19f0a-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="19f0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f0a-129">CommonParameters</span></span>
<span data-ttu-id="19f0a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f0a-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f0a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f0a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19f0a-132">INPUTS</span></span>

### <span data-ttu-id="19f0a-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19f0a-133">PSLoadBalancer</span></span>
<span data-ttu-id="19f0a-134">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="19f0a-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="19f0a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19f0a-135">OUTPUTS</span></span>

### <span data-ttu-id="19f0a-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19f0a-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="19f0a-137">Note</span><span class="sxs-lookup"><span data-stu-id="19f0a-137">NOTES</span></span>

## <span data-ttu-id="19f0a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19f0a-138">RELATED LINKS</span></span>

[<span data-ttu-id="19f0a-139">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19f0a-139">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19f0a-140">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19f0a-140">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19f0a-141">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19f0a-141">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19f0a-142">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19f0a-142">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="19f0a-143">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19f0a-143">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


