---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 783eb017f336cd587f51f286cad296c267e6b68c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997693"
---
# <span data-ttu-id="f8eca-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f8eca-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="f8eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8eca-102">SYNOPSIS</span></span>
<span data-ttu-id="f8eca-103">Crea un pool di indirizzi back-end su un carico di carico.</span><span class="sxs-lookup"><span data-stu-id="f8eca-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="f8eca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8eca-104">SYNTAX</span></span>

### <span data-ttu-id="f8eca-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8eca-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8eca-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8eca-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8eca-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8eca-107">DESCRIPTION</span></span>
<span data-ttu-id="f8eca-108">Crea un pool di indirizzi back-end su un carico di carico.</span><span class="sxs-lookup"><span data-stu-id="f8eca-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="f8eca-109">Consente di specificare una matrice di PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="f8eca-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="f8eca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8eca-110">EXAMPLES</span></span>

### <span data-ttu-id="f8eca-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8eca-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="f8eca-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f8eca-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="f8eca-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f8eca-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="f8eca-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="f8eca-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="f8eca-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8eca-115">PARAMETERS</span></span>

### <span data-ttu-id="f8eca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8eca-116">-DefaultProfile</span></span>
<span data-ttu-id="f8eca-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8eca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8eca-118">-LoadBalancer</span></span>
<span data-ttu-id="f8eca-119">Risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f8eca-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="f8eca-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="f8eca-121">Gli indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="f8eca-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="f8eca-122">-LoadBalancerName</span></span>
<span data-ttu-id="f8eca-123">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f8eca-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f8eca-124">-Name</span></span>
<span data-ttu-id="f8eca-125">Nome del pool back-end.</span><span class="sxs-lookup"><span data-stu-id="f8eca-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="f8eca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8eca-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8eca-127">Nome del gruppo di risorse per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f8eca-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8eca-128">-Confirm</span></span>
<span data-ttu-id="f8eca-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8eca-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8eca-130">-WhatIf</span></span>
<span data-ttu-id="f8eca-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8eca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8eca-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8eca-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8eca-133">CommonParameters</span></span>
<span data-ttu-id="f8eca-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8eca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8eca-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8eca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8eca-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8eca-136">INPUTS</span></span>

### <span data-ttu-id="f8eca-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8eca-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8eca-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8eca-138">OUTPUTS</span></span>

### <span data-ttu-id="f8eca-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f8eca-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f8eca-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8eca-140">NOTES</span></span>

## <span data-ttu-id="f8eca-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8eca-141">RELATED LINKS</span></span>
