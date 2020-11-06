---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490997"
---
# <span data-ttu-id="a7af0-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a7af0-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="a7af0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7af0-102">SYNOPSIS</span></span>
<span data-ttu-id="a7af0-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="a7af0-103">Create or update a quota.</span></span>

## <span data-ttu-id="a7af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7af0-104">SYNTAX</span></span>

### <span data-ttu-id="a7af0-105">Quote (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7af0-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7af0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7af0-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7af0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7af0-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7af0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7af0-108">DESCRIPTION</span></span>
<span data-ttu-id="a7af0-109">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="a7af0-109">Create or update a quota.</span></span>

## <span data-ttu-id="a7af0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7af0-110">EXAMPLES</span></span>

### <span data-ttu-id="a7af0-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7af0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="a7af0-112">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="a7af0-112">Update a network quota by name.</span></span>

### <span data-ttu-id="a7af0-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7af0-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="a7af0-114">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="a7af0-114">Update a network quota by name.</span></span>

## <span data-ttu-id="a7af0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7af0-115">PARAMETERS</span></span>

### <span data-ttu-id="a7af0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7af0-116">-InputObject</span></span>
<span data-ttu-id="a7af0-117">Quota di rete modificata di Posbbily restituita da Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a7af0-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="a7af0-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a7af0-118">-Location</span></span>
<span data-ttu-id="a7af0-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7af0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a7af0-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a7af0-121">Numero massimo di bilanciamento del carico consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-121">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a7af0-123">Le NIC massime consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-123">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a7af0-125">Gli indirizzi IP pubblici massimi consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-125">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a7af0-127">Numero massimo di gruppi di sicurezza consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-127">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a7af0-129">Numero massimo di connessioni Virtual Network Gateway consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a7af0-131">Numero massimo di gateway di rete virtuali consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7af0-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a7af0-133">Numero Maxium di reti virtuali consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7af0-133">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="a7af0-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7af0-134">-Name</span></span>
<span data-ttu-id="a7af0-135">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7af0-135">Name of the resource.</span></span>

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

### <span data-ttu-id="a7af0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7af0-136">-ResourceId</span></span>
<span data-ttu-id="a7af0-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7af0-137">The resource id.</span></span>

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

### <span data-ttu-id="a7af0-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7af0-138">-Confirm</span></span>
<span data-ttu-id="a7af0-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7af0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7af0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7af0-140">-WhatIf</span></span>
<span data-ttu-id="a7af0-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7af0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7af0-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7af0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7af0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7af0-143">CommonParameters</span></span>
<span data-ttu-id="a7af0-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7af0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7af0-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7af0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7af0-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7af0-146">INPUTS</span></span>

## <span data-ttu-id="a7af0-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7af0-147">OUTPUTS</span></span>

### <span data-ttu-id="a7af0-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="a7af0-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="a7af0-149">Note</span><span class="sxs-lookup"><span data-stu-id="a7af0-149">NOTES</span></span>

## <span data-ttu-id="a7af0-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7af0-150">RELATED LINKS</span></span>

