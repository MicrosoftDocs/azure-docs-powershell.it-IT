---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023203"
---
# <span data-ttu-id="a2191-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a2191-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="a2191-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2191-102">SYNOPSIS</span></span>
<span data-ttu-id="a2191-103">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="a2191-103">Create or update a quota.</span></span>

## <span data-ttu-id="a2191-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2191-104">SYNTAX</span></span>

### <span data-ttu-id="a2191-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2191-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2191-106">Creare</span><span class="sxs-lookup"><span data-stu-id="a2191-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2191-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2191-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2191-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a2191-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2191-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2191-109">DESCRIPTION</span></span>
<span data-ttu-id="a2191-110">Creare o aggiornare una quota.</span><span class="sxs-lookup"><span data-stu-id="a2191-110">Create or update a quota.</span></span>

## <span data-ttu-id="a2191-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2191-111">EXAMPLES</span></span>

### <span data-ttu-id="a2191-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2191-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="a2191-113">Creare una nuova quota di rete con tutti i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a2191-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="a2191-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2191-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="a2191-115">Creare una nuova quota di rete con valori non predefiniti per la quota.</span><span class="sxs-lookup"><span data-stu-id="a2191-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="a2191-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2191-116">PARAMETERS</span></span>

### <span data-ttu-id="a2191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2191-117">-DefaultProfile</span></span>
<span data-ttu-id="a2191-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2191-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2191-119">-InputObject</span></span>
<span data-ttu-id="a2191-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a2191-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a2191-121">-Location</span></span>
<span data-ttu-id="a2191-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2191-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a2191-124">Numero massimo di servizi di bilanciamento del carico che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a2191-126">Numero massimo di schede di nic che un abbonamento al tenant può provisionare.</span><span class="sxs-lookup"><span data-stu-id="a2191-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a2191-128">Numero massimo di indirizzi IP pubblici che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a2191-130">Numero massimo di gruppi di sicurezza a cui può essere fornito un abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a2191-132">Numero massimo di connessioni Virtual Network Gateway che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="a2191-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a2191-134">Numero massimo di gateway di rete virtuale che un abbonamento al tenant può eseguire.</span><span class="sxs-lookup"><span data-stu-id="a2191-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a2191-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a2191-136">Numero massimo di reti virtuali che possono essere provisionate dall'abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2191-137">-Name</span></span>
<span data-ttu-id="a2191-138">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2191-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-139">-Quota</span><span class="sxs-lookup"><span data-stu-id="a2191-139">-Quota</span></span>
<span data-ttu-id="a2191-140">Risorsa quota di rete.</span><span class="sxs-lookup"><span data-stu-id="a2191-140">Network quota resource.</span></span>
<span data-ttu-id="a2191-141">Per costruire, vedere la sezione Note per le proprietà delle quote e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a2191-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2191-142">-SubscriptionId</span></span>
<span data-ttu-id="a2191-143">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a2191-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a2191-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a2191-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2191-145">-Tag</span></span>
<span data-ttu-id="a2191-146">Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="a2191-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2191-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2191-147">-Confirm</span></span>
<span data-ttu-id="a2191-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2191-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2191-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2191-149">-WhatIf</span></span>
<span data-ttu-id="a2191-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2191-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2191-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2191-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2191-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2191-152">CommonParameters</span></span>
<span data-ttu-id="a2191-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2191-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2191-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2191-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2191-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2191-155">INPUTS</span></span>

### <span data-ttu-id="a2191-156">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="a2191-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="a2191-157">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a2191-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="a2191-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2191-158">OUTPUTS</span></span>

### <span data-ttu-id="a2191-159">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="a2191-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="a2191-160">Note</span><span class="sxs-lookup"><span data-stu-id="a2191-160">NOTES</span></span>

<span data-ttu-id="a2191-161">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a2191-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2191-162">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2191-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a2191-163">INPUTOBJECT <INetworkAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a2191-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2191-164">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a2191-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2191-165">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2191-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a2191-166">`[ResourceName <String>]`: Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2191-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="a2191-167">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a2191-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a2191-168">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a2191-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="a2191-169">QUOTA <IQuota> : risorsa quota di rete.</span><span class="sxs-lookup"><span data-stu-id="a2191-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="a2191-170">`[Tag <IResourceTags>]`: Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="a2191-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="a2191-171">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a2191-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a2191-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Numero massimo di servizi di bilanciamento del carico che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-173">`[MaxNicsPerSubscription <Int64?>]`: Numero massimo di nic che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="a2191-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Numero massimo di indirizzi IP pubblici che possono essere provisionati da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Numero massimo di gruppi di sicurezza a cui può essere previsto un abbonamento del tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Numero massimo di connessioni Virtual Network Gateway che un abbonamento a un tenant può fornire.</span><span class="sxs-lookup"><span data-stu-id="a2191-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Numero massimo di gateway di rete virtuale a cui è possibile eseguire il provisioning di un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a2191-178">`[MaxVnetsPerSubscription <Int64?>]`: Numero massimo di reti virtuali che possono essere provisionate da un abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a2191-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="a2191-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2191-179">RELATED LINKS</span></span>

