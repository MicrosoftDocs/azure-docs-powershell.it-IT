---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520179"
---
# <span data-ttu-id="243aa-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="243aa-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="243aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="243aa-102">SYNOPSIS</span></span>
<span data-ttu-id="243aa-103">Aggiunge una configurazione di probe a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="243aa-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="243aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="243aa-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="243aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="243aa-105">DESCRIPTION</span></span>
<span data-ttu-id="243aa-106">Il cmdlet **Add-AzureRmLoadBalancerProbeConfig** aggiunge una configurazione di probe a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="243aa-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="243aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="243aa-107">EXAMPLES</span></span>

### <span data-ttu-id="243aa-108">Esempio 1 aggiungere una configurazione di probe a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="243aa-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="243aa-109">Questo comando ottiene il bilanciamento del carico denominato myLb, aggiunge la configurazione di probe specificata e quindi usa il cmdlet **set-AzureRmLoadBalancer** per aggiornare il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="243aa-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="243aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="243aa-110">PARAMETERS</span></span>

### <span data-ttu-id="243aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243aa-111">-DefaultProfile</span></span>
<span data-ttu-id="243aa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="243aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="243aa-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="243aa-113">-IntervalInSeconds</span></span>
<span data-ttu-id="243aa-114">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza del servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="243aa-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="243aa-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="243aa-115">-LoadBalancer</span></span>
<span data-ttu-id="243aa-116">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="243aa-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="243aa-117">Questo cmdlet aggiunge una configurazione probe al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="243aa-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="243aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="243aa-118">-Name</span></span>
<span data-ttu-id="243aa-119">Specifica il nome della configurazione del Probe da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="243aa-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="243aa-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="243aa-120">-Port</span></span>
<span data-ttu-id="243aa-121">Specifica la porta in cui le sonde devono connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="243aa-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="243aa-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="243aa-122">-ProbeCount</span></span>
<span data-ttu-id="243aa-123">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="243aa-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="243aa-124">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="243aa-124">-Protocol</span></span>
<span data-ttu-id="243aa-125">Specifica il protocollo da usare per il probe.</span><span class="sxs-lookup"><span data-stu-id="243aa-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="243aa-126">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="243aa-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="243aa-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="243aa-127">-RequestPath</span></span>
<span data-ttu-id="243aa-128">Specifica il percorso nel servizio a carico bilanciato da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="243aa-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="243aa-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="243aa-129">-Confirm</span></span>
<span data-ttu-id="243aa-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="243aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="243aa-131">-WhatIf</span></span>
<span data-ttu-id="243aa-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="243aa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="243aa-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="243aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="243aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243aa-134">CommonParameters</span></span>
<span data-ttu-id="243aa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243aa-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243aa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="243aa-137">INPUTS</span></span>

### <span data-ttu-id="243aa-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="243aa-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="243aa-139">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="243aa-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="243aa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="243aa-140">OUTPUTS</span></span>

### <span data-ttu-id="243aa-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="243aa-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="243aa-142">Note</span><span class="sxs-lookup"><span data-stu-id="243aa-142">NOTES</span></span>

## <span data-ttu-id="243aa-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="243aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="243aa-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="243aa-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="243aa-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="243aa-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="243aa-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="243aa-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="243aa-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="243aa-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="243aa-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="243aa-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


