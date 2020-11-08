---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201056"
---
# <span data-ttu-id="d01d7-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d01d7-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d01d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d01d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d01d7-103">Aggiorna il pool back-end in un LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d01d7-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="d01d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d01d7-104">SYNTAX</span></span>

### <span data-ttu-id="d01d7-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d7-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01d7-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d7-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01d7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01d7-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d7-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d01d7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d01d7-109">DESCRIPTION</span></span>
<span data-ttu-id="d01d7-110">Aggiorna il pool back-end in un LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d01d7-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="d01d7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d01d7-111">EXAMPLES</span></span>

### <span data-ttu-id="d01d7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d01d7-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="d01d7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d01d7-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="d01d7-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d01d7-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="d01d7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d01d7-115">PARAMETERS</span></span>

### <span data-ttu-id="d01d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01d7-116">-DefaultProfile</span></span>
<span data-ttu-id="d01d7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d01d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01d7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d01d7-118">-Force</span></span>
<span data-ttu-id="d01d7-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d01d7-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d01d7-120">-InputObject</span></span>
<span data-ttu-id="d01d7-121">Il pool di indirizzi di backend da impostare</span><span class="sxs-lookup"><span data-stu-id="d01d7-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d01d7-122">-LoadBalancer</span></span>
<span data-ttu-id="d01d7-123">Risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d01d7-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="d01d7-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="d01d7-125">Indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="d01d7-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d01d7-126">-LoadBalancerName</span></span>
<span data-ttu-id="d01d7-127">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d01d7-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d01d7-128">-Name</span></span>
<span data-ttu-id="d01d7-129">Nome del pool di backend.</span><span class="sxs-lookup"><span data-stu-id="d01d7-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d01d7-130">-PassThru</span></span>
<span data-ttu-id="d01d7-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d01d7-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01d7-132">-ResourceGroupName</span></span>
<span data-ttu-id="d01d7-133">Nome del gruppo di risorse del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d01d7-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d01d7-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01d7-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d01d7-135">-Confirm</span></span>
<span data-ttu-id="d01d7-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d01d7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01d7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d01d7-137">-WhatIf</span></span>
<span data-ttu-id="d01d7-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d01d7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d01d7-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d01d7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01d7-140">CommonParameters</span></span>
<span data-ttu-id="d01d7-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01d7-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d01d7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01d7-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d01d7-143">INPUTS</span></span>

### <span data-ttu-id="d01d7-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d01d7-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d01d7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d01d7-145">System.String</span></span>

## <span data-ttu-id="d01d7-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d01d7-146">OUTPUTS</span></span>

### <span data-ttu-id="d01d7-147">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d01d7-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d01d7-148">Note</span><span class="sxs-lookup"><span data-stu-id="d01d7-148">NOTES</span></span>

## <span data-ttu-id="d01d7-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d01d7-149">RELATED LINKS</span></span>
