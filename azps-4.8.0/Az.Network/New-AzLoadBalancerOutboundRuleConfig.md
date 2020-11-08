---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032935"
---
# <span data-ttu-id="c43b9-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c43b9-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c43b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c43b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c43b9-103">Crea una configurazione della regola in uscita per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c43b9-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c43b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c43b9-104">SYNTAX</span></span>

### <span data-ttu-id="c43b9-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c43b9-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c43b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c43b9-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c43b9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c43b9-107">DESCRIPTION</span></span>
<span data-ttu-id="c43b9-108">Il cmdlet **New-AzLoadBalancerOutboundRuleConfig** crea una configurazione della regola in uscita per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c43b9-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c43b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c43b9-109">EXAMPLES</span></span>

### <span data-ttu-id="c43b9-110">Esempio 1: creare una configurazione della regola in uscita per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c43b9-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="c43b9-111">Il primo comando crea un indirizzo IP pubblico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="c43b9-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="c43b9-112">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip e lo archivia nella variabile $frontend.</span><span class="sxs-lookup"><span data-stu-id="c43b9-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="c43b9-113">Il terzo comando crea una configurazione del pool di indirizzi back-end denominata BackendAddressPool01 e la archivia nella variabile $backend.</span><span class="sxs-lookup"><span data-stu-id="c43b9-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="c43b9-114">Il quarto comando crea una configurazione di regola in uscita denominata MyOutboundRule usando gli oggetti front-end e back-end in $frontend e $backend.</span><span class="sxs-lookup"><span data-stu-id="c43b9-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="c43b9-115">I parametri *Protocol* , *FrontendIPConfiguration* e *BackendAddressPool* sono tutti necessari per creare una configurazione di regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="c43b9-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="c43b9-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c43b9-116">Example 2</span></span>

<span data-ttu-id="c43b9-117">Crea una configurazione della regola in uscita per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c43b9-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="c43b9-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c43b9-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="c43b9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c43b9-119">PARAMETERS</span></span>

### <span data-ttu-id="c43b9-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c43b9-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c43b9-121">Numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="c43b9-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c43b9-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c43b9-122">-BackendAddressPool</span></span>
<span data-ttu-id="c43b9-123">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="c43b9-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c43b9-124">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="c43b9-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c43b9-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c43b9-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="c43b9-126">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="c43b9-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c43b9-127">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="c43b9-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c43b9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43b9-128">-DefaultProfile</span></span>
<span data-ttu-id="c43b9-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c43b9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43b9-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c43b9-130">-EnableTcpReset</span></span>
<span data-ttu-id="c43b9-131">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="c43b9-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c43b9-132">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="c43b9-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c43b9-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c43b9-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c43b9-134">Gli indirizzi IP del frontend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c43b9-134">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="c43b9-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c43b9-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c43b9-136">Timeout per la connessione inattiva TCP</span><span class="sxs-lookup"><span data-stu-id="c43b9-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c43b9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="c43b9-137">-Name</span></span>
<span data-ttu-id="c43b9-138">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="c43b9-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c43b9-139">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c43b9-139">-Protocol</span></span>
<span data-ttu-id="c43b9-140">Protocol-TCP, UDP o all</span><span class="sxs-lookup"><span data-stu-id="c43b9-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="c43b9-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c43b9-141">-Confirm</span></span>
<span data-ttu-id="c43b9-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43b9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43b9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43b9-143">-WhatIf</span></span>
<span data-ttu-id="c43b9-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c43b9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c43b9-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c43b9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43b9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43b9-146">CommonParameters</span></span>
<span data-ttu-id="c43b9-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43b9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43b9-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43b9-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43b9-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c43b9-149">INPUTS</span></span>

### <span data-ttu-id="c43b9-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c43b9-150">System.Int32</span></span>

### <span data-ttu-id="c43b9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c43b9-151">System.String</span></span>

### <span data-ttu-id="c43b9-152">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c43b9-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c43b9-153">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c43b9-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c43b9-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c43b9-154">OUTPUTS</span></span>

### <span data-ttu-id="c43b9-155">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="c43b9-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="c43b9-156">Note</span><span class="sxs-lookup"><span data-stu-id="c43b9-156">NOTES</span></span>

## <span data-ttu-id="c43b9-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c43b9-157">RELATED LINKS</span></span>

[<span data-ttu-id="c43b9-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c43b9-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c43b9-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c43b9-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c43b9-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c43b9-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c43b9-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c43b9-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
