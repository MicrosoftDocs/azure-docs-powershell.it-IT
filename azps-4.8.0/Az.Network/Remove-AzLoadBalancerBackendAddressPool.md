---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188442"
---
# <span data-ttu-id="d5f2a-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5f2a-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d5f2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f2a-103">Rimuove un pool back-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="d5f2a-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="d5f2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5f2a-104">SYNTAX</span></span>

### <span data-ttu-id="d5f2a-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f2a-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f2a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f2a-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5f2a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f2a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f2a-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f2a-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5f2a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5f2a-109">DESCRIPTION</span></span>
<span data-ttu-id="d5f2a-110">Rimuove un pool back-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="d5f2a-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="d5f2a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5f2a-111">EXAMPLES</span></span>

### <span data-ttu-id="d5f2a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5f2a-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="d5f2a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d5f2a-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="d5f2a-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d5f2a-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="d5f2a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5f2a-115">PARAMETERS</span></span>

### <span data-ttu-id="d5f2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f2a-116">-DefaultProfile</span></span>
<span data-ttu-id="d5f2a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f2a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5f2a-118">-InputObject</span></span>
<span data-ttu-id="d5f2a-119">Il pool di indirizzi back-end da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d5f2a-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5f2a-120">-LoadBalancer</span></span>
<span data-ttu-id="d5f2a-121">Risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d5f2a-122">-LoadBalancerName</span></span>
<span data-ttu-id="d5f2a-123">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5f2a-124">-Name</span></span>
<span data-ttu-id="d5f2a-125">Nome del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5f2a-126">-PassThru</span></span>
<span data-ttu-id="d5f2a-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d5f2a-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d5f2a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f2a-128">-ResourceGroupName</span></span>
<span data-ttu-id="d5f2a-129">Nome del gruppo di risorse del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5f2a-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f2a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5f2a-131">-Confirm</span></span>
<span data-ttu-id="d5f2a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5f2a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f2a-133">-WhatIf</span></span>
<span data-ttu-id="d5f2a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5f2a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5f2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f2a-136">CommonParameters</span></span>
<span data-ttu-id="d5f2a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f2a-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5f2a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f2a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5f2a-139">INPUTS</span></span>

### <span data-ttu-id="d5f2a-140">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5f2a-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d5f2a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d5f2a-141">System.String</span></span>

## <span data-ttu-id="d5f2a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5f2a-142">OUTPUTS</span></span>

### <span data-ttu-id="d5f2a-143">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5f2a-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d5f2a-144">Note</span><span class="sxs-lookup"><span data-stu-id="d5f2a-144">NOTES</span></span>

## <span data-ttu-id="d5f2a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5f2a-145">RELATED LINKS</span></span>
