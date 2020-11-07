---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677483"
---
# <span data-ttu-id="197b2-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="197b2-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="197b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="197b2-102">SYNOPSIS</span></span>
<span data-ttu-id="197b2-103">Modifica una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="197b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="197b2-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="197b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="197b2-105">DESCRIPTION</span></span>
<span data-ttu-id="197b2-106">Il cmdlet **set-AzRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="197b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="197b2-107">EXAMPLES</span></span>

### <span data-ttu-id="197b2-108">Esempio 1: modificare una cache di redis</span><span class="sxs-lookup"><span data-stu-id="197b2-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="197b2-109">Questo comando Aggiorna i criteri di MaxMemory per la cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="197b2-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="197b2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="197b2-110">PARAMETERS</span></span>

### <span data-ttu-id="197b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="197b2-111">-DefaultProfile</span></span>
<span data-ttu-id="197b2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="197b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="197b2-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="197b2-113">-EnableNonSslPort</span></span>
<span data-ttu-id="197b2-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="197b2-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="197b2-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="197b2-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="197b2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="197b2-116">-Name</span></span>
<span data-ttu-id="197b2-117">Specifica il nome della cache Redis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="197b2-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="197b2-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="197b2-118">-RedisConfiguration</span></span>
<span data-ttu-id="197b2-119">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="197b2-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="197b2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="197b2-121">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="197b2-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="197b2-122">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="197b2-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="197b2-123">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-123">Premium tier only.</span></span>
- <span data-ttu-id="197b2-124">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="197b2-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="197b2-125">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="197b2-126">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-126">Premium tier only.</span></span>
- <span data-ttu-id="197b2-127">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="197b2-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="197b2-128">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="197b2-129">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-129">Premium tier only.</span></span> 
- <span data-ttu-id="197b2-130">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="197b2-130">maxmemory-reserved.</span></span>
<span data-ttu-id="197b2-131">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="197b2-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="197b2-132">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-133">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="197b2-133">maxmemory-policy.</span></span>
<span data-ttu-id="197b2-134">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="197b2-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="197b2-135">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="197b2-135">All pricing tiers.</span></span> 
- <span data-ttu-id="197b2-136">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="197b2-136">notify-keyspace-events.</span></span>
<span data-ttu-id="197b2-137">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="197b2-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="197b2-138">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="197b2-139">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="197b2-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="197b2-140">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="197b2-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="197b2-141">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-142">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="197b2-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="197b2-143">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="197b2-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="197b2-144">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-145">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="197b2-145">set-max-intset-entries.</span></span>
<span data-ttu-id="197b2-146">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="197b2-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="197b2-147">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-148">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="197b2-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="197b2-149">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="197b2-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="197b2-150">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-151">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="197b2-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="197b2-152">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="197b2-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="197b2-153">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="197b2-154">database.</span><span class="sxs-lookup"><span data-stu-id="197b2-154">databases.</span></span>
<span data-ttu-id="197b2-155">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="197b2-155">Configures the number of databases.</span></span>
<span data-ttu-id="197b2-156">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="197b2-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="197b2-157">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="197b2-158">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="197b2-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="197b2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="197b2-159">-ResourceGroupName</span></span>
<span data-ttu-id="197b2-160">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="197b2-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="197b2-161">-ShardCount</span></span>
<span data-ttu-id="197b2-162">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="197b2-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="197b2-163">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="197b2-163">-Size</span></span>
<span data-ttu-id="197b2-164">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="197b2-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="197b2-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="197b2-165">Valid values are:</span></span> 
- <span data-ttu-id="197b2-166">P1</span><span class="sxs-lookup"><span data-stu-id="197b2-166">P1</span></span>
- <span data-ttu-id="197b2-167">P2</span><span class="sxs-lookup"><span data-stu-id="197b2-167">P2</span></span>
- <span data-ttu-id="197b2-168">P3</span><span class="sxs-lookup"><span data-stu-id="197b2-168">P3</span></span>
- <span data-ttu-id="197b2-169">P4</span><span class="sxs-lookup"><span data-stu-id="197b2-169">P4</span></span>
- <span data-ttu-id="197b2-170">C0</span><span class="sxs-lookup"><span data-stu-id="197b2-170">C0</span></span>
- <span data-ttu-id="197b2-171">C1</span><span class="sxs-lookup"><span data-stu-id="197b2-171">C1</span></span>
- <span data-ttu-id="197b2-172">C2</span><span class="sxs-lookup"><span data-stu-id="197b2-172">C2</span></span>
- <span data-ttu-id="197b2-173">C3</span><span class="sxs-lookup"><span data-stu-id="197b2-173">C3</span></span>
- <span data-ttu-id="197b2-174">C4</span><span class="sxs-lookup"><span data-stu-id="197b2-174">C4</span></span>
- <span data-ttu-id="197b2-175">C5</span><span class="sxs-lookup"><span data-stu-id="197b2-175">C5</span></span>
- <span data-ttu-id="197b2-176">C6</span><span class="sxs-lookup"><span data-stu-id="197b2-176">C6</span></span>
- <span data-ttu-id="197b2-177">250MB</span><span class="sxs-lookup"><span data-stu-id="197b2-177">250MB</span></span>
- <span data-ttu-id="197b2-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="197b2-178">1GB</span></span>
- <span data-ttu-id="197b2-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="197b2-179">2.5GB</span></span>
- <span data-ttu-id="197b2-180">6GB</span><span class="sxs-lookup"><span data-stu-id="197b2-180">6GB</span></span>
- <span data-ttu-id="197b2-181">13 GB</span><span class="sxs-lookup"><span data-stu-id="197b2-181">13GB</span></span>
- <span data-ttu-id="197b2-182">26GB</span><span class="sxs-lookup"><span data-stu-id="197b2-182">26GB</span></span>
- <span data-ttu-id="197b2-183">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="197b2-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="197b2-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="197b2-184">-Sku</span></span>
<span data-ttu-id="197b2-185">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="197b2-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="197b2-186">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="197b2-186">Valid values are:</span></span> 
- <span data-ttu-id="197b2-187">Base</span><span class="sxs-lookup"><span data-stu-id="197b2-187">Basic</span></span>
- <span data-ttu-id="197b2-188">Standard</span><span class="sxs-lookup"><span data-stu-id="197b2-188">Standard</span></span>
- <span data-ttu-id="197b2-189">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="197b2-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="197b2-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="197b2-190">-Tag</span></span>
<span data-ttu-id="197b2-191">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="197b2-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="197b2-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="197b2-192">-TenantSettings</span></span>
<span data-ttu-id="197b2-193">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="197b2-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="197b2-194">-Confermare</span><span class="sxs-lookup"><span data-stu-id="197b2-194">-Confirm</span></span>
<span data-ttu-id="197b2-195">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="197b2-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="197b2-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="197b2-196">-WhatIf</span></span>
<span data-ttu-id="197b2-197">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="197b2-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="197b2-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="197b2-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="197b2-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="197b2-199">CommonParameters</span></span>
<span data-ttu-id="197b2-200">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="197b2-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="197b2-201">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="197b2-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="197b2-202">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="197b2-202">INPUTS</span></span>

### <span data-ttu-id="197b2-203">System. String</span><span class="sxs-lookup"><span data-stu-id="197b2-203">System.String</span></span>

### <span data-ttu-id="197b2-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="197b2-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="197b2-205">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="197b2-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="197b2-206">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="197b2-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="197b2-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="197b2-207">OUTPUTS</span></span>

### <span data-ttu-id="197b2-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="197b2-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="197b2-209">Note</span><span class="sxs-lookup"><span data-stu-id="197b2-209">NOTES</span></span>

## <span data-ttu-id="197b2-210">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="197b2-210">RELATED LINKS</span></span>

[<span data-ttu-id="197b2-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="197b2-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="197b2-212">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="197b2-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="197b2-213">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="197b2-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


