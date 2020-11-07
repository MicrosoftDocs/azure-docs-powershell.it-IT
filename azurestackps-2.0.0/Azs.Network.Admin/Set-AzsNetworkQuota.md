---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861673"
---
# <span data-ttu-id="d991e-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="d991e-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="d991e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d991e-102">SYNOPSIS</span></span>
<span data-ttu-id="d991e-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="d991e-103">Create or update a quota.</span></span>

## <span data-ttu-id="d991e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d991e-104">SYNTAX</span></span>

### <span data-ttu-id="d991e-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d991e-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d991e-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d991e-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d991e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d991e-107">DESCRIPTION</span></span>
<span data-ttu-id="d991e-108">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="d991e-108">Create or update a quota.</span></span>

## <span data-ttu-id="d991e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d991e-109">EXAMPLES</span></span>

### <span data-ttu-id="d991e-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d991e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="d991e-111">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="d991e-111">Update a network quota by name.</span></span>

### <span data-ttu-id="d991e-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d991e-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="d991e-113">Aggiornare una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="d991e-113">Update a network quota by name.</span></span>

## <span data-ttu-id="d991e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d991e-114">PARAMETERS</span></span>

### <span data-ttu-id="d991e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d991e-115">-DefaultProfile</span></span>
<span data-ttu-id="d991e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d991e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d991e-117">-Location</span></span>
<span data-ttu-id="d991e-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d991e-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="d991e-120">Numero massimo di servizi di bilanciamento del carico che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="d991e-122">Numero massimo di schede di nic che un abbonamento al tenant può provisionare.</span><span class="sxs-lookup"><span data-stu-id="d991e-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="d991e-124">Numero massimo di indirizzi IP pubblici che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="d991e-126">Numero massimo di gruppi di sicurezza a cui può essere fornito un abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="d991e-128">Numero massimo di connessioni Virtual Network Gateway che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="d991e-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="d991e-130">Numero massimo di gateway di rete virtuale che un abbonamento al tenant può eseguire.</span><span class="sxs-lookup"><span data-stu-id="d991e-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d991e-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="d991e-132">Numero massimo di reti virtuali che possono essere provisionate dall'abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d991e-133">-Name</span></span>
<span data-ttu-id="d991e-134">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d991e-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-135">-Quota</span><span class="sxs-lookup"><span data-stu-id="d991e-135">-Quota</span></span>
<span data-ttu-id="d991e-136">Risorsa quota di rete.</span><span class="sxs-lookup"><span data-stu-id="d991e-136">Network quota resource.</span></span>
<span data-ttu-id="d991e-137">Per costruire, vedere la sezione Note per le proprietà delle quote e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d991e-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d991e-138">-SubscriptionId</span></span>
<span data-ttu-id="d991e-139">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d991e-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d991e-140">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d991e-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="d991e-141">-Tag</span></span>
<span data-ttu-id="d991e-142">Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="d991e-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d991e-143">-Confirm</span></span>
<span data-ttu-id="d991e-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d991e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d991e-145">-WhatIf</span></span>
<span data-ttu-id="d991e-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d991e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d991e-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d991e-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d991e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d991e-148">CommonParameters</span></span>
<span data-ttu-id="d991e-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d991e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d991e-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d991e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d991e-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d991e-151">INPUTS</span></span>

### <span data-ttu-id="d991e-152">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d991e-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="d991e-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d991e-153">OUTPUTS</span></span>

### <span data-ttu-id="d991e-154">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d991e-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="d991e-155">Note</span><span class="sxs-lookup"><span data-stu-id="d991e-155">NOTES</span></span>

<span data-ttu-id="d991e-156">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d991e-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d991e-157">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d991e-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d991e-158">QUOTA <IQuota> : risorsa quota di rete.</span><span class="sxs-lookup"><span data-stu-id="d991e-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="d991e-159">`[Tag <IResourceTags>]`: Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="d991e-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="d991e-160">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d991e-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d991e-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Numero massimo di servizi di bilanciamento del carico che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-162">`[MaxNicsPerSubscription <Int64?>]`: Numero massimo di nic che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="d991e-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Numero massimo di indirizzi IP pubblici che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Numero massimo di gruppi di sicurezza a cui può essere previsto un abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Numero massimo di connessioni Virtual Network Gateway che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="d991e-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Numero massimo di gateway di rete virtuale a cui è possibile eseguire il provisioning di un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d991e-167">`[MaxVnetsPerSubscription <Int64?>]`: Numero massimo di reti virtuali che possono essere provisionate da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="d991e-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="d991e-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d991e-168">RELATED LINKS</span></span>

