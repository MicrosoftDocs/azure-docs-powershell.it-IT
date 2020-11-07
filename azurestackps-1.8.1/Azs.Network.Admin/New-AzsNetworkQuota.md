---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859881"
---
# <span data-ttu-id="65373-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="65373-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="65373-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65373-102">SYNOPSIS</span></span>
<span data-ttu-id="65373-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="65373-103">Create or update a quota.</span></span>

## <span data-ttu-id="65373-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65373-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65373-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65373-105">DESCRIPTION</span></span>
<span data-ttu-id="65373-106">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="65373-106">Create or update a quota.</span></span>

## <span data-ttu-id="65373-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65373-107">EXAMPLES</span></span>

### <span data-ttu-id="65373-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="65373-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="65373-109">Creare una nuova quota di rete con tutti i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="65373-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="65373-110">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="65373-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="65373-111">Creare una nuova quota di rete con valori non predefiniti per la quota.</span><span class="sxs-lookup"><span data-stu-id="65373-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="65373-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65373-112">PARAMETERS</span></span>

### <span data-ttu-id="65373-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="65373-113">-Name</span></span>
<span data-ttu-id="65373-114">Nome della risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="65373-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="65373-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="65373-116">Le NIC massime consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="65373-118">Gli indirizzi IP pubblici massimi consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="65373-120">Numero massimo di connessioni Virtual Network Gateway consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="65373-122">Numero Maxium di reti virtuali consentite per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="65373-124">Numero massimo di gateway di rete virtuali consentiti per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="65373-126">Numero massimo di gruppi di sicurezza consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="65373-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="65373-128">Numero massimo di bilanciamento del carico consentiti per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="65373-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="65373-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="65373-129">-Location</span></span>
<span data-ttu-id="65373-130">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="65373-130">Location of the resource.</span></span>

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

### <span data-ttu-id="65373-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="65373-131">-MigrationPhase</span></span>
<span data-ttu-id="65373-132">Stato di migrazione, ad esempio None, prepara, conferma e Interrompi.</span><span class="sxs-lookup"><span data-stu-id="65373-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="65373-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65373-133">-WhatIf</span></span>
<span data-ttu-id="65373-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65373-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65373-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65373-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65373-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65373-136">-Confirm</span></span>
<span data-ttu-id="65373-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65373-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65373-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65373-138">CommonParameters</span></span>
<span data-ttu-id="65373-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65373-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65373-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65373-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65373-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65373-141">INPUTS</span></span>

## <span data-ttu-id="65373-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65373-142">OUTPUTS</span></span>

### <span data-ttu-id="65373-143">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="65373-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="65373-144">Note</span><span class="sxs-lookup"><span data-stu-id="65373-144">NOTES</span></span>

## <span data-ttu-id="65373-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65373-145">RELATED LINKS</span></span>
