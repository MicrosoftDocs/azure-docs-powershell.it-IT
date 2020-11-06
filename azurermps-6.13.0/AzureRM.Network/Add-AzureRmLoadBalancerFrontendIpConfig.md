---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510920"
---
# <span data-ttu-id="301d8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="301d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="301d8-102">SYNOPSIS</span></span>
<span data-ttu-id="301d8-103">Aggiunge una configurazione IP front-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="301d8-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="301d8-104">SYNTAX</span></span>

### <span data-ttu-id="301d8-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="301d8-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301d8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="301d8-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301d8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="301d8-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301d8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="301d8-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301d8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="301d8-109">DESCRIPTION</span></span>
<span data-ttu-id="301d8-110">Il cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** aggiunge una configurazione IP front-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="301d8-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="301d8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="301d8-111">EXAMPLES</span></span>

### <span data-ttu-id="301d8-112">Esempio 1 aggiungere una configurazione IP front-end con un indirizzo IP dinamico</span><span class="sxs-lookup"><span data-stu-id="301d8-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="301d8-113">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="301d8-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="301d8-114">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="301d8-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="301d8-115">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP dinamico privato dalla subnet archiviata nella variabile denominata $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="301d8-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="301d8-116">Esempio 2 aggiunta di una configurazione IP front-end con un indirizzo IP statico</span><span class="sxs-lookup"><span data-stu-id="301d8-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="301d8-117">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="301d8-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="301d8-118">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="301d8-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="301d8-119">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP privato statico dalla subnet archiviata nella variabile denominata $subnet.</span><span class="sxs-lookup"><span data-stu-id="301d8-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="301d8-120">Esempio 3 aggiunta di una configurazione IP front-end con un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="301d8-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="301d8-121">Il primo comando ottiene l'indirizzo IP pubblico di Azure denominato MyPub e archivia il risultato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="301d8-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="301d8-122">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con l'indirizzo IP pubblico archiviato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="301d8-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="301d8-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="301d8-123">PARAMETERS</span></span>

### <span data-ttu-id="301d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301d8-124">-DefaultProfile</span></span>
<span data-ttu-id="301d8-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="301d8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="301d8-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="301d8-126">-LoadBalancer</span></span>
<span data-ttu-id="301d8-127">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="301d8-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="301d8-128">Questo cmdlet aggiunge una configurazione IP front-end al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="301d8-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="301d8-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="301d8-129">-Name</span></span>
<span data-ttu-id="301d8-130">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="301d8-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="301d8-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="301d8-131">-PrivateIpAddress</span></span>
<span data-ttu-id="301d8-132">Specifica l'indirizzo IP privato da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="301d8-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="301d8-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="301d8-133">-PublicIpAddress</span></span>
<span data-ttu-id="301d8-134">Specifica l'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="301d8-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="301d8-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="301d8-135">-PublicIpAddressId</span></span>
<span data-ttu-id="301d8-136">Specifica l'ID dell'indirizzo IP pubblico in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="301d8-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="301d8-137">-Subnet</span><span class="sxs-lookup"><span data-stu-id="301d8-137">-Subnet</span></span>
<span data-ttu-id="301d8-138">Specifica l'oggetto subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="301d8-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="301d8-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="301d8-139">-SubnetId</span></span>
<span data-ttu-id="301d8-140">Specifica l'ID della subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="301d8-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="301d8-141">-Zona</span><span class="sxs-lookup"><span data-stu-id="301d8-141">-Zone</span></span>
<span data-ttu-id="301d8-142">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="301d8-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="301d8-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="301d8-143">-Confirm</span></span>
<span data-ttu-id="301d8-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="301d8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301d8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301d8-145">-WhatIf</span></span>
<span data-ttu-id="301d8-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="301d8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="301d8-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="301d8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301d8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301d8-148">CommonParameters</span></span>
<span data-ttu-id="301d8-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301d8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301d8-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301d8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301d8-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="301d8-151">INPUTS</span></span>

### <span data-ttu-id="301d8-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="301d8-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="301d8-153">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="301d8-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="301d8-154">System. Collections. Generic. List \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="301d8-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="301d8-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="301d8-155">OUTPUTS</span></span>

### <span data-ttu-id="301d8-156">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="301d8-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="301d8-157">Note</span><span class="sxs-lookup"><span data-stu-id="301d8-157">NOTES</span></span>

## <span data-ttu-id="301d8-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="301d8-158">RELATED LINKS</span></span>

[<span data-ttu-id="301d8-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="301d8-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="301d8-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="301d8-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="301d8-162">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="301d8-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="301d8-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="301d8-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


