---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192790"
---
# <span data-ttu-id="c8402-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8402-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="c8402-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8402-102">SYNOPSIS</span></span>
<span data-ttu-id="c8402-103">Crea un pool di indirizzi back-end in un LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="c8402-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="c8402-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8402-104">SYNTAX</span></span>

### <span data-ttu-id="c8402-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8402-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8402-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8402-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8402-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8402-107">DESCRIPTION</span></span>
<span data-ttu-id="c8402-108">Crea un pool di indirizzi back-end in un LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="c8402-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="c8402-109">Consente di specifica una matrice di PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="c8402-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="c8402-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8402-110">EXAMPLES</span></span>

### <span data-ttu-id="c8402-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8402-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="c8402-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8402-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="c8402-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c8402-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="c8402-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c8402-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="c8402-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8402-115">PARAMETERS</span></span>

### <span data-ttu-id="c8402-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8402-116">-DefaultProfile</span></span>
<span data-ttu-id="c8402-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8402-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8402-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8402-118">-LoadBalancer</span></span>
<span data-ttu-id="c8402-119">Risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c8402-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="c8402-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c8402-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="c8402-121">Indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="c8402-121">The backend addresses.</span></span>

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

### <span data-ttu-id="c8402-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c8402-122">-LoadBalancerName</span></span>
<span data-ttu-id="c8402-123">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c8402-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="c8402-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8402-124">-Name</span></span>
<span data-ttu-id="c8402-125">Nome del pool di backend.</span><span class="sxs-lookup"><span data-stu-id="c8402-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="c8402-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8402-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8402-127">Nome del gruppo di risorse del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c8402-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="c8402-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8402-128">-Confirm</span></span>
<span data-ttu-id="c8402-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8402-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8402-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8402-130">-WhatIf</span></span>
<span data-ttu-id="c8402-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8402-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8402-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8402-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8402-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8402-133">CommonParameters</span></span>
<span data-ttu-id="c8402-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8402-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8402-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8402-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8402-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8402-136">INPUTS</span></span>

### <span data-ttu-id="c8402-137">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8402-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c8402-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8402-138">OUTPUTS</span></span>

### <span data-ttu-id="c8402-139">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8402-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c8402-140">Note</span><span class="sxs-lookup"><span data-stu-id="c8402-140">NOTES</span></span>

## <span data-ttu-id="c8402-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8402-141">RELATED LINKS</span></span>