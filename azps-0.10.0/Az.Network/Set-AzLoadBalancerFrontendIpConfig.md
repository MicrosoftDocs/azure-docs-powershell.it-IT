---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862793"
---
# <span data-ttu-id="8cefd-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cefd-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8cefd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cefd-102">SYNOPSIS</span></span>
<span data-ttu-id="8cefd-103">Imposta lo stato obiettivo per una configurazione IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8cefd-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="8cefd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cefd-104">SYNTAX</span></span>

### <span data-ttu-id="8cefd-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="8cefd-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cefd-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="8cefd-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cefd-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8cefd-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cefd-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8cefd-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cefd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cefd-109">DESCRIPTION</span></span>
<span data-ttu-id="8cefd-110">Il cmdlet **set-AzLoadBalancerFrontendIpConfig** imposta lo stato dell'obiettivo per una configurazione IP front-end in un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cefd-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="8cefd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cefd-111">EXAMPLES</span></span>

### <span data-ttu-id="8cefd-112">Esempio 1: modificare la configurazione IP front-end di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="8cefd-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="8cefd-113">Il primo comando consente di ottenere la subnet virtuale denominata subnet e di archiviarla nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8cefd-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="8cefd-114">Il secondo comando ottiene il bilanciamento del carico associato denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="8cefd-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="8cefd-115">Il terzo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerFrontendIpConfig, che crea una configurazione IP front-end denominata NewFrontend per $slb.</span><span class="sxs-lookup"><span data-stu-id="8cefd-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="8cefd-116">Il quarto comando passa il bilanciamento del carico in $slb a **set-AzLoadBalancerFrontendIpConfig** , che consente di salvare e aggiornare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="8cefd-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="8cefd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cefd-117">PARAMETERS</span></span>

### <span data-ttu-id="8cefd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cefd-118">-DefaultProfile</span></span>
<span data-ttu-id="8cefd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cefd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cefd-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cefd-120">-LoadBalancer</span></span>
<span data-ttu-id="8cefd-121">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8cefd-121">Specifies a load balancer.</span></span>
<span data-ttu-id="8cefd-122">Questo cmdlet imposta lo stato dell'obiettivo per una configurazione front-end per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8cefd-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8cefd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cefd-123">-Name</span></span>
<span data-ttu-id="8cefd-124">Specifica il nome della configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="8cefd-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="8cefd-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8cefd-125">-PrivateIpAddress</span></span>
<span data-ttu-id="8cefd-126">Specifica l'indirizzo IP privato del bilanciamento del carico associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="8cefd-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="8cefd-127">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="8cefd-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="8cefd-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8cefd-128">-PublicIpAddress</span></span>
<span data-ttu-id="8cefd-129">Specifica l'oggetto **PublicIpAddress** associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="8cefd-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="8cefd-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8cefd-130">-PublicIpAddressId</span></span>
<span data-ttu-id="8cefd-131">Specifica l'ID dell'oggetto **PublicIpAddress** associato alla configurazione IP front-end che questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="8cefd-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8cefd-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8cefd-132">-Subnet</span></span>
<span data-ttu-id="8cefd-133">Specifica l'oggetto **subnet** che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cefd-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8cefd-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8cefd-134">-SubnetId</span></span>
<span data-ttu-id="8cefd-135">Specifica l'ID della subnet che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cefd-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8cefd-136">-Zona</span><span class="sxs-lookup"><span data-stu-id="8cefd-136">-Zone</span></span>
<span data-ttu-id="8cefd-137">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="8cefd-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8cefd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cefd-138">CommonParameters</span></span>
<span data-ttu-id="8cefd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cefd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cefd-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cefd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cefd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cefd-141">INPUTS</span></span>

### <span data-ttu-id="8cefd-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cefd-142">PSLoadBalancer</span></span>
<span data-ttu-id="8cefd-143">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8cefd-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8cefd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cefd-144">OUTPUTS</span></span>

### <span data-ttu-id="8cefd-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cefd-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8cefd-146">Note</span><span class="sxs-lookup"><span data-stu-id="8cefd-146">NOTES</span></span>

## <span data-ttu-id="8cefd-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cefd-147">RELATED LINKS</span></span>

[<span data-ttu-id="8cefd-148">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cefd-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8cefd-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cefd-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8cefd-150">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cefd-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8cefd-151">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8cefd-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="8cefd-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cefd-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8cefd-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cefd-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


