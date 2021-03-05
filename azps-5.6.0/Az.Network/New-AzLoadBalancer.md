---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 2bc63fb21de63dc35855acad53c7e42a13caf215
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011838"
---
# <span data-ttu-id="26df8-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26df8-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="26df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26df8-102">SYNOPSIS</span></span>
<span data-ttu-id="26df8-103">Crea una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-103">Creates a load balancer.</span></span>

## <span data-ttu-id="26df8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26df8-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26df8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26df8-105">DESCRIPTION</span></span>
<span data-ttu-id="26df8-106">Il cmdlet **New-AzLoadBalancer** crea una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="26df8-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="26df8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26df8-107">EXAMPLES</span></span>

### <span data-ttu-id="26df8-108">Esempio 1: Creare una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="26df8-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="26df8-109">Per distribuire una soluzione di bilanciamento del carico è necessario creare prima diversi oggetti e i primi sette comandi mostrano come creare tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="26df8-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="26df8-110">L'ottavo comando crea una bilanciamento del carico denominata MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26df8-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="26df8-111">Il nono e l'ultimo comando recuperano la nuova funzionalità di bilanciamento del carico per assicurarsi che sia stata creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="26df8-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="26df8-112">Si noti che questo esempio illustra solo come creare una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="26df8-113">È anche necessario configurarla usando il cmdlet Add-AzNetworkInterfaceIpConfig per assegnare le nicchie a macchine virtuali diverse.</span><span class="sxs-lookup"><span data-stu-id="26df8-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="26df8-114">Esempio 2: Creare una bilanciamento del carico globale</span><span class="sxs-lookup"><span data-stu-id="26df8-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="26df8-115">La distribuzione di una soluzione di bilanciamento del carico globale richiede la creazione di diversi oggetti e i primi cinque comandi mostrano come creare tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="26df8-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="26df8-116">Il sesto comando crea una bilanciamento del carico denominata MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26df8-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="26df8-117">Il settimo e l'ultimo comando ottiene il nuovo bilanciamento del carico per assicurarsi che sia stato creato correttamente.</span><span class="sxs-lookup"><span data-stu-id="26df8-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="26df8-118">Si noti che questo esempio illustra solo come creare una bilanciamento del carico globale.</span><span class="sxs-lookup"><span data-stu-id="26df8-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="26df8-119">È anche necessario configurarla usando il cmdlet New-AzLoadBalancerBackendAddressConfig per assegnare id frontend ipconfig di bilanciamento del carico locale al pool di indirizzi back-end</span><span class="sxs-lookup"><span data-stu-id="26df8-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="26df8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26df8-120">PARAMETERS</span></span>

### <span data-ttu-id="26df8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26df8-121">-AsJob</span></span>
<span data-ttu-id="26df8-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="26df8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26df8-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="26df8-123">-BackendAddressPool</span></span>
<span data-ttu-id="26df8-124">Specifica un pool di indirizzi back-end da associare a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26df8-125">-DefaultProfile</span></span>
<span data-ttu-id="26df8-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26df8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26df8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="26df8-127">-Force</span></span>
<span data-ttu-id="26df8-128">Indica che questo cmdlet crea una bilanciamento del carico anche se esiste già una bilanciamento del carico con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="26df8-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="26df8-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="26df8-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="26df8-130">Specifica un elenco di indirizzi IP front-end da associare a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="26df8-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="26df8-132">-InboundNatRule</span></span>
<span data-ttu-id="26df8-133">Specifica un elenco di regole NAT (Network Address Translation) in ingresso da associare a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="26df8-134">-LoadBalancingRule</span></span>
<span data-ttu-id="26df8-135">Specifica un elenco di regole di bilanciamento del carico da associare a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-136">-Location</span><span class="sxs-lookup"><span data-stu-id="26df8-136">-Location</span></span>
<span data-ttu-id="26df8-137">Specifica l'area in cui creare un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="26df8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="26df8-138">-Name</span></span>
<span data-ttu-id="26df8-139">Specifica il nome della bilanciamento del carico creato.</span><span class="sxs-lookup"><span data-stu-id="26df8-139">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="26df8-140">-OutboundRule</span></span>
<span data-ttu-id="26df8-141">Regole in uscita.</span><span class="sxs-lookup"><span data-stu-id="26df8-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-142">-Snodato</span><span class="sxs-lookup"><span data-stu-id="26df8-142">-Probe</span></span>
<span data-ttu-id="26df8-143">Specifica un elenco di campi da associare a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26df8-144">-ResourceGroupName</span></span>
<span data-ttu-id="26df8-145">Specifica il nome del gruppo di risorse in cui creare una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="26df8-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="26df8-146">-Sku</span></span>
<span data-ttu-id="26df8-147">Nome della SKU della bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="26df8-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="26df8-148">-Tag</span></span>
<span data-ttu-id="26df8-149">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="26df8-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26df8-150">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="26df8-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="26df8-151">-Tier</span></span>
<span data-ttu-id="26df8-152">Livello SKU della bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="26df8-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="26df8-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26df8-153">-Confirm</span></span>
<span data-ttu-id="26df8-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26df8-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26df8-155">-WhatIf</span></span>
<span data-ttu-id="26df8-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26df8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26df8-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26df8-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26df8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26df8-158">CommonParameters</span></span>
<span data-ttu-id="26df8-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26df8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26df8-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26df8-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26df8-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="26df8-161">INPUTS</span></span>

### <span data-ttu-id="26df8-162">System.String</span><span class="sxs-lookup"><span data-stu-id="26df8-162">System.String</span></span>

### <span data-ttu-id="26df8-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="26df8-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26df8-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="26df8-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="26df8-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="26df8-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="26df8-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="26df8-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="26df8-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="26df8-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="26df8-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="26df8-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="26df8-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="26df8-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="26df8-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="26df8-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="26df8-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26df8-171">OUTPUTS</span></span>

### <span data-ttu-id="26df8-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26df8-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26df8-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="26df8-173">NOTES</span></span>

## <span data-ttu-id="26df8-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26df8-174">RELATED LINKS</span></span>

[<span data-ttu-id="26df8-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="26df8-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="26df8-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26df8-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="26df8-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26df8-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="26df8-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26df8-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
