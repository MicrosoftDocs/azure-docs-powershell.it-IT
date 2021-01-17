---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356674"
---
# <span data-ttu-id="2adb0-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2adb0-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="2adb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2adb0-102">SYNOPSIS</span></span>
<span data-ttu-id="2adb0-103">Aggiorna una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2adb0-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="2adb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2adb0-104">SYNTAX</span></span>

### <span data-ttu-id="2adb0-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2adb0-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2adb0-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="2adb0-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2adb0-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2adb0-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2adb0-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2adb0-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2adb0-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2adb0-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2adb0-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2adb0-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2adb0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2adb0-111">DESCRIPTION</span></span>
<span data-ttu-id="2adb0-112">Il cmdlet **set-AzLoadBalancerFrontendIpConfig** aggiorna una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2adb0-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="2adb0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2adb0-113">EXAMPLES</span></span>

### <span data-ttu-id="2adb0-114">Esempio 1: modificare la configurazione IP front-end di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="2adb0-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="2adb0-115">Il primo comando consente di ottenere la subnet virtuale denominata subnet e di archiviarla nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2adb0-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2adb0-116">Il secondo comando ottiene il bilanciamento del carico associato denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="2adb0-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2adb0-117">Il terzo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerFrontendIpConfig, che crea una configurazione IP front-end denominata NewFrontend per $slb.</span><span class="sxs-lookup"><span data-stu-id="2adb0-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="2adb0-118">Il quarto comando passa il bilanciamento del carico in $slb a **set-AzLoadBalancerFrontendIpConfig**, che consente di salvare e aggiornare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="2adb0-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="2adb0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2adb0-119">PARAMETERS</span></span>

### <span data-ttu-id="2adb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adb0-120">-DefaultProfile</span></span>
<span data-ttu-id="2adb0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2adb0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2adb0-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2adb0-122">-LoadBalancer</span></span>
<span data-ttu-id="2adb0-123">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2adb0-123">Specifies a load balancer.</span></span>
<span data-ttu-id="2adb0-124">Questo cmdlet aggiorna una configurazione front-end per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2adb0-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2adb0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2adb0-125">-Name</span></span>
<span data-ttu-id="2adb0-126">Specifica il nome della configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="2adb0-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="2adb0-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2adb0-127">-PrivateIpAddress</span></span>
<span data-ttu-id="2adb0-128">Specifica l'indirizzo IP privato del bilanciamento del carico associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="2adb0-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="2adb0-129">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="2adb0-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="2adb0-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2adb0-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="2adb0-131">La versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="2adb0-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="2adb0-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2adb0-132">-PublicIpAddress</span></span>
<span data-ttu-id="2adb0-133">Specifica l'oggetto **PublicIpAddress** associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="2adb0-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="2adb0-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2adb0-134">-PublicIpAddressId</span></span>
<span data-ttu-id="2adb0-135">Specifica l'ID dell'oggetto **PublicIpAddress** associato alla configurazione IP front-end che questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="2adb0-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2adb0-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2adb0-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="2adb0-137">Specifica l'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="2adb0-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2adb0-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="2adb0-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="2adb0-139">Specifica l'ID dell'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="2adb0-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2adb0-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="2adb0-140">-Subnet</span></span>
<span data-ttu-id="2adb0-141">Specifica l'oggetto **subnet** che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adb0-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2adb0-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2adb0-142">-SubnetId</span></span>
<span data-ttu-id="2adb0-143">Specifica l'ID della subnet che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adb0-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2adb0-144">-Zona</span><span class="sxs-lookup"><span data-stu-id="2adb0-144">-Zone</span></span>
<span data-ttu-id="2adb0-145">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="2adb0-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2adb0-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2adb0-146">-Confirm</span></span>
<span data-ttu-id="2adb0-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adb0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2adb0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2adb0-148">-WhatIf</span></span>
<span data-ttu-id="2adb0-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2adb0-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2adb0-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2adb0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2adb0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adb0-151">CommonParameters</span></span>
<span data-ttu-id="2adb0-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adb0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adb0-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2adb0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adb0-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2adb0-154">INPUTS</span></span>

### <span data-ttu-id="2adb0-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2adb0-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2adb0-156">System. String</span><span class="sxs-lookup"><span data-stu-id="2adb0-156">System.String</span></span>

### <span data-ttu-id="2adb0-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="2adb0-157">System.String[]</span></span>

### <span data-ttu-id="2adb0-158">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2adb0-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="2adb0-159">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2adb0-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2adb0-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2adb0-160">OUTPUTS</span></span>

### <span data-ttu-id="2adb0-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2adb0-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2adb0-162">Note</span><span class="sxs-lookup"><span data-stu-id="2adb0-162">NOTES</span></span>

## <span data-ttu-id="2adb0-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2adb0-163">RELATED LINKS</span></span>

[<span data-ttu-id="2adb0-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2adb0-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2adb0-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2adb0-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2adb0-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2adb0-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2adb0-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2adb0-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="2adb0-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2adb0-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2adb0-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2adb0-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


