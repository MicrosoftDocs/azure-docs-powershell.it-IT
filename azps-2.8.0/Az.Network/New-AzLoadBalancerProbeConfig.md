---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854441"
---
# <span data-ttu-id="54f57-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54f57-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="54f57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54f57-102">SYNOPSIS</span></span>
<span data-ttu-id="54f57-103">Crea una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="54f57-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="54f57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54f57-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54f57-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54f57-105">DESCRIPTION</span></span>
<span data-ttu-id="54f57-106">Il cmdlet **New-AzLoadBalancerProbeConfig** crea una configurazione di probe per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="54f57-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="54f57-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54f57-107">EXAMPLES</span></span>

### <span data-ttu-id="54f57-108">Esempio 1: creare una configurazione Probe</span><span class="sxs-lookup"><span data-stu-id="54f57-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="54f57-109">Questo comando crea una configurazione di probe denominata Probe usando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="54f57-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="54f57-110">La nuova sonda si connette a un servizio con bilanciamento del carico sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="54f57-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="54f57-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54f57-111">PARAMETERS</span></span>

### <span data-ttu-id="54f57-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f57-112">-DefaultProfile</span></span>
<span data-ttu-id="54f57-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54f57-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f57-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="54f57-114">-IntervalInSeconds</span></span>
<span data-ttu-id="54f57-115">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza di un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="54f57-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="54f57-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="54f57-116">-Name</span></span>
<span data-ttu-id="54f57-117">Specifica il nome della configurazione del Probe da creare.</span><span class="sxs-lookup"><span data-stu-id="54f57-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="54f57-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="54f57-118">-Port</span></span>
<span data-ttu-id="54f57-119">Specifica la porta in cui la nuova sonda deve connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="54f57-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="54f57-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="54f57-120">-ProbeCount</span></span>
<span data-ttu-id="54f57-121">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="54f57-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="54f57-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="54f57-122">-Protocol</span></span>
<span data-ttu-id="54f57-123">Specifica il protocollo da usare per la configurazione del probe.</span><span class="sxs-lookup"><span data-stu-id="54f57-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="54f57-124">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="54f57-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="54f57-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="54f57-125">-RequestPath</span></span>
<span data-ttu-id="54f57-126">Specifica il percorso in un servizio con bilanciamento del carico da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="54f57-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="54f57-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54f57-127">-Confirm</span></span>
<span data-ttu-id="54f57-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54f57-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f57-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f57-129">-WhatIf</span></span>
<span data-ttu-id="54f57-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54f57-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54f57-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54f57-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f57-132">CommonParameters</span></span>
<span data-ttu-id="54f57-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f57-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f57-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f57-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54f57-135">INPUTS</span></span>

### <span data-ttu-id="54f57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="54f57-136">System.String</span></span>

### <span data-ttu-id="54f57-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="54f57-137">System.Int32</span></span>

## <span data-ttu-id="54f57-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54f57-138">OUTPUTS</span></span>

### <span data-ttu-id="54f57-139">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="54f57-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="54f57-140">Note</span><span class="sxs-lookup"><span data-stu-id="54f57-140">NOTES</span></span>

## <span data-ttu-id="54f57-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54f57-141">RELATED LINKS</span></span>

[<span data-ttu-id="54f57-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54f57-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54f57-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54f57-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54f57-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54f57-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="54f57-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="54f57-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


