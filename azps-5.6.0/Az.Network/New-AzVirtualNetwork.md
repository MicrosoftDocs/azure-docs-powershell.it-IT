---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9608dfd5a780006d2ab050a1ca2e85ee26949f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961726"
---
# <span data-ttu-id="c0340-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0340-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="c0340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0340-102">SYNOPSIS</span></span>
<span data-ttu-id="c0340-103">Crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-103">Creates a virtual network.</span></span>

## <span data-ttu-id="c0340-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0340-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0340-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0340-105">DESCRIPTION</span></span>
<span data-ttu-id="c0340-106">Il cmdlet **New-AzVirtualNetwork** crea una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0340-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="c0340-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0340-107">EXAMPLES</span></span>

### <span data-ttu-id="c0340-108">Esempio 1: Creare una rete virtuale con due subnet</span><span class="sxs-lookup"><span data-stu-id="c0340-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c0340-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="c0340-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="c0340-110">Prima di tutto, viene creato un nuovo gruppo di risorse nell'area centrale.</span><span class="sxs-lookup"><span data-stu-id="c0340-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="c0340-111">L'esempio crea quindi rappresentazioni in memoria di due subnet.</span><span class="sxs-lookup"><span data-stu-id="c0340-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="c0340-112">Il New-AzVirtualNetworkSubnetConfig cmdlet non creerà alcuna subnet sul lato server.</span><span class="sxs-lookup"><span data-stu-id="c0340-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="c0340-113">Esistono una subnet denominata FrontendSubnet e una denominata BackendSubnet.</span><span class="sxs-lookup"><span data-stu-id="c0340-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="c0340-114">Il cmdlet New-AzVirtualNetwork quindi crea una rete virtuale usando il codice errore CIDR 10.0.0.0/16 come prefisso dell'indirizzo e due subnet.</span><span class="sxs-lookup"><span data-stu-id="c0340-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="c0340-115">Esempio 2: Creare una rete virtuale con impostazioni DNS</span><span class="sxs-lookup"><span data-stu-id="c0340-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="c0340-116">Questo esempio crea una rete virtuale con due subnet e due server DNS.</span><span class="sxs-lookup"><span data-stu-id="c0340-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="c0340-117">L'effetto della specifica dei server DNS nella rete virtuale è che le schede di rete/vm distribuite in questa rete virtuale ereditano questi server DNS come predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c0340-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="c0340-118">Queste impostazioni predefinite possono essere sovrascritte per nic tramite un'impostazione a livello di NIC.</span><span class="sxs-lookup"><span data-stu-id="c0340-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="c0340-119">Se in una rete VNET non sono specificati server DNS e non sono presenti server DNS nelle schede di rete, per la risoluzione DNS vengono usati i server DNS di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c0340-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="c0340-120">Esempio 3: Creare una rete virtuale con una subnet che fa riferimento a un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="c0340-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c0340-121">Questo esempio crea una rete virtuale con subnet che fanno riferimento a un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c0340-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="c0340-122">Prima di tutto, nell'esempio viene creato un gruppo di risorse come contenitore per le risorse che verranno create.</span><span class="sxs-lookup"><span data-stu-id="c0340-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="c0340-123">Viene quindi creato un gruppo di sicurezza di rete che consente l'accesso RDP in ingresso, ma in caso contrario applica le regole predefinite del gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c0340-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="c0340-124">Il New-AzVirtualNetworkSubnetConfig crea quindi rappresentazioni in memoria di due subnet che fanno entrambi riferimento al gruppo di sicurezza di rete creato.</span><span class="sxs-lookup"><span data-stu-id="c0340-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="c0340-125">Il New-AzVirtualNetwork crea quindi la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="c0340-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0340-126">PARAMETERS</span></span>

### <span data-ttu-id="c0340-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c0340-127">-AddressPrefix</span></span>
<span data-ttu-id="c0340-128">Specifica un intervallo di indirizzi IP per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0340-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0340-129">-AsJob</span></span>
<span data-ttu-id="c0340-130">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c0340-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0340-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="c0340-131">-BgpCommunity</span></span>
<span data-ttu-id="c0340-132">Community BGP annunciata su ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c0340-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="c0340-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="c0340-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="c0340-134">Riferimento alla risorsa del piano di protezione DDoS associata alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="c0340-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0340-135">-DefaultProfile</span></span>
<span data-ttu-id="c0340-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0340-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0340-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="c0340-137">-DnsServer</span></span>
<span data-ttu-id="c0340-138">Specifica il server DNS per una subnet.</span><span class="sxs-lookup"><span data-stu-id="c0340-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0340-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="c0340-139">-EnableDdosProtection</span></span>
<span data-ttu-id="c0340-140">Parametro switch che rappresenta se la protezione DDoS è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="c0340-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0340-141">-Force</span><span class="sxs-lookup"><span data-stu-id="c0340-141">-Force</span></span>
<span data-ttu-id="c0340-142">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="c0340-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0340-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c0340-143">-IpAllocation</span></span>
<span data-ttu-id="c0340-144">Specifica IpAllocations per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0340-145">-Location</span><span class="sxs-lookup"><span data-stu-id="c0340-145">-Location</span></span>
<span data-ttu-id="c0340-146">Specifica l'area geografica per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="c0340-147">-Name</span><span class="sxs-lookup"><span data-stu-id="c0340-147">-Name</span></span>
<span data-ttu-id="c0340-148">Specifica il nome della rete virtuale creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0340-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c0340-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0340-149">-ResourceGroupName</span></span>
<span data-ttu-id="c0340-150">Specifica il nome di un gruppo di risorse che deve contenere la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="c0340-151">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c0340-151">-Subnet</span></span>
<span data-ttu-id="c0340-152">Specifica un elenco di subnet da associare alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0340-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0340-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0340-153">-Tag</span></span>
<span data-ttu-id="c0340-154">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c0340-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c0340-155">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c0340-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c0340-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0340-156">-Confirm</span></span>
<span data-ttu-id="c0340-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0340-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0340-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0340-158">-WhatIf</span></span>
<span data-ttu-id="c0340-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0340-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0340-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0340-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0340-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0340-161">CommonParameters</span></span>
<span data-ttu-id="c0340-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0340-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0340-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0340-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0340-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0340-164">INPUTS</span></span>

### <span data-ttu-id="c0340-165">System.String</span><span class="sxs-lookup"><span data-stu-id="c0340-165">System.String</span></span>

### <span data-ttu-id="c0340-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c0340-166">System.String[]</span></span>

### <span data-ttu-id="c0340-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="c0340-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="c0340-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0340-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0340-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0340-169">OUTPUTS</span></span>

### <span data-ttu-id="c0340-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0340-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c0340-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0340-171">NOTES</span></span>

## <span data-ttu-id="c0340-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0340-172">RELATED LINKS</span></span>

[<span data-ttu-id="c0340-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0340-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="c0340-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0340-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="c0340-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c0340-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="c0340-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c0340-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
