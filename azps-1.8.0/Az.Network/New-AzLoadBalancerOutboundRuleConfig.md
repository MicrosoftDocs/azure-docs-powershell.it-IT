---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50a8cd14c6ea61f7c772df96f4addb9ae7955444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678278"
---
# <span data-ttu-id="b572f-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b572f-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="b572f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b572f-102">SYNOPSIS</span></span>
<span data-ttu-id="b572f-103">Crea una configurazione della regola in uscita per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b572f-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b572f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b572f-104">SYNTAX</span></span>

### <span data-ttu-id="b572f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b572f-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b572f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b572f-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b572f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b572f-107">DESCRIPTION</span></span>
<span data-ttu-id="b572f-108">Il cmdlet **New-AzLoadBalancerOutboundRuleConfig** crea una configurazione della regola in uscita per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="b572f-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b572f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b572f-109">EXAMPLES</span></span>

### <span data-ttu-id="b572f-110">Esempio 1: creare una configurazione della regola in uscita per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="b572f-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="b572f-111">Il primo comando crea un indirizzo IP pubblico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="b572f-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="b572f-112">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip e lo archivia nella variabile $frontend.</span><span class="sxs-lookup"><span data-stu-id="b572f-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="b572f-113">Il terzo comando crea una configurazione del pool di indirizzi back-end denominata BackendAddressPool01 e la archivia nella variabile $backend.</span><span class="sxs-lookup"><span data-stu-id="b572f-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="b572f-114">Il quarto comando crea una configurazione di regola in uscita denominata MyOutboundRule usando gli oggetti front-end e back-end in $frontend e $backend.</span><span class="sxs-lookup"><span data-stu-id="b572f-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="b572f-115">I parametri *Protocol* , *FrontendIPConfiguration* e *BackendAddressPool* sono tutti necessari per creare una configurazione di regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="b572f-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="b572f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b572f-116">PARAMETERS</span></span>

### <span data-ttu-id="b572f-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="b572f-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="b572f-118">Numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="b572f-118">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b572f-119">-BackendAddressPool</span></span>
<span data-ttu-id="b572f-120">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="b572f-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="b572f-121">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="b572f-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b572f-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="b572f-123">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="b572f-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="b572f-124">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="b572f-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b572f-125">-DefaultProfile</span></span>
<span data-ttu-id="b572f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b572f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b572f-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b572f-127">-EnableTcpReset</span></span>
<span data-ttu-id="b572f-128">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="b572f-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="b572f-129">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="b572f-129">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b572f-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b572f-131">Gli indirizzi IP del frontend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b572f-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b572f-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b572f-133">Timeout per la connessione inattiva TCP</span><span class="sxs-lookup"><span data-stu-id="b572f-133">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="b572f-134">-Name</span></span>
<span data-ttu-id="b572f-135">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="b572f-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="b572f-136">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b572f-136">-Protocol</span></span>
<span data-ttu-id="b572f-137">Protocol-TCP, UDP o all</span><span class="sxs-lookup"><span data-stu-id="b572f-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b572f-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b572f-138">-Confirm</span></span>
<span data-ttu-id="b572f-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b572f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b572f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b572f-140">-WhatIf</span></span>
<span data-ttu-id="b572f-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b572f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b572f-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b572f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b572f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b572f-143">CommonParameters</span></span>
<span data-ttu-id="b572f-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b572f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b572f-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b572f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b572f-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b572f-146">INPUTS</span></span>

### <span data-ttu-id="b572f-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b572f-147">System.Int32</span></span>

### <span data-ttu-id="b572f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b572f-148">System.String</span></span>

### <span data-ttu-id="b572f-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="b572f-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="b572f-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b572f-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b572f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b572f-151">OUTPUTS</span></span>

### <span data-ttu-id="b572f-152">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="b572f-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="b572f-153">Note</span><span class="sxs-lookup"><span data-stu-id="b572f-153">NOTES</span></span>

## <span data-ttu-id="b572f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b572f-154">RELATED LINKS</span></span>

[<span data-ttu-id="b572f-155">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b572f-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b572f-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b572f-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b572f-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b572f-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b572f-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b572f-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)