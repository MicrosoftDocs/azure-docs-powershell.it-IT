---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385475"
---
# <span data-ttu-id="d3226-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d3226-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d3226-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3226-102">SYNOPSIS</span></span>
<span data-ttu-id="d3226-103">Crea un pool di indirizzi back-end in un LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d3226-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="d3226-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3226-104">SYNTAX</span></span>

### <span data-ttu-id="d3226-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3226-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3226-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3226-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3226-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3226-107">DESCRIPTION</span></span>
<span data-ttu-id="d3226-108">Crea un pool di indirizzi back-end in un LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d3226-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="d3226-109">Consente di specifica una matrice di PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="d3226-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="d3226-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3226-110">EXAMPLES</span></span>

### <span data-ttu-id="d3226-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3226-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="d3226-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d3226-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="d3226-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d3226-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="d3226-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d3226-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="d3226-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3226-115">PARAMETERS</span></span>

### <span data-ttu-id="d3226-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3226-116">-DefaultProfile</span></span>
<span data-ttu-id="d3226-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3226-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3226-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3226-118">-LoadBalancer</span></span>
<span data-ttu-id="d3226-119">Risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d3226-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="d3226-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="d3226-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="d3226-121">Indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="d3226-121">The backend addresses.</span></span>

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

### <span data-ttu-id="d3226-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d3226-122">-LoadBalancerName</span></span>
<span data-ttu-id="d3226-123">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d3226-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="d3226-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3226-124">-Name</span></span>
<span data-ttu-id="d3226-125">Nome del pool di backend.</span><span class="sxs-lookup"><span data-stu-id="d3226-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="d3226-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3226-126">-ResourceGroupName</span></span>
<span data-ttu-id="d3226-127">Nome del gruppo di risorse del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d3226-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="d3226-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3226-128">-Confirm</span></span>
<span data-ttu-id="d3226-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3226-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3226-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3226-130">-WhatIf</span></span>
<span data-ttu-id="d3226-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3226-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3226-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3226-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3226-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3226-133">CommonParameters</span></span>
<span data-ttu-id="d3226-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3226-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3226-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3226-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3226-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3226-136">INPUTS</span></span>

### <span data-ttu-id="d3226-137">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3226-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3226-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3226-138">OUTPUTS</span></span>

### <span data-ttu-id="d3226-139">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d3226-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d3226-140">Note</span><span class="sxs-lookup"><span data-stu-id="d3226-140">NOTES</span></span>

## <span data-ttu-id="d3226-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3226-141">RELATED LINKS</span></span>
