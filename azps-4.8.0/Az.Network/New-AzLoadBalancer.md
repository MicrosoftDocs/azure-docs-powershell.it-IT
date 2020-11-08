---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 0b51e2b01fd194b0cb400e2d8547f7d7df78f0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189521"
---
# <span data-ttu-id="13eb2-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13eb2-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="13eb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="13eb2-103">Crea un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-103">Creates a load balancer.</span></span>

## <span data-ttu-id="13eb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13eb2-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13eb2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13eb2-105">DESCRIPTION</span></span>
<span data-ttu-id="13eb2-106">Il cmdlet **New-AzLoadBalancer** crea un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="13eb2-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="13eb2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13eb2-107">EXAMPLES</span></span>

### <span data-ttu-id="13eb2-108">Esempio 1: creare un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="13eb2-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="13eb2-109">La distribuzione di un bilanciamento del carico richiede la prima creazione di diversi oggetti e i primi sette comandi illustrano come creare tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="13eb2-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="13eb2-110">L'ottavo comando crea un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13eb2-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="13eb2-111">Il nono e ultimo comando consente di ottenere il nuovo bilanciamento del carico per verificare che sia stato creato correttamente.</span><span class="sxs-lookup"><span data-stu-id="13eb2-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="13eb2-112">Tieni presente che questo esempio Mostra solo come creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="13eb2-113">Devi anche configurarlo usando il cmdlet Add-AzNetworkInterfaceIpConfig per assegnare le NIC a macchine virtuali diverse.</span><span class="sxs-lookup"><span data-stu-id="13eb2-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="13eb2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13eb2-114">PARAMETERS</span></span>

### <span data-ttu-id="13eb2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13eb2-115">-AsJob</span></span>
<span data-ttu-id="13eb2-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="13eb2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13eb2-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13eb2-117">-BackendAddressPool</span></span>
<span data-ttu-id="13eb2-118">Specifica un pool di indirizzi di backend da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13eb2-119">-DefaultProfile</span></span>
<span data-ttu-id="13eb2-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13eb2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13eb2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="13eb2-121">-Force</span></span>
<span data-ttu-id="13eb2-122">Indica che questo cmdlet crea un bilanciamento del carico anche se esiste già un bilanciamento del carico con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="13eb2-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="13eb2-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="13eb2-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="13eb2-124">Specifica un elenco di indirizzi IP front-end da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="13eb2-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="13eb2-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="13eb2-126">-InboundNatRule</span></span>
<span data-ttu-id="13eb2-127">Specifica un elenco di regole NAT (Network Address Translation) in ingresso da associare a un sistema di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="13eb2-128">-LoadBalancingRule</span></span>
<span data-ttu-id="13eb2-129">Specifica un elenco di regole di bilanciamento del carico da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="13eb2-130">-Location</span></span>
<span data-ttu-id="13eb2-131">Specifica l'area geografica in cui creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="13eb2-132">-Name</span></span>
<span data-ttu-id="13eb2-133">Specifica il nome del bilanciamento del carico creato.</span><span class="sxs-lookup"><span data-stu-id="13eb2-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="13eb2-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="13eb2-134">-OutboundRule</span></span>
<span data-ttu-id="13eb2-135">Regole in uscita.</span><span class="sxs-lookup"><span data-stu-id="13eb2-135">The outbound rules.</span></span>

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

### <span data-ttu-id="13eb2-136">-Probe</span><span class="sxs-lookup"><span data-stu-id="13eb2-136">-Probe</span></span>
<span data-ttu-id="13eb2-137">Specifica un elenco di sonde da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-137">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13eb2-138">-ResourceGroupName</span></span>
<span data-ttu-id="13eb2-139">Specifica il nome del gruppo di risorse in cui creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="13eb2-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="13eb2-140">-Sku</span></span>
<span data-ttu-id="13eb2-141">Nome della SKU di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="13eb2-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="13eb2-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="13eb2-142">-Tag</span></span>
<span data-ttu-id="13eb2-143">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="13eb2-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="13eb2-144">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="13eb2-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="13eb2-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13eb2-145">-Confirm</span></span>
<span data-ttu-id="13eb2-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13eb2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13eb2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13eb2-147">-WhatIf</span></span>
<span data-ttu-id="13eb2-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13eb2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13eb2-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13eb2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13eb2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13eb2-150">CommonParameters</span></span>
<span data-ttu-id="13eb2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13eb2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13eb2-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13eb2-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13eb2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13eb2-153">INPUTS</span></span>

### <span data-ttu-id="13eb2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="13eb2-154">System.String</span></span>

### <span data-ttu-id="13eb2-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="13eb2-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="13eb2-156">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="13eb2-156">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="13eb2-157">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="13eb2-157">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="13eb2-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="13eb2-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="13eb2-159">Microsoft. Azure. Commands. Network. Models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="13eb2-159">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="13eb2-160">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="13eb2-160">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="13eb2-161">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="13eb2-161">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="13eb2-162">Microsoft. Azure. Commands. Network. Models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="13eb2-162">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="13eb2-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13eb2-163">OUTPUTS</span></span>

### <span data-ttu-id="13eb2-164">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13eb2-164">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="13eb2-165">Note</span><span class="sxs-lookup"><span data-stu-id="13eb2-165">NOTES</span></span>

## <span data-ttu-id="13eb2-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13eb2-166">RELATED LINKS</span></span>

[<span data-ttu-id="13eb2-167">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="13eb2-167">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="13eb2-168">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13eb2-168">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="13eb2-169">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13eb2-169">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="13eb2-170">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13eb2-170">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
