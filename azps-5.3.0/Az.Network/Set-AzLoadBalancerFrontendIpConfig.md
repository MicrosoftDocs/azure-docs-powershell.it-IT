---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488894"
---
# <span data-ttu-id="f118f-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f118f-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f118f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f118f-102">SYNOPSIS</span></span>
<span data-ttu-id="f118f-103">Aggiorna una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f118f-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="f118f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f118f-104">SYNTAX</span></span>

### <span data-ttu-id="f118f-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f118f-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f118f-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f118f-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f118f-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f118f-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f118f-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f118f-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f118f-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f118f-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f118f-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f118f-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f118f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f118f-111">DESCRIPTION</span></span>
<span data-ttu-id="f118f-112">Il cmdlet **set-AzLoadBalancerFrontendIpConfig** aggiorna una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f118f-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="f118f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f118f-113">EXAMPLES</span></span>

### <span data-ttu-id="f118f-114">Esempio 1: modificare la configurazione IP front-end di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="f118f-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="f118f-115">Il primo comando consente di ottenere la subnet virtuale denominata subnet e di archiviarla nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f118f-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f118f-116">Il secondo comando ottiene il bilanciamento del carico associato denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="f118f-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f118f-117">Il terzo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerFrontendIpConfig, che crea una configurazione IP front-end denominata NewFrontend per $slb.</span><span class="sxs-lookup"><span data-stu-id="f118f-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="f118f-118">Il quarto comando passa il bilanciamento del carico in $slb a **set-AzLoadBalancerFrontendIpConfig**, che consente di salvare e aggiornare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="f118f-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="f118f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f118f-119">PARAMETERS</span></span>

### <span data-ttu-id="f118f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f118f-120">-DefaultProfile</span></span>
<span data-ttu-id="f118f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f118f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f118f-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f118f-122">-LoadBalancer</span></span>
<span data-ttu-id="f118f-123">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f118f-123">Specifies a load balancer.</span></span>
<span data-ttu-id="f118f-124">Questo cmdlet aggiorna una configurazione front-end per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f118f-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f118f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f118f-125">-Name</span></span>
<span data-ttu-id="f118f-126">Specifica il nome della configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="f118f-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f118f-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f118f-127">-PrivateIpAddress</span></span>
<span data-ttu-id="f118f-128">Specifica l'indirizzo IP privato del bilanciamento del carico associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="f118f-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="f118f-129">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="f118f-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="f118f-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f118f-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f118f-131">La versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f118f-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="f118f-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f118f-132">-PublicIpAddress</span></span>
<span data-ttu-id="f118f-133">Specifica l'oggetto **PublicIpAddress** associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="f118f-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f118f-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f118f-134">-PublicIpAddressId</span></span>
<span data-ttu-id="f118f-135">Specifica l'ID dell'oggetto **PublicIpAddress** associato alla configurazione IP front-end che questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="f118f-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f118f-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f118f-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="f118f-137">Specifica l'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="f118f-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f118f-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="f118f-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="f118f-139">Specifica l'ID dell'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="f118f-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f118f-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f118f-140">-Subnet</span></span>
<span data-ttu-id="f118f-141">Specifica l'oggetto **subnet** che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f118f-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f118f-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f118f-142">-SubnetId</span></span>
<span data-ttu-id="f118f-143">Specifica l'ID della subnet che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f118f-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f118f-144">-Zona</span><span class="sxs-lookup"><span data-stu-id="f118f-144">-Zone</span></span>
<span data-ttu-id="f118f-145">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="f118f-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f118f-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f118f-146">-Confirm</span></span>
<span data-ttu-id="f118f-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f118f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f118f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f118f-148">-WhatIf</span></span>
<span data-ttu-id="f118f-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f118f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f118f-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f118f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f118f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f118f-151">CommonParameters</span></span>
<span data-ttu-id="f118f-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f118f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f118f-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f118f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f118f-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f118f-154">INPUTS</span></span>

### <span data-ttu-id="f118f-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f118f-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f118f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f118f-156">System.String</span></span>

### <span data-ttu-id="f118f-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="f118f-157">System.String[]</span></span>

### <span data-ttu-id="f118f-158">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f118f-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f118f-159">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f118f-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f118f-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f118f-160">OUTPUTS</span></span>

### <span data-ttu-id="f118f-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f118f-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f118f-162">Note</span><span class="sxs-lookup"><span data-stu-id="f118f-162">NOTES</span></span>

## <span data-ttu-id="f118f-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f118f-163">RELATED LINKS</span></span>

[<span data-ttu-id="f118f-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f118f-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f118f-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f118f-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f118f-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f118f-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f118f-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f118f-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f118f-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f118f-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f118f-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f118f-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


