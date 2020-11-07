---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860985"
---
# <span data-ttu-id="8216e-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8216e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8216e-102">SYNOPSIS</span></span>
<span data-ttu-id="8216e-103">Aggiunge una configurazione IP front-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8216e-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="8216e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8216e-104">SYNTAX</span></span>

### <span data-ttu-id="8216e-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="8216e-105">SetByResourceSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8216e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="8216e-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8216e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8216e-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8216e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8216e-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8216e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8216e-109">DESCRIPTION</span></span>
<span data-ttu-id="8216e-110">Il cmdlet **Add-AzLoadBalancerFrontendIpConifg** aggiunge una configurazione IP front-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="8216e-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="8216e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8216e-111">EXAMPLES</span></span>

### <span data-ttu-id="8216e-112">Esempio 1 aggiungere una configurazione IP front-end con un indirizzo IP dinamico</span><span class="sxs-lookup"><span data-stu-id="8216e-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="8216e-113">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="8216e-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="8216e-114">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8216e-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="8216e-115">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP dinamico privato dalla subnet archiviata nella variabile denominata $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="8216e-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="8216e-116">Esempio 2 aggiunta di una configurazione IP front-end con un indirizzo IP statico</span><span class="sxs-lookup"><span data-stu-id="8216e-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="8216e-117">Il primo comando ottiene la rete virtuale di Azure denominata MyVnet e passa il risultato usando la pipeline al cmdlet **Get-AzVirtualNetworkSubnetConfig** per ottenere la subnet denominata sottoreti.</span><span class="sxs-lookup"><span data-stu-id="8216e-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="8216e-118">Il comando Archivia quindi il risultato nella variabile denominata $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8216e-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="8216e-119">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con un indirizzo IP privato statico dalla subnet archiviata nella variabile denominata $subnet.</span><span class="sxs-lookup"><span data-stu-id="8216e-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="8216e-120">Esempio 3 aggiunta di una configurazione IP front-end con un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="8216e-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="8216e-121">Il primo comando ottiene l'indirizzo IP pubblico di Azure denominato MyPub e archivia il risultato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="8216e-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="8216e-122">Il secondo comando ottiene il bilanciamento del carico denominato MyLB e passa il risultato al cmdlet **Add-AzLoadBalancerFrontendIpConfig** che aggiunge una configurazione IP front-end al bilanciamento del carico con l'indirizzo IP pubblico archiviato nella variabile denominata $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="8216e-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="8216e-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8216e-123">PARAMETERS</span></span>

### <span data-ttu-id="8216e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8216e-124">-DefaultProfile</span></span>
<span data-ttu-id="8216e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8216e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8216e-126">-LoadBalancer</span></span>
<span data-ttu-id="8216e-127">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="8216e-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="8216e-128">Questo cmdlet aggiunge una configurazione IP front-end al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8216e-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8216e-129">-Name</span></span>
<span data-ttu-id="8216e-130">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="8216e-130">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8216e-131">-PrivateIpAddress</span></span>
<span data-ttu-id="8216e-132">Specifica l'indirizzo IP privato da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8216e-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8216e-133">-PublicIpAddress</span></span>
<span data-ttu-id="8216e-134">Specifica l'indirizzo IP pubblico da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8216e-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8216e-135">-PublicIpAddressId</span></span>
<span data-ttu-id="8216e-136">Specifica l'ID dell'indirizzo IP pubblico in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8216e-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-137">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8216e-137">-Subnet</span></span>
<span data-ttu-id="8216e-138">Specifica l'oggetto subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8216e-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8216e-139">-SubnetId</span></span>
<span data-ttu-id="8216e-140">Specifica l'ID della subnet in cui aggiungere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8216e-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216e-141">-Zona</span><span class="sxs-lookup"><span data-stu-id="8216e-141">-Zone</span></span>
<span data-ttu-id="8216e-142">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="8216e-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8216e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8216e-143">CommonParameters</span></span>
<span data-ttu-id="8216e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8216e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8216e-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8216e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8216e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8216e-146">INPUTS</span></span>

### <span data-ttu-id="8216e-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8216e-147">PSLoadBalancer</span></span>
<span data-ttu-id="8216e-148">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8216e-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8216e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8216e-149">OUTPUTS</span></span>

### <span data-ttu-id="8216e-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8216e-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8216e-151">Note</span><span class="sxs-lookup"><span data-stu-id="8216e-151">NOTES</span></span>

## <span data-ttu-id="8216e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8216e-152">RELATED LINKS</span></span>

[<span data-ttu-id="8216e-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8216e-154">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8216e-154">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="8216e-155">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-155">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8216e-156">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-156">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8216e-157">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-157">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8216e-158">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8216e-158">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


