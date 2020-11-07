---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 8de9d162ceba8dc436d5244f75011b79a949ddeb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866850"
---
# <span data-ttu-id="c441a-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c441a-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c441a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c441a-102">SYNOPSIS</span></span>
<span data-ttu-id="c441a-103">Imposta lo stato obiettivo per una configurazione IP front-end in un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c441a-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c441a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c441a-104">SYNTAX</span></span>

### <span data-ttu-id="c441a-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="c441a-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c441a-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="c441a-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c441a-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c441a-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c441a-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c441a-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c441a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c441a-109">DESCRIPTION</span></span>
<span data-ttu-id="c441a-110">Il cmdlet **set-AzureRmLoadBalancerFrontendIpConfig** imposta lo stato dell'obiettivo per una configurazione IP front-end in un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c441a-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="c441a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c441a-111">EXAMPLES</span></span>

### <span data-ttu-id="c441a-112">Esempio 1: modificare la configurazione IP front-end di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c441a-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="c441a-113">Il primo comando consente di ottenere la subnet virtuale denominata subnet e di archiviarla nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c441a-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="c441a-114">Il secondo comando ottiene il bilanciamento del carico associato denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="c441a-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="c441a-115">Il terzo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzureRmLoadBalancerFrontendIpConfig, che crea una configurazione IP front-end denominata NewFrontend per $slb.</span><span class="sxs-lookup"><span data-stu-id="c441a-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="c441a-116">Il quarto comando passa il bilanciamento del carico in $slb a **set-AzureRmLoadBalancerFrontendIpConfig** , che consente di salvare e aggiornare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="c441a-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="c441a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c441a-117">PARAMETERS</span></span>

### <span data-ttu-id="c441a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c441a-118">-DefaultProfile</span></span>
<span data-ttu-id="c441a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c441a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c441a-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c441a-120">-LoadBalancer</span></span>
<span data-ttu-id="c441a-121">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c441a-121">Specifies a load balancer.</span></span>
<span data-ttu-id="c441a-122">Questo cmdlet imposta lo stato dell'obiettivo per una configurazione front-end per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c441a-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c441a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c441a-123">-Name</span></span>
<span data-ttu-id="c441a-124">Specifica il nome della configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="c441a-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="c441a-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c441a-125">-PrivateIpAddress</span></span>
<span data-ttu-id="c441a-126">Specifica l'indirizzo IP privato del bilanciamento del carico associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="c441a-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="c441a-127">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="c441a-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="c441a-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c441a-128">-PublicIpAddress</span></span>
<span data-ttu-id="c441a-129">Specifica l'oggetto **PublicIpAddress** associato alla configurazione IP front-end da impostare.</span><span class="sxs-lookup"><span data-stu-id="c441a-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="c441a-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c441a-130">-PublicIpAddressId</span></span>
<span data-ttu-id="c441a-131">Specifica l'ID dell'oggetto **PublicIpAddress** associato alla configurazione IP front-end che questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="c441a-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c441a-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c441a-132">-Subnet</span></span>
<span data-ttu-id="c441a-133">Specifica l'oggetto **subnet** che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c441a-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c441a-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c441a-134">-SubnetId</span></span>
<span data-ttu-id="c441a-135">Specifica l'ID della subnet che contiene la configurazione IP front-end impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c441a-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c441a-136">-Zona</span><span class="sxs-lookup"><span data-stu-id="c441a-136">-Zone</span></span>
<span data-ttu-id="c441a-137">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="c441a-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="c441a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c441a-138">CommonParameters</span></span>
<span data-ttu-id="c441a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c441a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c441a-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c441a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c441a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c441a-141">INPUTS</span></span>

### <span data-ttu-id="c441a-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c441a-142">PSLoadBalancer</span></span>
<span data-ttu-id="c441a-143">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c441a-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c441a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c441a-144">OUTPUTS</span></span>

### <span data-ttu-id="c441a-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c441a-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c441a-146">Note</span><span class="sxs-lookup"><span data-stu-id="c441a-146">NOTES</span></span>

## <span data-ttu-id="c441a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c441a-147">RELATED LINKS</span></span>

[<span data-ttu-id="c441a-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c441a-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c441a-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c441a-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c441a-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c441a-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c441a-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c441a-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c441a-152">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c441a-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c441a-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c441a-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


