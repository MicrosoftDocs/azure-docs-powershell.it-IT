---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300678"
---
# <span data-ttu-id="b10af-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b10af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b10af-102">SYNOPSIS</span></span>
<span data-ttu-id="b10af-103">Aggiunge una configurazione IP front-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b10af-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="b10af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b10af-104">SYNTAX</span></span>

### <span data-ttu-id="b10af-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b10af-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b10af-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="b10af-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b10af-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b10af-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b10af-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b10af-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b10af-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b10af-109">DESCRIPTION</span></span>
<span data-ttu-id="b10af-110">Il cmdlet **Add-AzLoadBalancerFrontendIpConfig** aggiunge una configurazione IP front-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="b10af-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b10af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b10af-111">EXAMPLES</span></span>

### <span data-ttu-id="b10af-112">Esempio 1 aggiungere una configurazione IP front-end con un indirizzo IP dinamico</span><span class="sxs-lookup"><span data-stu-id="b10af-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="b10af-113">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="b10af-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b10af-114">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b10af-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b10af-115">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP dinamico privato dalla subnet archiviata nella variabile denominata $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="b10af-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="b10af-116">Esempio 2 aggiunta di una configurazione IP front-end con un indirizzo IP statico</span><span class="sxs-lookup"><span data-stu-id="b10af-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="b10af-117">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="b10af-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b10af-118">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b10af-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b10af-119">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP privato statico dalla subnet archiviata nella variabile denominata $subnet.</span><span class="sxs-lookup"><span data-stu-id="b10af-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="b10af-120">Esempio 3 aggiunta di una configurazione IP front-end con un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="b10af-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="b10af-121">Il primo comando ottiene l'indirizzo IP pubblico di Azure denominato MyPub e archivia il risultato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b10af-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="b10af-122">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con l'indirizzo IP pubblico archiviato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b10af-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="b10af-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b10af-123">PARAMETERS</span></span>

### <span data-ttu-id="b10af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10af-124">-DefaultProfile</span></span>
<span data-ttu-id="b10af-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b10af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b10af-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10af-126">-LoadBalancer</span></span>
<span data-ttu-id="b10af-127">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="b10af-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b10af-128">Questo cmdlet aggiunge una configurazione IP front-end al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b10af-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b10af-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b10af-129">-Name</span></span>
<span data-ttu-id="b10af-130">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b10af-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="b10af-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b10af-131">-PrivateIpAddress</span></span>
<span data-ttu-id="b10af-132">Specifica l'indirizzo IP privato da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b10af-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b10af-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b10af-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b10af-134">La versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="b10af-134">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="b10af-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b10af-135">-PublicIpAddress</span></span>
<span data-ttu-id="b10af-136">Specifica l'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b10af-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b10af-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b10af-137">-PublicIpAddressId</span></span>
<span data-ttu-id="b10af-138">Specifica l'ID dell'indirizzo IP pubblico in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b10af-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b10af-139">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b10af-139">-Subnet</span></span>
<span data-ttu-id="b10af-140">Specifica l'oggetto subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b10af-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b10af-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b10af-141">-SubnetId</span></span>
<span data-ttu-id="b10af-142">Specifica l'ID della subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b10af-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b10af-143">-Zona</span><span class="sxs-lookup"><span data-stu-id="b10af-143">-Zone</span></span>
<span data-ttu-id="b10af-144">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="b10af-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b10af-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b10af-145">-Confirm</span></span>
<span data-ttu-id="b10af-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b10af-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10af-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10af-147">-WhatIf</span></span>
<span data-ttu-id="b10af-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b10af-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b10af-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b10af-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10af-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10af-150">CommonParameters</span></span>
<span data-ttu-id="b10af-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b10af-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10af-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b10af-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10af-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b10af-153">INPUTS</span></span>

### <span data-ttu-id="b10af-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10af-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b10af-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b10af-155">System.String</span></span>

### <span data-ttu-id="b10af-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="b10af-156">System.String[]</span></span>

### <span data-ttu-id="b10af-157">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b10af-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b10af-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b10af-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b10af-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b10af-159">OUTPUTS</span></span>

### <span data-ttu-id="b10af-160">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10af-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b10af-161">Note</span><span class="sxs-lookup"><span data-stu-id="b10af-161">NOTES</span></span>

## <span data-ttu-id="b10af-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b10af-162">RELATED LINKS</span></span>

[<span data-ttu-id="b10af-163">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b10af-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10af-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b10af-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b10af-166">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b10af-167">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b10af-168">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b10af-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


