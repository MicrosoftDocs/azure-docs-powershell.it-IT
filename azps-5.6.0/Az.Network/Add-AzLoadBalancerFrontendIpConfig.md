---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d68c4329eee7c75889db48fb55772bf903417170
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952301"
---
# <span data-ttu-id="3987b-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="3987b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3987b-102">SYNOPSIS</span></span>
<span data-ttu-id="3987b-103">Aggiunge una configurazione IP front-end a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3987b-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="3987b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3987b-104">SYNTAX</span></span>

### <span data-ttu-id="3987b-105">SetByResourceSubnet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3987b-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3987b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="3987b-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3987b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3987b-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3987b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3987b-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3987b-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3987b-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3987b-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3987b-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3987b-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3987b-111">DESCRIPTION</span></span>
<span data-ttu-id="3987b-112">Il cmdlet **Add-AzLoadBalancerFrontendIpConfig aggiunge** una configurazione IP front-end a una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="3987b-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="3987b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3987b-113">EXAMPLES</span></span>

### <span data-ttu-id="3987b-114">Esempio 1: Aggiungere una configurazione IP front-end con un indirizzo IP dinamico</span><span class="sxs-lookup"><span data-stu-id="3987b-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="3987b-115">Il primo comando recupera la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="3987b-116">Il comando archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="3987b-117">Il secondo comando ottiene la bilanciamento del carico denominata MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end alla bilanciamento del carico con un indirizzo IP privato dinamico dalla subnet archiviata nella variabile $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="3987b-118">Esempio 2: Aggiungere una configurazione IP front-end con un indirizzo IP statico</span><span class="sxs-lookup"><span data-stu-id="3987b-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="3987b-119">Il primo comando recupera la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="3987b-120">Il comando archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="3987b-121">Il secondo comando ottiene la bilanciamento del carico denominata MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end alla bilanciamento del carico con un indirizzo IP privato statico dalla subnet archiviata nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3987b-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="3987b-122">Esempio 3 Aggiungere una configurazione IP front-end con un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="3987b-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="3987b-123">Il primo comando ottiene l'indirizzo IP pubblico di Azure denominato MyPub e archivia il risultato nella variabile $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3987b-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="3987b-124">Il secondo comando recupera la bilanciamento del carico denominata MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end alla bilanciamento del carico con l'indirizzo IP pubblico archiviato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3987b-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="3987b-125">Esempio 4 Aggiungere una configurazione IP front-end con un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="3987b-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="3987b-126">Il primo comando ottiene il prefisso IP pubblico di Azure denominato PrefissoPub e archivia il risultato nella variabile $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3987b-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="3987b-127">Il secondo comando recupera la bilanciamento del carico denominata MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end alla bilanciamento del carico con prefisso IP pubblico archiviato nella variabile denominata $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3987b-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="3987b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3987b-128">PARAMETERS</span></span>

### <span data-ttu-id="3987b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3987b-129">-DefaultProfile</span></span>
<span data-ttu-id="3987b-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3987b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3987b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3987b-131">-LoadBalancer</span></span>
<span data-ttu-id="3987b-132">Specifica un **oggetto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="3987b-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="3987b-133">Questo cmdlet aggiunge una configurazione IP front-end alla bilanciamento del carico specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3987b-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="3987b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3987b-134">-Name</span></span>
<span data-ttu-id="3987b-135">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3987b-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="3987b-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3987b-136">-PrivateIpAddress</span></span>
<span data-ttu-id="3987b-137">Specifica l'indirizzo IP privato da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3987b-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="3987b-139">Versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="3987b-139">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3987b-140">-PublicIpAddress</span></span>
<span data-ttu-id="3987b-141">Specifica l'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3987b-142">-PublicIpAddressId</span></span>
<span data-ttu-id="3987b-143">Specifica l'ID dell'indirizzo IP pubblico in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3987b-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="3987b-145">Specifica l'oggetto prefisso dell'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="3987b-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="3987b-147">Specifica l'ID dell'oggetto prefisso dell'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-148">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3987b-148">-Subnet</span></span>
<span data-ttu-id="3987b-149">Specifica l'oggetto subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3987b-150">-SubnetId</span></span>
<span data-ttu-id="3987b-151">Specifica l'ID della subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3987b-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3987b-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="3987b-152">-Zone</span></span>
<span data-ttu-id="3987b-153">Elenco di aree di disponibilità che denota l'indirizzo IP allocato per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3987b-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="3987b-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3987b-154">-Confirm</span></span>
<span data-ttu-id="3987b-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3987b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3987b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3987b-156">-WhatIf</span></span>
<span data-ttu-id="3987b-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3987b-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3987b-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3987b-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3987b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3987b-159">CommonParameters</span></span>
<span data-ttu-id="3987b-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3987b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3987b-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3987b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3987b-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="3987b-162">INPUTS</span></span>

### <span data-ttu-id="3987b-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3987b-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3987b-164">System.String</span><span class="sxs-lookup"><span data-stu-id="3987b-164">System.String</span></span>

### <span data-ttu-id="3987b-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3987b-165">System.String[]</span></span>

### <span data-ttu-id="3987b-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3987b-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="3987b-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3987b-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="3987b-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3987b-168">OUTPUTS</span></span>

### <span data-ttu-id="3987b-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3987b-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3987b-170">NOTE</span><span class="sxs-lookup"><span data-stu-id="3987b-170">NOTES</span></span>

## <span data-ttu-id="3987b-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3987b-171">RELATED LINKS</span></span>

[<span data-ttu-id="3987b-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3987b-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3987b-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="3987b-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3987b-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3987b-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3987b-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3987b-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


