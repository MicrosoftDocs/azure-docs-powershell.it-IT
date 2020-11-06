---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515056"
---
# <span data-ttu-id="97948-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97948-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="97948-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97948-102">SYNOPSIS</span></span>
<span data-ttu-id="97948-103">Crea una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="97948-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97948-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97948-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97948-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97948-105">DESCRIPTION</span></span>
<span data-ttu-id="97948-106">Il cmdlet **New-AzureRmLoadBalancerProbeConfig** crea una configurazione di probe per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="97948-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="97948-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97948-107">EXAMPLES</span></span>

### <span data-ttu-id="97948-108">Esempio 1: creare una configurazione Probe</span><span class="sxs-lookup"><span data-stu-id="97948-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="97948-109">Questo comando crea una configurazione di probe denominata Probe usando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="97948-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="97948-110">La nuova sonda si connette a un servizio con bilanciamento del carico sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="97948-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="97948-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97948-111">PARAMETERS</span></span>

### <span data-ttu-id="97948-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97948-112">-DefaultProfile</span></span>
<span data-ttu-id="97948-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97948-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97948-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="97948-114">-IntervalInSeconds</span></span>
<span data-ttu-id="97948-115">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza di un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="97948-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="97948-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="97948-116">-Name</span></span>
<span data-ttu-id="97948-117">Specifica il nome della configurazione del Probe da creare.</span><span class="sxs-lookup"><span data-stu-id="97948-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="97948-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="97948-118">-Port</span></span>
<span data-ttu-id="97948-119">Specifica la porta in cui la nuova sonda deve connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="97948-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="97948-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="97948-120">-ProbeCount</span></span>
<span data-ttu-id="97948-121">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="97948-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="97948-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="97948-122">-Protocol</span></span>
<span data-ttu-id="97948-123">Specifica il protocollo da usare per la configurazione del probe.</span><span class="sxs-lookup"><span data-stu-id="97948-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="97948-124">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="97948-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="97948-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="97948-125">-RequestPath</span></span>
<span data-ttu-id="97948-126">Specifica il percorso in un servizio con bilanciamento del carico da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="97948-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="97948-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97948-127">-Confirm</span></span>
<span data-ttu-id="97948-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97948-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97948-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97948-129">-WhatIf</span></span>
<span data-ttu-id="97948-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97948-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97948-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97948-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97948-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97948-132">CommonParameters</span></span>
<span data-ttu-id="97948-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97948-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97948-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97948-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97948-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97948-135">INPUTS</span></span>

### <span data-ttu-id="97948-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97948-136">None</span></span>

## <span data-ttu-id="97948-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97948-137">OUTPUTS</span></span>

### <span data-ttu-id="97948-138">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="97948-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="97948-139">Note</span><span class="sxs-lookup"><span data-stu-id="97948-139">NOTES</span></span>

## <span data-ttu-id="97948-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97948-140">RELATED LINKS</span></span>

[<span data-ttu-id="97948-141">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97948-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="97948-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97948-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="97948-143">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97948-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="97948-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="97948-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


