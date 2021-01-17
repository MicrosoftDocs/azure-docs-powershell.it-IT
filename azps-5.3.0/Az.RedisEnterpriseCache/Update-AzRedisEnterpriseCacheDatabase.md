---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378153"
---
# <span data-ttu-id="d36cc-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="d36cc-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="d36cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d36cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d36cc-103">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="d36cc-103">Updates a database</span></span>

## <span data-ttu-id="d36cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d36cc-104">SYNTAX</span></span>

### <span data-ttu-id="d36cc-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d36cc-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d36cc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d36cc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d36cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d36cc-107">DESCRIPTION</span></span>
<span data-ttu-id="d36cc-108">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="d36cc-108">Updates a database</span></span>

## <span data-ttu-id="d36cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d36cc-109">EXAMPLES</span></span>

### <span data-ttu-id="d36cc-110">Esempio 1: aggiornare il protocollo client</span><span class="sxs-lookup"><span data-stu-id="d36cc-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="d36cc-111">Questo comando Aggiorna il protocollo client del database per la cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="d36cc-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="d36cc-112">Esempio 2: aggiornare il protocollo client e i criteri di eliminazione</span><span class="sxs-lookup"><span data-stu-id="d36cc-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="d36cc-113">Questo comando Aggiorna il protocollo client e i criteri di eliminazione del database per la cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="d36cc-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d36cc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d36cc-114">PARAMETERS</span></span>

### <span data-ttu-id="d36cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d36cc-115">-AsJob</span></span>
<span data-ttu-id="d36cc-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d36cc-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d36cc-117">-ClientProtocol</span></span>
<span data-ttu-id="d36cc-118">Specifica se i client Redis possono connettersi usando i protocolli di redis crittografati in TLS o in chiaro.</span><span class="sxs-lookup"><span data-stu-id="d36cc-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="d36cc-119">Il valore predefinito è TLS-crittografato.</span><span class="sxs-lookup"><span data-stu-id="d36cc-119">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="d36cc-120">-ClusteringPolicy</span></span>
<span data-ttu-id="d36cc-121">Criteri di clustering: l'impostazione predefinita è OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="d36cc-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="d36cc-122">Specificato in Crea ora.</span><span class="sxs-lookup"><span data-stu-id="d36cc-122">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-123">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d36cc-123">-ClusterName</span></span>
<span data-ttu-id="d36cc-124">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d36cc-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36cc-125">-DefaultProfile</span></span>
<span data-ttu-id="d36cc-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d36cc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d36cc-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d36cc-127">-EvictionPolicy</span></span>
<span data-ttu-id="d36cc-128">Criteri di eliminazione di redis-l'impostazione predefinita è VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="d36cc-128">Redis eviction policy - default is VolatileLRU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d36cc-129">-InputObject</span></span>
<span data-ttu-id="d36cc-130">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d36cc-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-131">-Module</span><span class="sxs-lookup"><span data-stu-id="d36cc-131">-Module</span></span>
<span data-ttu-id="d36cc-132">Set facoltativo di moduli Redis per l'abilitazione in questo database-i moduli possono essere aggiunti solo in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="d36cc-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="d36cc-133">Per creare una tabella hash, vedere la sezione Note per le proprietà del modulo.</span><span class="sxs-lookup"><span data-stu-id="d36cc-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-134">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d36cc-134">-NoWait</span></span>
<span data-ttu-id="d36cc-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d36cc-135">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-136">-Porta</span><span class="sxs-lookup"><span data-stu-id="d36cc-136">-Port</span></span>
<span data-ttu-id="d36cc-137">Porta TCP dell'endpoint di database.</span><span class="sxs-lookup"><span data-stu-id="d36cc-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="d36cc-138">Specificato in Crea ora.</span><span class="sxs-lookup"><span data-stu-id="d36cc-138">Specified at create time.</span></span>
<span data-ttu-id="d36cc-139">Impostazione predefinita per una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="d36cc-139">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d36cc-140">-ResourceGroupName</span></span>
<span data-ttu-id="d36cc-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d36cc-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d36cc-142">-SubscriptionId</span></span>
<span data-ttu-id="d36cc-143">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d36cc-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d36cc-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d36cc-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36cc-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d36cc-145">-Confirm</span></span>
<span data-ttu-id="d36cc-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d36cc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d36cc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d36cc-147">-WhatIf</span></span>
<span data-ttu-id="d36cc-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d36cc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d36cc-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d36cc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d36cc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36cc-150">CommonParameters</span></span>
<span data-ttu-id="d36cc-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d36cc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36cc-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d36cc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36cc-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d36cc-153">INPUTS</span></span>

### <span data-ttu-id="d36cc-154">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="d36cc-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="d36cc-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d36cc-155">OUTPUTS</span></span>

### <span data-ttu-id="d36cc-156">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="d36cc-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="d36cc-157">Note</span><span class="sxs-lookup"><span data-stu-id="d36cc-157">NOTES</span></span>

<span data-ttu-id="d36cc-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d36cc-158">ALIASES</span></span>

<span data-ttu-id="d36cc-159">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d36cc-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d36cc-160">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d36cc-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d36cc-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d36cc-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d36cc-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d36cc-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d36cc-163">`[ClusterName <String>]`: Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d36cc-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="d36cc-164">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d36cc-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d36cc-165">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d36cc-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d36cc-166">`[Location <String>]`: L'area geografica in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d36cc-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="d36cc-167">`[OperationId <String>]`: Identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d36cc-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="d36cc-168">`[PrivateEndpointConnectionName <String>]`: Nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="d36cc-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="d36cc-169">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d36cc-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d36cc-170">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d36cc-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d36cc-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d36cc-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d36cc-172">MODULE <IModule [] >: set facoltativo di moduli Redis per l'abilitazione in questo database-i moduli possono essere aggiunti solo in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="d36cc-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="d36cc-173">`Name <String>`: Nome del modulo, ad esempio "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="d36cc-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="d36cc-174">`[Arg <String>]`: Opzioni di configurazione per il modulo, ad esempio "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="d36cc-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="d36cc-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d36cc-175">RELATED LINKS</span></span>

