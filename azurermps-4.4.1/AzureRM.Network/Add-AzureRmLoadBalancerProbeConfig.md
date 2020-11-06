---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 79e9d856825e174bc8667f99e7b25b301230dec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519568"
---
# <span data-ttu-id="779da-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="779da-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="779da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="779da-102">SYNOPSIS</span></span>
<span data-ttu-id="779da-103">Aggiunge una configurazione di probe a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="779da-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="779da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="779da-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="779da-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="779da-105">DESCRIPTION</span></span>
<span data-ttu-id="779da-106">Il cmdlet **Add-AzureRmLoadBalancerProbeConfig** aggiunge una configurazione di probe a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="779da-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="779da-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="779da-107">EXAMPLES</span></span>

### <span data-ttu-id="779da-108">Esempio 1 aggiungere una configurazione di probe a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="779da-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="779da-109">Questo comando ottiene il bilanciamento del carico denominato myLb, aggiunge la configurazione di probe specificata e quindi usa il cmdlet **set-AzureRmLoadBalancer** per aggiornare il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="779da-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="779da-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="779da-110">PARAMETERS</span></span>

### <span data-ttu-id="779da-111">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="779da-111">-IntervalInSeconds</span></span>
<span data-ttu-id="779da-112">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="779da-112">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="779da-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="779da-113">-LoadBalancer</span></span>
<span data-ttu-id="779da-114">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="779da-114">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="779da-115">Questo cmdlet aggiunge una configurazione probe al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="779da-115">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="779da-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="779da-116">-Name</span></span>
<span data-ttu-id="779da-117">Specifica il nome della configurazione del Probe da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="779da-117">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="779da-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="779da-118">-Port</span></span>
<span data-ttu-id="779da-119">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="779da-119">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="779da-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="779da-120">-ProbeCount</span></span>
<span data-ttu-id="779da-121">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="779da-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="779da-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="779da-122">-Protocol</span></span>
<span data-ttu-id="779da-123">Specifica il protocollo da usare per il probe.</span><span class="sxs-lookup"><span data-stu-id="779da-123">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="779da-124">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="779da-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="779da-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="779da-125">-RequestPath</span></span>
<span data-ttu-id="779da-126">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="779da-126">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="779da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779da-127">-DefaultProfile</span></span>
<span data-ttu-id="779da-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="779da-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="779da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779da-129">CommonParameters</span></span>
<span data-ttu-id="779da-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779da-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779da-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="779da-132">INPUTS</span></span>

### <span data-ttu-id="779da-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="779da-133">PSLoadBalancer</span></span>
<span data-ttu-id="779da-134">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="779da-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="779da-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="779da-135">OUTPUTS</span></span>

### <span data-ttu-id="779da-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="779da-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="779da-137">Note</span><span class="sxs-lookup"><span data-stu-id="779da-137">NOTES</span></span>

## <span data-ttu-id="779da-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="779da-138">RELATED LINKS</span></span>

[<span data-ttu-id="779da-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="779da-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="779da-140">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="779da-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="779da-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="779da-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="779da-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="779da-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="779da-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="779da-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


