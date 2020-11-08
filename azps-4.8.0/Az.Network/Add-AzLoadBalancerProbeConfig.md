---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189562"
---
# <span data-ttu-id="fad1e-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad1e-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="fad1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fad1e-102">SYNOPSIS</span></span>
<span data-ttu-id="fad1e-103">Aggiunge una configurazione di probe a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fad1e-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="fad1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fad1e-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fad1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad1e-105">DESCRIPTION</span></span>
<span data-ttu-id="fad1e-106">Il cmdlet **Add-AzLoadBalancerProbeConfig** aggiunge una configurazione di probe a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="fad1e-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="fad1e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fad1e-107">EXAMPLES</span></span>

### <span data-ttu-id="fad1e-108">Esempio 1: aggiungere una configurazione di probe a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="fad1e-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="fad1e-109">Questo comando ottiene il bilanciamento del carico denominato myLb, aggiunge la configurazione di probe specificata e quindi usa il cmdlet **set-AzLoadBalancer** per aggiornare il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fad1e-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="fad1e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fad1e-110">PARAMETERS</span></span>

### <span data-ttu-id="fad1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad1e-111">-DefaultProfile</span></span>
<span data-ttu-id="fad1e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fad1e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad1e-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fad1e-113">-IntervalInSeconds</span></span>
<span data-ttu-id="fad1e-114">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fad1e-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="fad1e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fad1e-115">-LoadBalancer</span></span>
<span data-ttu-id="fad1e-116">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="fad1e-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="fad1e-117">Questo cmdlet aggiunge una configurazione probe al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fad1e-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fad1e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fad1e-118">-Name</span></span>
<span data-ttu-id="fad1e-119">Specifica il nome della configurazione del Probe da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fad1e-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="fad1e-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="fad1e-120">-Port</span></span>
<span data-ttu-id="fad1e-121">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fad1e-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="fad1e-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="fad1e-122">-ProbeCount</span></span>
<span data-ttu-id="fad1e-123">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="fad1e-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="fad1e-124">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="fad1e-124">-Protocol</span></span>
<span data-ttu-id="fad1e-125">Specifica il protocollo da usare per il probe.</span><span class="sxs-lookup"><span data-stu-id="fad1e-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="fad1e-126">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="fad1e-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="fad1e-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="fad1e-127">-RequestPath</span></span>
<span data-ttu-id="fad1e-128">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="fad1e-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="fad1e-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fad1e-129">-Confirm</span></span>
<span data-ttu-id="fad1e-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad1e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fad1e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fad1e-131">-WhatIf</span></span>
<span data-ttu-id="fad1e-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fad1e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fad1e-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fad1e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fad1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad1e-134">CommonParameters</span></span>
<span data-ttu-id="fad1e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad1e-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad1e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad1e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fad1e-137">INPUTS</span></span>

### <span data-ttu-id="fad1e-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fad1e-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="fad1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fad1e-139">System.String</span></span>

### <span data-ttu-id="fad1e-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fad1e-140">System.Int32</span></span>

## <span data-ttu-id="fad1e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fad1e-141">OUTPUTS</span></span>

### <span data-ttu-id="fad1e-142">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fad1e-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fad1e-143">Note</span><span class="sxs-lookup"><span data-stu-id="fad1e-143">NOTES</span></span>

## <span data-ttu-id="fad1e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fad1e-144">RELATED LINKS</span></span>

[<span data-ttu-id="fad1e-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad1e-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fad1e-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad1e-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fad1e-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad1e-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fad1e-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fad1e-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="fad1e-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad1e-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


