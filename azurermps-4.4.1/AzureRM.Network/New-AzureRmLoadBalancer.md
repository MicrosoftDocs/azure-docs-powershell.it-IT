---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: 423061d4aeaba16d0edf6bbe122f9fbe3f078218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688010"
---
# <span data-ttu-id="e231d-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e231d-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="e231d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e231d-102">SYNOPSIS</span></span>
<span data-ttu-id="e231d-103">Crea un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e231d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e231d-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e231d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e231d-105">DESCRIPTION</span></span>
<span data-ttu-id="e231d-106">Il cmdlet **New-AzureRmLoadBalancer** crea un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e231d-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="e231d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e231d-107">EXAMPLES</span></span>

### <span data-ttu-id="e231d-108">Esempio 1: creare un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e231d-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e231d-109">La distribuzione di un bilanciamento del carico richiede la prima creazione di diversi oggetti e i primi sette comandi illustrano come creare tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="e231d-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="e231d-110">L'ottavo comando crea un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e231d-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="e231d-111">Il nono e ultimo comando consente di ottenere il nuovo bilanciamento del carico per verificare che sia stato creato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e231d-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="e231d-112">Tieni presente che questo esempio Mostra solo come creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="e231d-113">Devi anche configurarlo usando il cmdlet Add-AzureRmNetworkInterfaceIpConfig per assegnare le NIC a macchine virtuali diverse.</span><span class="sxs-lookup"><span data-stu-id="e231d-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="e231d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e231d-114">PARAMETERS</span></span>

### <span data-ttu-id="e231d-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e231d-115">-BackendAddressPool</span></span>
<span data-ttu-id="e231d-116">Specifica un pool di indirizzi di backend da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-116">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e231d-117">-Force</span></span>
<span data-ttu-id="e231d-118">Indica che questo cmdlet crea un bilanciamento del carico anche se esiste già un bilanciamento del carico con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e231d-118">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="e231d-119">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e231d-119">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e231d-120">Specifica un elenco di indirizzi IP front-end da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-120">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-121">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="e231d-121">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-122">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e231d-122">-InboundNatRule</span></span>
<span data-ttu-id="e231d-123">Specifica un elenco di regole NAT (Network Address Translation) in ingresso da associare a un sistema di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-123">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-124">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="e231d-124">-LoadBalancingRule</span></span>
<span data-ttu-id="e231d-125">Specifica un elenco di regole di bilanciamento del carico da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-125">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e231d-126">-Location</span></span>
<span data-ttu-id="e231d-127">Specifica l'area geografica in cui creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-127">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="e231d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e231d-128">-Name</span></span>
<span data-ttu-id="e231d-129">Specifica il nome del bilanciamento del carico creato.</span><span class="sxs-lookup"><span data-stu-id="e231d-129">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="e231d-130">-Probe</span><span class="sxs-lookup"><span data-stu-id="e231d-130">-Probe</span></span>
<span data-ttu-id="e231d-131">Specifica un elenco di sonde da associare a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-131">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e231d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e231d-133">Specifica il nome del gruppo di risorse in cui creare un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-133">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="e231d-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="e231d-134">-Sku</span></span>
<span data-ttu-id="e231d-135">Nome della SKU di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e231d-135">The load balancer Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e231d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e231d-136">-Tag</span></span>
<span data-ttu-id="e231d-137">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e231d-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e231d-138">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="e231d-138">For example:</span></span>

<span data-ttu-id="e231d-139">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e231d-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e231d-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e231d-140">-Confirm</span></span>
<span data-ttu-id="e231d-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e231d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e231d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e231d-142">-WhatIf</span></span>
<span data-ttu-id="e231d-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e231d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e231d-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e231d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e231d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e231d-145">-DefaultProfile</span></span>
<span data-ttu-id="e231d-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e231d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e231d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e231d-147">CommonParameters</span></span>
<span data-ttu-id="e231d-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e231d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e231d-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e231d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e231d-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e231d-150">INPUTS</span></span>

## <span data-ttu-id="e231d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e231d-151">OUTPUTS</span></span>

### <span data-ttu-id="e231d-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e231d-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e231d-153">Note</span><span class="sxs-lookup"><span data-stu-id="e231d-153">NOTES</span></span>

## <span data-ttu-id="e231d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e231d-154">RELATED LINKS</span></span>

[<span data-ttu-id="e231d-155">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e231d-155">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e231d-156">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e231d-156">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e231d-157">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e231d-157">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="e231d-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e231d-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
