---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 9c52a5f234b374612b07d53b21ac9409a45cc35a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686609"
---
# <span data-ttu-id="6af9e-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6af9e-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="6af9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6af9e-102">SYNOPSIS</span></span>
<span data-ttu-id="6af9e-103">Crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6af9e-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-EnableVmProtection] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af9e-105">DESCRIPTION</span></span>
<span data-ttu-id="6af9e-106">Il cmdlet **New-AzureRmVirtualNetwork** crea una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6af9e-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="6af9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6af9e-107">EXAMPLES</span></span>

### <span data-ttu-id="6af9e-108">1: creare una rete virtuale con due subnet</span><span class="sxs-lookup"><span data-stu-id="6af9e-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="6af9e-109">Questo esempio crea una rete virtuale con due subnet.</span><span class="sxs-lookup"><span data-stu-id="6af9e-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="6af9e-110">Viene innanzitutto creato un nuovo gruppo di risorse nell'area centrale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="6af9e-111">L'esempio crea quindi rappresentazioni in memoria di due sottoreti.</span><span class="sxs-lookup"><span data-stu-id="6af9e-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="6af9e-112">Il cmdlet New-AzureRmVirtualNetworkSubnetConfig non creerà alcuna subnet sul lato server.</span><span class="sxs-lookup"><span data-stu-id="6af9e-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="6af9e-113">Esiste una subnet denominata frontendSubnet e una subnet denominata backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="6af9e-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="6af9e-114">Il cmdlet New-AzureRmVirtualNetwork crea quindi una rete virtuale usando la notazione CIDR 10.0.0.0/16 come prefisso dell'indirizzo e due sottoreti.</span><span class="sxs-lookup"><span data-stu-id="6af9e-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="6af9e-115">2: creare una rete virtuale con le impostazioni DNS</span><span class="sxs-lookup"><span data-stu-id="6af9e-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="6af9e-116">Questo esempio crea una rete virtuale con due subnet e due server DNS.</span><span class="sxs-lookup"><span data-stu-id="6af9e-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="6af9e-117">L'effetto di specificare i server DNS nella rete virtuale è che le NIC/VM distribuite in questa rete virtuale ereditano questi server DNS come predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6af9e-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="6af9e-118">Queste impostazioni predefinite possono essere sovrascritte per NIC tramite un'impostazione a livello di NIC.</span><span class="sxs-lookup"><span data-stu-id="6af9e-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="6af9e-119">Se non sono specificati server DNS in un VNET e nessun server DNS sulle schede di nic, vengono usati i server DNS di Azure predefiniti per la risoluzione DNS.</span><span class="sxs-lookup"><span data-stu-id="6af9e-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="6af9e-120">3: creare una rete virtuale con una subnet che fa riferimento a un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="6af9e-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="6af9e-121">Questo esempio crea una rete virtuale con subnet che fanno riferimento a un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="6af9e-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="6af9e-122">In primo luogo, nell'esempio viene creato un gruppo di risorse come contenitore per le risorse che verranno create.</span><span class="sxs-lookup"><span data-stu-id="6af9e-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="6af9e-123">Viene quindi creato un gruppo di sicurezza di rete che consente l'accesso RDP in ingresso, ma impone in caso contrario le regole predefinite del gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="6af9e-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="6af9e-124">Il cmdlet New-AzureRmVirtualNetworkSubnetConfig crea quindi rappresentazioni in memoria di due subnet che fanno riferimento al gruppo di sicurezza di rete creato.</span><span class="sxs-lookup"><span data-stu-id="6af9e-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="6af9e-125">Il comando New-AzureRmVirtualNetwork crea quindi la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="6af9e-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6af9e-126">PARAMETERS</span></span>

### <span data-ttu-id="6af9e-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6af9e-127">-AddressPrefix</span></span>
<span data-ttu-id="6af9e-128">Specifica un intervallo di indirizzi IP per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af9e-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6af9e-129">-AsJob</span></span>
<span data-ttu-id="6af9e-130">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6af9e-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6af9e-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="6af9e-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="6af9e-132">Riferimento alla risorsa del piano di protezione DDoS associata alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="6af9e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af9e-133">-DefaultProfile</span></span>
<span data-ttu-id="6af9e-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6af9e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6af9e-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="6af9e-135">-DnsServer</span></span>
<span data-ttu-id="6af9e-136">Specifica il server DNS per una subnet.</span><span class="sxs-lookup"><span data-stu-id="6af9e-136">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af9e-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="6af9e-137">-EnableDdosProtection</span></span>
<span data-ttu-id="6af9e-138">Parametro switch che rappresenta se è abilitata o meno la protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="6af9e-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="6af9e-139">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="6af9e-139">-EnableVmProtection</span></span>
<span data-ttu-id="6af9e-140">Parametro switch che rappresenta se la protezione VM è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="6af9e-140">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af9e-141">-Force</span><span class="sxs-lookup"><span data-stu-id="6af9e-141">-Force</span></span>
<span data-ttu-id="6af9e-142">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6af9e-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6af9e-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6af9e-143">-Location</span></span>
<span data-ttu-id="6af9e-144">Specifica l'area geografica della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="6af9e-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="6af9e-145">-Name</span></span>
<span data-ttu-id="6af9e-146">Specifica il nome della rete virtuale creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af9e-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6af9e-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af9e-147">-ResourceGroupName</span></span>
<span data-ttu-id="6af9e-148">Specifica il nome di un gruppo di risorse che contiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="6af9e-149">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6af9e-149">-Subnet</span></span>
<span data-ttu-id="6af9e-150">Specifica un elenco di subnet da associare alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af9e-150">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af9e-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="6af9e-151">-Tag</span></span>
<span data-ttu-id="6af9e-152">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6af9e-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6af9e-153">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6af9e-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6af9e-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6af9e-154">-Confirm</span></span>
<span data-ttu-id="6af9e-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af9e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af9e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af9e-156">-WhatIf</span></span>
<span data-ttu-id="6af9e-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af9e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af9e-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af9e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af9e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af9e-159">CommonParameters</span></span>
<span data-ttu-id="6af9e-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af9e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af9e-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af9e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af9e-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6af9e-162">INPUTS</span></span>

### <span data-ttu-id="6af9e-163">System. String</span><span class="sxs-lookup"><span data-stu-id="6af9e-163">System.String</span></span>

### <span data-ttu-id="6af9e-164">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6af9e-164">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6af9e-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSSubnet, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6af9e-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSubnet, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6af9e-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6af9e-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6af9e-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6af9e-167">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6af9e-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6af9e-168">OUTPUTS</span></span>

### <span data-ttu-id="6af9e-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6af9e-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6af9e-170">Note</span><span class="sxs-lookup"><span data-stu-id="6af9e-170">NOTES</span></span>

## <span data-ttu-id="6af9e-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6af9e-171">RELATED LINKS</span></span>

[<span data-ttu-id="6af9e-172">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6af9e-172">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6af9e-173">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6af9e-173">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6af9e-174">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6af9e-174">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6af9e-175">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6af9e-175">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)
