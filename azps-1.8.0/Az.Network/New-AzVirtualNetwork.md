---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 0b839d0392153fc21b9d57c15a823158827bdc72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678222"
---
# <span data-ttu-id="9449f-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9449f-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="9449f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9449f-102">SYNOPSIS</span></span>
<span data-ttu-id="9449f-103">Crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-103">Creates a virtual network.</span></span>

## <span data-ttu-id="9449f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9449f-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-Tag <Hashtable>] [-EnableDdosProtection]
 [-DdosProtectionPlanId <String>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9449f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9449f-105">DESCRIPTION</span></span>
<span data-ttu-id="9449f-106">Il cmdlet **New-AzVirtualNetwork** crea una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9449f-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="9449f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9449f-107">EXAMPLES</span></span>

### <span data-ttu-id="9449f-108">1: creare una rete virtuale con due subnet</span><span class="sxs-lookup"><span data-stu-id="9449f-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="9449f-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="9449f-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="9449f-110">Viene innanzitutto creato un nuovo gruppo di risorse nell'area centrale.</span><span class="sxs-lookup"><span data-stu-id="9449f-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="9449f-111">L'esempio crea quindi rappresentazioni in memoria di due sottoreti.</span><span class="sxs-lookup"><span data-stu-id="9449f-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="9449f-112">Il cmdlet New-AzVirtualNetworkSubnetConfig non creerà alcuna subnet sul lato server.</span><span class="sxs-lookup"><span data-stu-id="9449f-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="9449f-113">Esiste una subnet denominata frontendSubnet e una subnet denominata backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="9449f-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="9449f-114">Il cmdlet New-AzVirtualNetwork crea quindi una rete virtuale usando la notazione CIDR 10.0.0.0/16 come prefisso dell'indirizzo e due sottoreti.</span><span class="sxs-lookup"><span data-stu-id="9449f-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="9449f-115">2: creare una rete virtuale con le impostazioni DNS</span><span class="sxs-lookup"><span data-stu-id="9449f-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="9449f-116">Questo esempio crea una rete virtuale con due subnet e due server DNS.</span><span class="sxs-lookup"><span data-stu-id="9449f-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="9449f-117">L'effetto di specificare i server DNS nella rete virtuale è che le NIC/VM distribuite in questa rete virtuale ereditano questi server DNS come predefiniti.</span><span class="sxs-lookup"><span data-stu-id="9449f-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="9449f-118">Queste impostazioni predefinite possono essere sovrascritte per NIC tramite un'impostazione a livello di NIC.</span><span class="sxs-lookup"><span data-stu-id="9449f-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="9449f-119">Se non sono specificati server DNS in un VNET e nessun server DNS sulle schede di nic, vengono usati i server DNS di Azure predefiniti per la risoluzione DNS.</span><span class="sxs-lookup"><span data-stu-id="9449f-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="9449f-120">3: creare una rete virtuale con una subnet che fa riferimento a un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="9449f-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="9449f-121">Questo esempio crea una rete virtuale con subnet che fanno riferimento a un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9449f-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="9449f-122">In primo luogo, nell'esempio viene creato un gruppo di risorse come contenitore per le risorse che verranno create.</span><span class="sxs-lookup"><span data-stu-id="9449f-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="9449f-123">Viene quindi creato un gruppo di sicurezza di rete che consente l'accesso RDP in ingresso, ma impone in caso contrario le regole predefinite del gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9449f-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="9449f-124">Il cmdlet New-AzVirtualNetworkSubnetConfig crea quindi rappresentazioni in memoria di due subnet che fanno riferimento al gruppo di sicurezza di rete creato.</span><span class="sxs-lookup"><span data-stu-id="9449f-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="9449f-125">Il comando New-AzVirtualNetwork crea quindi la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="9449f-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9449f-126">PARAMETERS</span></span>

### <span data-ttu-id="9449f-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9449f-127">-AddressPrefix</span></span>
<span data-ttu-id="9449f-128">Specifica un intervallo di indirizzi IP per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="9449f-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9449f-129">-AsJob</span></span>
<span data-ttu-id="9449f-130">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9449f-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9449f-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="9449f-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="9449f-132">Riferimento alla risorsa del piano di protezione DDoS associata alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="9449f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9449f-133">-DefaultProfile</span></span>
<span data-ttu-id="9449f-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9449f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9449f-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="9449f-135">-DnsServer</span></span>
<span data-ttu-id="9449f-136">Specifica il server DNS per una subnet.</span><span class="sxs-lookup"><span data-stu-id="9449f-136">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="9449f-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="9449f-137">-EnableDdosProtection</span></span>
<span data-ttu-id="9449f-138">Parametro switch che rappresenta se è abilitata o meno la protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="9449f-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="9449f-139">-Force</span><span class="sxs-lookup"><span data-stu-id="9449f-139">-Force</span></span>
<span data-ttu-id="9449f-140">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9449f-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9449f-141">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9449f-141">-Location</span></span>
<span data-ttu-id="9449f-142">Specifica l'area geografica della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-142">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="9449f-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="9449f-143">-Name</span></span>
<span data-ttu-id="9449f-144">Specifica il nome della rete virtuale creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9449f-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9449f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9449f-145">-ResourceGroupName</span></span>
<span data-ttu-id="9449f-146">Specifica il nome di un gruppo di risorse che contiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-146">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="9449f-147">-Subnet</span><span class="sxs-lookup"><span data-stu-id="9449f-147">-Subnet</span></span>
<span data-ttu-id="9449f-148">Specifica un elenco di subnet da associare alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9449f-148">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="9449f-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="9449f-149">-Tag</span></span>
<span data-ttu-id="9449f-150">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9449f-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9449f-151">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9449f-151">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9449f-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9449f-152">-Confirm</span></span>
<span data-ttu-id="9449f-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9449f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9449f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9449f-154">-WhatIf</span></span>
<span data-ttu-id="9449f-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9449f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9449f-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9449f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9449f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9449f-157">CommonParameters</span></span>
<span data-ttu-id="9449f-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9449f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9449f-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9449f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9449f-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9449f-160">INPUTS</span></span>

### <span data-ttu-id="9449f-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9449f-161">System.String</span></span>

### <span data-ttu-id="9449f-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="9449f-162">System.String[]</span></span>

### <span data-ttu-id="9449f-163">Microsoft. Azure. Commands. Network. Models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="9449f-163">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="9449f-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9449f-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9449f-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9449f-165">OUTPUTS</span></span>

### <span data-ttu-id="9449f-166">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9449f-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9449f-167">Note</span><span class="sxs-lookup"><span data-stu-id="9449f-167">NOTES</span></span>

## <span data-ttu-id="9449f-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9449f-168">RELATED LINKS</span></span>

[<span data-ttu-id="9449f-169">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9449f-169">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9449f-170">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9449f-170">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="9449f-171">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9449f-171">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="9449f-172">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9449f-172">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
