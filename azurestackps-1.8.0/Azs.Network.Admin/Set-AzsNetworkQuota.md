---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859293"
---
# <span data-ttu-id="fb6c3-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="fb6c3-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="fb6c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6c3-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-103">Create or update a quota.</span></span>

## <span data-ttu-id="fb6c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb6c3-104">SYNTAX</span></span>

### <span data-ttu-id="fb6c3-105">Quote (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb6c3-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6c3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6c3-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6c3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6c3-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6c3-108">DESCRIPTION</span></span>
<span data-ttu-id="fb6c3-109">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-109">Create or update a quota.</span></span>

## <span data-ttu-id="fb6c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb6c3-110">EXAMPLES</span></span>

### <span data-ttu-id="fb6c3-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="fb6c3-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="fb6c3-112">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-112">Update a network quota by name.</span></span>

### <span data-ttu-id="fb6c3-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="fb6c3-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="fb6c3-114">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-114">Update a network quota by name.</span></span>

## <span data-ttu-id="fb6c3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb6c3-115">PARAMETERS</span></span>

### <span data-ttu-id="fb6c3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb6c3-116">-Name</span></span>
<span data-ttu-id="fb6c3-117">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="fb6c3-119">Le NIC massime consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="fb6c3-121">Gli indirizzi IP pubblici massimi consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="fb6c3-123">Numero massimo di connessioni Virtual Network Gateway consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="fb6c3-125">Numero Maxium di reti virtuali consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="fb6c3-127">Numero massimo di gateway di rete virtuali consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="fb6c3-129">Numero massimo di gruppi di sicurezza consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6c3-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="fb6c3-131">Numero massimo di bilanciamento del carico consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fb6c3-132">-Location</span></span>
<span data-ttu-id="fb6c3-133">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6c3-134">-ResourceId</span></span>
<span data-ttu-id="fb6c3-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6c3-136">-InputObject</span></span>
<span data-ttu-id="fb6c3-137">Quota di rete modificata di Posbbily restituita da Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="fb6c3-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6c3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6c3-138">-WhatIf</span></span>
<span data-ttu-id="fb6c3-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6c3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6c3-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb6c3-141">-Confirm</span></span>
<span data-ttu-id="fb6c3-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6c3-143">CommonParameters</span></span>
<span data-ttu-id="fb6c3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6c3-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6c3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6c3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb6c3-146">INPUTS</span></span>

## <span data-ttu-id="fb6c3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb6c3-147">OUTPUTS</span></span>

### <span data-ttu-id="fb6c3-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="fb6c3-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="fb6c3-149">Note</span><span class="sxs-lookup"><span data-stu-id="fb6c3-149">NOTES</span></span>

## <span data-ttu-id="fb6c3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb6c3-150">RELATED LINKS</span></span>
