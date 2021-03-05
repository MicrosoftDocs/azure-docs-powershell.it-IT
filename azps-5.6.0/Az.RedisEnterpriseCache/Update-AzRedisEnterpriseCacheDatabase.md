---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 882bbb9f45720114fe3ca12e8094e1464b895881
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000685"
---
# <span data-ttu-id="3c578-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="3c578-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="3c578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c578-102">SYNOPSIS</span></span>
<span data-ttu-id="3c578-103">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="3c578-103">Updates a database</span></span>

## <span data-ttu-id="3c578-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c578-104">SYNTAX</span></span>

### <span data-ttu-id="3c578-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c578-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c578-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3c578-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3c578-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c578-107">DESCRIPTION</span></span>
<span data-ttu-id="3c578-108">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="3c578-108">Updates a database</span></span>

## <span data-ttu-id="3c578-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c578-109">EXAMPLES</span></span>

### <span data-ttu-id="3c578-110">Esempio 1: Aggiornare il protocollo client</span><span class="sxs-lookup"><span data-stu-id="3c578-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3c578-111">Questo comando aggiorna il protocollo client del database per la cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="3c578-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3c578-112">Esempio 2: Aggiornare il protocollo client e i criteri di sgombero</span><span class="sxs-lookup"><span data-stu-id="3c578-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3c578-113">Questo comando aggiorna il protocollo client e i criteri di evizione del database per la cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="3c578-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3c578-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c578-114">PARAMETERS</span></span>

### <span data-ttu-id="3c578-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c578-115">-AsJob</span></span>
<span data-ttu-id="3c578-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3c578-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3c578-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3c578-117">-ClientProtocol</span></span>
<span data-ttu-id="3c578-118">Specifica se i client di ridisposizione possono connettersi usando protocolli di ridisposizione tls crittografati con TLS o testo normale.</span><span class="sxs-lookup"><span data-stu-id="3c578-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="3c578-119">Il valore predefinito è tls crittografato.</span><span class="sxs-lookup"><span data-stu-id="3c578-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="3c578-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="3c578-120">-ClusteringPolicy</span></span>
<span data-ttu-id="3c578-121">Criterio di clustering: il valore predefinito è OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="3c578-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="3c578-122">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-122">Specified at create time.</span></span>

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

### <span data-ttu-id="3c578-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3c578-123">-ClusterName</span></span>
<span data-ttu-id="3c578-124">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3c578-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3c578-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c578-125">-DefaultProfile</span></span>
<span data-ttu-id="3c578-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c578-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c578-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c578-127">-EvictionPolicy</span></span>
<span data-ttu-id="3c578-128">Criterio di ridisposizione - il valore predefinito è VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="3c578-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="3c578-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c578-129">-InputObject</span></span>
<span data-ttu-id="3c578-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3c578-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c578-131">-Module</span><span class="sxs-lookup"><span data-stu-id="3c578-131">-Module</span></span>
<span data-ttu-id="3c578-132">Set facoltativo di ridisposizione dei moduli da abilitare in questo database: i moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="3c578-133">Per creare, vedere la sezione NOTE per le proprietà MODULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3c578-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c578-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c578-134">-NoWait</span></span>
<span data-ttu-id="3c578-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3c578-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c578-136">-Port</span><span class="sxs-lookup"><span data-stu-id="3c578-136">-Port</span></span>
<span data-ttu-id="3c578-137">Porta TCP dell'endpoint di database.</span><span class="sxs-lookup"><span data-stu-id="3c578-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="3c578-138">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-138">Specified at create time.</span></span>
<span data-ttu-id="3c578-139">L'impostazione predefinita è una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="3c578-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="3c578-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c578-140">-ResourceGroupName</span></span>
<span data-ttu-id="3c578-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c578-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c578-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c578-142">-SubscriptionId</span></span>
<span data-ttu-id="3c578-143">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c578-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c578-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c578-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c578-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c578-145">-Confirm</span></span>
<span data-ttu-id="3c578-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c578-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c578-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c578-147">-WhatIf</span></span>
<span data-ttu-id="3c578-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c578-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c578-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c578-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c578-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c578-150">CommonParameters</span></span>
<span data-ttu-id="3c578-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c578-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c578-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c578-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c578-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c578-153">INPUTS</span></span>

### <span data-ttu-id="3c578-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="3c578-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="3c578-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c578-155">OUTPUTS</span></span>

### <span data-ttu-id="3c578-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="3c578-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="3c578-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c578-157">NOTES</span></span>

<span data-ttu-id="3c578-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3c578-158">ALIASES</span></span>

<span data-ttu-id="3c578-159">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3c578-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c578-160">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3c578-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c578-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c578-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c578-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3c578-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c578-163">`[ClusterName <String>]`: nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3c578-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="3c578-164">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="3c578-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3c578-165">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3c578-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c578-166">`[Location <String>]`: l'area in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="3c578-167">`[OperationId <String>]`: l'identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="3c578-168">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="3c578-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="3c578-169">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c578-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3c578-170">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c578-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3c578-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c578-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3c578-172">MODULE <IModule[]>: set facoltativo di ridisposizione dei moduli da abilitare nel database. I moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3c578-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="3c578-173">`Name <String>`: il nome del modulo, ad esempio "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="3c578-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="3c578-174">`[Arg <String>]`: le opzioni di configurazione per il modulo, ad esempio "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="3c578-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="3c578-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c578-175">RELATED LINKS</span></span>

