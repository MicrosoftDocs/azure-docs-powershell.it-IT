---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000910"
---
# <span data-ttu-id="0ddac-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ddac-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="0ddac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ddac-102">SYNOPSIS</span></span>
<span data-ttu-id="0ddac-103">Modifica una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="0ddac-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="0ddac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ddac-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ddac-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ddac-105">DESCRIPTION</span></span>
<span data-ttu-id="0ddac-106">Il cmdlet **Set-AzRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="0ddac-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="0ddac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ddac-107">EXAMPLES</span></span>

### <span data-ttu-id="0ddac-108">Esempio 1: Modificare una cache di Ridisposizione</span><span class="sxs-lookup"><span data-stu-id="0ddac-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="0ddac-109">Questo comando aggiorna i criteri di maxmemory per la cache di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="0ddac-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="0ddac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ddac-110">PARAMETERS</span></span>

### <span data-ttu-id="0ddac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ddac-111">-DefaultProfile</span></span>
<span data-ttu-id="0ddac-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ddac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="0ddac-113">-EnableNonSslPort</span></span>
<span data-ttu-id="0ddac-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0ddac-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="0ddac-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="0ddac-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0ddac-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="0ddac-117">Specificare la versione di TLS richiesta dai client per connettersi alla cache.</span><span class="sxs-lookup"><span data-stu-id="0ddac-117">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0ddac-118">-Name</span></span>
<span data-ttu-id="0ddac-119">Specifica il nome della cache di Ridis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0ddac-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ddac-120">-RedisConfiguration</span></span>
<span data-ttu-id="0ddac-121">Specifica le impostazioni di configurazione di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="0ddac-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="0ddac-122">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="0ddac-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ddac-123">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="0ddac-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="0ddac-124">Specifica che la persistenza dei dati di Ridisposizione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0ddac-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="0ddac-125">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-125">Premium tier only.</span></span>
- <span data-ttu-id="0ddac-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="0ddac-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="0ddac-127">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="0ddac-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="0ddac-128">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-128">Premium tier only.</span></span>
- <span data-ttu-id="0ddac-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="0ddac-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="0ddac-130">Specifica la frequenza di backup per la persistenza dei dati di Redis.</span><span class="sxs-lookup"><span data-stu-id="0ddac-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="0ddac-131">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-131">Premium tier only.</span></span> 
- <span data-ttu-id="0ddac-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="0ddac-132">maxmemory-reserved.</span></span>
<span data-ttu-id="0ddac-133">Configura la memoria riservata ai processi non cache.</span><span class="sxs-lookup"><span data-stu-id="0ddac-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="0ddac-134">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="0ddac-135">maxmemory-policy.</span></span>
<span data-ttu-id="0ddac-136">Configura i criteri di sgombero per la cache.</span><span class="sxs-lookup"><span data-stu-id="0ddac-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="0ddac-137">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="0ddac-137">All pricing tiers.</span></span> 
- <span data-ttu-id="0ddac-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="0ddac-138">notify-keyspace-events.</span></span>
<span data-ttu-id="0ddac-139">Configura le notifiche di keyspace.</span><span class="sxs-lookup"><span data-stu-id="0ddac-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="0ddac-140">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="0ddac-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="0ddac-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="0ddac-142">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="0ddac-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0ddac-143">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="0ddac-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="0ddac-145">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="0ddac-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0ddac-146">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="0ddac-147">set-max-intset-entries.</span></span>
<span data-ttu-id="0ddac-148">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="0ddac-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0ddac-149">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="0ddac-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="0ddac-151">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="0ddac-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0ddac-152">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="0ddac-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="0ddac-154">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="0ddac-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0ddac-155">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0ddac-156">database.</span><span class="sxs-lookup"><span data-stu-id="0ddac-156">databases.</span></span>
<span data-ttu-id="0ddac-157">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="0ddac-157">Configures the number of databases.</span></span>
<span data-ttu-id="0ddac-158">Questa proprietà può essere configurata solo durante la creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="0ddac-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="0ddac-159">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="0ddac-160">Per altre informazioni, vedere Gestire la cache di Azure Redis con Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="0ddac-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ddac-161">-ResourceGroupName</span></span>
<span data-ttu-id="0ddac-162">Specifica il nome del gruppo di risorse che contiene la cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="0ddac-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="0ddac-163">-ShardCount</span></span>
<span data-ttu-id="0ddac-164">Specifica il numero di parti da creare in una cache cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="0ddac-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-165">-Size</span><span class="sxs-lookup"><span data-stu-id="0ddac-165">-Size</span></span>
<span data-ttu-id="0ddac-166">Specifica le dimensioni della cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="0ddac-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="0ddac-167">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0ddac-167">Valid values are:</span></span> 
- <span data-ttu-id="0ddac-168">P1</span><span class="sxs-lookup"><span data-stu-id="0ddac-168">P1</span></span>
- <span data-ttu-id="0ddac-169">P2</span><span class="sxs-lookup"><span data-stu-id="0ddac-169">P2</span></span>
- <span data-ttu-id="0ddac-170">P3</span><span class="sxs-lookup"><span data-stu-id="0ddac-170">P3</span></span>
- <span data-ttu-id="0ddac-171">P4</span><span class="sxs-lookup"><span data-stu-id="0ddac-171">P4</span></span>
- <span data-ttu-id="0ddac-172">P5</span><span class="sxs-lookup"><span data-stu-id="0ddac-172">P5</span></span>
- <span data-ttu-id="0ddac-173">C0</span><span class="sxs-lookup"><span data-stu-id="0ddac-173">C0</span></span>
- <span data-ttu-id="0ddac-174">C1</span><span class="sxs-lookup"><span data-stu-id="0ddac-174">C1</span></span>
- <span data-ttu-id="0ddac-175">C2</span><span class="sxs-lookup"><span data-stu-id="0ddac-175">C2</span></span>
- <span data-ttu-id="0ddac-176">C3</span><span class="sxs-lookup"><span data-stu-id="0ddac-176">C3</span></span>
- <span data-ttu-id="0ddac-177">C4</span><span class="sxs-lookup"><span data-stu-id="0ddac-177">C4</span></span>
- <span data-ttu-id="0ddac-178">C5</span><span class="sxs-lookup"><span data-stu-id="0ddac-178">C5</span></span>
- <span data-ttu-id="0ddac-179">C6</span><span class="sxs-lookup"><span data-stu-id="0ddac-179">C6</span></span>
- <span data-ttu-id="0ddac-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="0ddac-180">250MB</span></span>
- <span data-ttu-id="0ddac-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-181">1GB</span></span>
- <span data-ttu-id="0ddac-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-182">2.5GB</span></span>
- <span data-ttu-id="0ddac-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-183">6GB</span></span>
- <span data-ttu-id="0ddac-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-184">13GB</span></span>
- <span data-ttu-id="0ddac-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-185">26GB</span></span>
- <span data-ttu-id="0ddac-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="0ddac-186">53GB</span></span>
- <span data-ttu-id="0ddac-187">120 GB Il valore predefinito è 1 GB o C1.</span><span class="sxs-lookup"><span data-stu-id="0ddac-187">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="0ddac-188">-Sku</span></span>
<span data-ttu-id="0ddac-189">Specifica lo SKU della cache di Ridis da creare.</span><span class="sxs-lookup"><span data-stu-id="0ddac-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="0ddac-190">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0ddac-190">Valid values are:</span></span> 
- <span data-ttu-id="0ddac-191">Di base</span><span class="sxs-lookup"><span data-stu-id="0ddac-191">Basic</span></span>
- <span data-ttu-id="0ddac-192">Standard</span><span class="sxs-lookup"><span data-stu-id="0ddac-192">Standard</span></span>
- <span data-ttu-id="0ddac-193">Premium Il valore predefinito è Standard.</span><span class="sxs-lookup"><span data-stu-id="0ddac-193">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ddac-194">-Tag</span></span>
<span data-ttu-id="0ddac-195">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="0ddac-195">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="0ddac-196">-TenantSettings</span></span>
<span data-ttu-id="0ddac-197">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="0ddac-197">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddac-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ddac-198">-Confirm</span></span>
<span data-ttu-id="0ddac-199">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ddac-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ddac-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ddac-200">-WhatIf</span></span>
<span data-ttu-id="0ddac-201">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ddac-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ddac-202">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ddac-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ddac-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ddac-203">CommonParameters</span></span>
<span data-ttu-id="0ddac-204">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ddac-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ddac-205">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ddac-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ddac-206">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ddac-206">INPUTS</span></span>

### <span data-ttu-id="0ddac-207">System.String</span><span class="sxs-lookup"><span data-stu-id="0ddac-207">System.String</span></span>

### <span data-ttu-id="0ddac-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ddac-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0ddac-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ddac-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ddac-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ddac-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0ddac-211">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ddac-211">OUTPUTS</span></span>

### <span data-ttu-id="0ddac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0ddac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="0ddac-213">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ddac-213">NOTES</span></span>

## <span data-ttu-id="0ddac-214">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ddac-214">RELATED LINKS</span></span>

[<span data-ttu-id="0ddac-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ddac-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="0ddac-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ddac-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="0ddac-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ddac-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


