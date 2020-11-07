---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673596"
---
# <span data-ttu-id="27311-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="27311-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="27311-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27311-102">SYNOPSIS</span></span>
<span data-ttu-id="27311-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="27311-103">Create or update a quota.</span></span>

## <span data-ttu-id="27311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27311-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27311-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27311-105">DESCRIPTION</span></span>
<span data-ttu-id="27311-106">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="27311-106">Create or update a quota.</span></span>

## <span data-ttu-id="27311-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27311-107">EXAMPLES</span></span>

### <span data-ttu-id="27311-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27311-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="27311-109">Creare una nuova quota di rete con tutti i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="27311-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="27311-110">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="27311-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="27311-111">Creare una nuova quota di rete con valori non predefiniti per la quota.</span><span class="sxs-lookup"><span data-stu-id="27311-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="27311-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27311-112">PARAMETERS</span></span>

### <span data-ttu-id="27311-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="27311-113">-Location</span></span>
<span data-ttu-id="27311-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="27311-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="27311-116">Numero massimo di bilanciamento del carico consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="27311-118">Le NIC massime consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-119">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="27311-120">Gli indirizzi IP pubblici massimi consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="27311-122">Numero massimo di gruppi di sicurezza consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="27311-124">Numero massimo di connessioni Virtual Network Gateway consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="27311-126">Numero massimo di gateway di rete virtuali consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27311-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="27311-128">Numero Maxium di reti virtuali consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="27311-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="27311-129">-MigrationPhase</span></span>
<span data-ttu-id="27311-130">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="27311-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="27311-131">-Name</span></span>
<span data-ttu-id="27311-132">Nome della risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="27311-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27311-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27311-133">-Confirm</span></span>
<span data-ttu-id="27311-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27311-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27311-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27311-135">-WhatIf</span></span>
<span data-ttu-id="27311-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27311-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27311-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27311-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27311-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27311-138">CommonParameters</span></span>
<span data-ttu-id="27311-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27311-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27311-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27311-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27311-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27311-141">INPUTS</span></span>

## <span data-ttu-id="27311-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27311-142">OUTPUTS</span></span>

### <span data-ttu-id="27311-143">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="27311-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="27311-144">Note</span><span class="sxs-lookup"><span data-stu-id="27311-144">NOTES</span></span>

## <span data-ttu-id="27311-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27311-145">RELATED LINKS</span></span>

