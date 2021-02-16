---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201950"
---
# <span data-ttu-id="3ff01-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="3ff01-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="3ff01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff01-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff01-103">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="3ff01-103">Updates a database</span></span>

## <span data-ttu-id="3ff01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ff01-104">SYNTAX</span></span>

### <span data-ttu-id="3ff01-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ff01-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ff01-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3ff01-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3ff01-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ff01-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff01-108">Aggiorna un database</span><span class="sxs-lookup"><span data-stu-id="3ff01-108">Updates a database</span></span>

## <span data-ttu-id="3ff01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ff01-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff01-110">Esempio 1: Aggiornare il protocollo client</span><span class="sxs-lookup"><span data-stu-id="3ff01-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3ff01-111">Questo comando aggiorna il protocollo client del database per la cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="3ff01-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3ff01-112">Esempio 2: Aggiornare il protocollo client e i criteri di sgombero</span><span class="sxs-lookup"><span data-stu-id="3ff01-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3ff01-113">Questo comando aggiorna il protocollo client e i criteri di evizione del database per la cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="3ff01-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3ff01-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff01-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff01-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ff01-115">-AsJob</span></span>
<span data-ttu-id="3ff01-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3ff01-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3ff01-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3ff01-117">-ClientProtocol</span></span>
<span data-ttu-id="3ff01-118">Specifica se i client ridisposizione possono connettersi usando protocolli didis con crittografia TLS o testo normale.</span><span class="sxs-lookup"><span data-stu-id="3ff01-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="3ff01-119">Il valore predefinito è TLS-encrypted.</span><span class="sxs-lookup"><span data-stu-id="3ff01-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="3ff01-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="3ff01-120">-ClusteringPolicy</span></span>
<span data-ttu-id="3ff01-121">Criterio di clustering: il valore predefinito è OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="3ff01-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="3ff01-122">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-122">Specified at create time.</span></span>

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

### <span data-ttu-id="3ff01-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3ff01-123">-ClusterName</span></span>
<span data-ttu-id="3ff01-124">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3ff01-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3ff01-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff01-125">-DefaultProfile</span></span>
<span data-ttu-id="3ff01-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff01-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff01-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="3ff01-127">-EvictionPolicy</span></span>
<span data-ttu-id="3ff01-128">Criterio di evizione di ridisposizione - il valore predefinito è VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="3ff01-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="3ff01-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff01-129">-InputObject</span></span>
<span data-ttu-id="3ff01-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3ff01-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ff01-131">-Module</span><span class="sxs-lookup"><span data-stu-id="3ff01-131">-Module</span></span>
<span data-ttu-id="3ff01-132">Set facoltativo di ridisposizione dei moduli da abilitare in questo database: i moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="3ff01-133">Per creare, vedere la sezione NOTE per le proprietà MODULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3ff01-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ff01-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ff01-134">-NoWait</span></span>
<span data-ttu-id="3ff01-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3ff01-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ff01-136">-Porta</span><span class="sxs-lookup"><span data-stu-id="3ff01-136">-Port</span></span>
<span data-ttu-id="3ff01-137">Porta TCP dell'endpoint di database.</span><span class="sxs-lookup"><span data-stu-id="3ff01-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="3ff01-138">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-138">Specified at create time.</span></span>
<span data-ttu-id="3ff01-139">L'impostazione predefinita è una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="3ff01-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="3ff01-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff01-140">-ResourceGroupName</span></span>
<span data-ttu-id="3ff01-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ff01-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ff01-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ff01-142">-SubscriptionId</span></span>
<span data-ttu-id="3ff01-143">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff01-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ff01-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3ff01-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ff01-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ff01-145">-Confirm</span></span>
<span data-ttu-id="3ff01-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff01-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff01-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff01-147">-WhatIf</span></span>
<span data-ttu-id="3ff01-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ff01-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff01-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ff01-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff01-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff01-150">CommonParameters</span></span>
<span data-ttu-id="3ff01-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff01-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff01-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ff01-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff01-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ff01-153">INPUTS</span></span>

### <span data-ttu-id="3ff01-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="3ff01-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="3ff01-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ff01-155">OUTPUTS</span></span>

### <span data-ttu-id="3ff01-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="3ff01-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="3ff01-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ff01-157">NOTES</span></span>

<span data-ttu-id="3ff01-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3ff01-158">ALIASES</span></span>

<span data-ttu-id="3ff01-159">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3ff01-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ff01-160">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3ff01-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ff01-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ff01-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ff01-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="3ff01-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ff01-163">`[ClusterName <String>]`: nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3ff01-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="3ff01-164">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="3ff01-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3ff01-165">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3ff01-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ff01-166">`[Location <String>]`: l'area in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="3ff01-167">`[OperationId <String>]`: l'identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="3ff01-168">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="3ff01-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="3ff01-169">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ff01-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3ff01-170">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff01-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3ff01-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3ff01-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3ff01-172">MODULE <IModule[]>: set facoltativo di ridisposizione dei moduli da abilitare nel database. I moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3ff01-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="3ff01-173">`Name <String>`: il nome del modulo, ad esempio "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="3ff01-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="3ff01-174">`[Arg <String>]`: le opzioni di configurazione per il modulo, ad esempio "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="3ff01-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="3ff01-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ff01-175">RELATED LINKS</span></span>

