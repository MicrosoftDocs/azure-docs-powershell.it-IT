---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 622501a69632be9c9c70cfccaf4e806df94e7276
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006478"
---
# <span data-ttu-id="b8935-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8935-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b8935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8935-102">SYNOPSIS</span></span>
<span data-ttu-id="b8935-103">Aggiunge una configurazione a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b8935-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="b8935-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8935-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8935-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b8935-105">DESCRIPTION</span></span>
<span data-ttu-id="b8935-106">Il cmdlet **Add-AzLoadBalancerProbeConfig aggiunge** una configurazione dominio a una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="b8935-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b8935-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8935-107">EXAMPLES</span></span>

### <span data-ttu-id="b8935-108">Esempio 1: Aggiungere una configurazione di configurazione a un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="b8935-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="b8935-109">Questo comando recupera la bilanciamento del carico denominata myLb, aggiunge la configurazione di configurazione specificata e quindi usa il cmdlet **Set-AzLoadBalancer** per aggiornare la bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b8935-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="b8935-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8935-110">PARAMETERS</span></span>

### <span data-ttu-id="b8935-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8935-111">-DefaultProfile</span></span>
<span data-ttu-id="b8935-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8935-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8935-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b8935-113">-IntervalInSeconds</span></span>
<span data-ttu-id="b8935-114">Specifica l'intervallo, in secondi, tra le due istanze del servizio con carico bilanciato.</span><span class="sxs-lookup"><span data-stu-id="b8935-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="b8935-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8935-115">-LoadBalancer</span></span>
<span data-ttu-id="b8935-116">Specifica un **oggetto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="b8935-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b8935-117">Questo cmdlet aggiunge una configurazione di configurazione al servizio di bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b8935-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8935-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b8935-118">-Name</span></span>
<span data-ttu-id="b8935-119">Specifica il nome della configurazione da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b8935-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="b8935-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="b8935-120">-Port</span></span>
<span data-ttu-id="b8935-121">Specifica la porta in cui le applicazioni devono connettersi a un servizio con carico bilanciato.</span><span class="sxs-lookup"><span data-stu-id="b8935-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="b8935-122">-CountCount</span><span class="sxs-lookup"><span data-stu-id="b8935-122">-ProbeCount</span></span>
<span data-ttu-id="b8935-123">Specifica il numero di errori consecutivi per istanza per cui un'istanza deve essere considerata non integra.</span><span class="sxs-lookup"><span data-stu-id="b8935-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="b8935-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b8935-124">-Protocol</span></span>
<span data-ttu-id="b8935-125">Specifica il protocollo da usare per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b8935-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="b8935-126">I valori accettabili per questo parametro sono: Tcp o Http.</span><span class="sxs-lookup"><span data-stu-id="b8935-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="b8935-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="b8935-127">-RequestPath</span></span>
<span data-ttu-id="b8935-128">Specifica il percorso nel servizio con carico bilanciato per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="b8935-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="b8935-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8935-129">-Confirm</span></span>
<span data-ttu-id="b8935-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8935-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8935-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8935-131">-WhatIf</span></span>
<span data-ttu-id="b8935-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8935-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8935-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8935-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8935-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8935-134">CommonParameters</span></span>
<span data-ttu-id="b8935-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8935-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8935-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8935-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8935-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b8935-137">INPUTS</span></span>

### <span data-ttu-id="b8935-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8935-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b8935-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b8935-139">System.String</span></span>

### <span data-ttu-id="b8935-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b8935-140">System.Int32</span></span>

## <span data-ttu-id="b8935-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8935-141">OUTPUTS</span></span>

### <span data-ttu-id="b8935-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8935-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b8935-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b8935-143">NOTES</span></span>

## <span data-ttu-id="b8935-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8935-144">RELATED LINKS</span></span>

[<span data-ttu-id="b8935-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8935-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b8935-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8935-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b8935-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8935-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b8935-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8935-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="b8935-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8935-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


