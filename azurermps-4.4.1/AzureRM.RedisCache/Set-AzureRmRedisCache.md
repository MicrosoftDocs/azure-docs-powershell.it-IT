---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513040"
---
# <span data-ttu-id="429aa-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="429aa-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="429aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="429aa-102">SYNOPSIS</span></span>
<span data-ttu-id="429aa-103">Modifica una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="429aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="429aa-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="429aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429aa-105">DESCRIPTION</span></span>
<span data-ttu-id="429aa-106">Il cmdlet **set-AzureRmRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="429aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="429aa-107">EXAMPLES</span></span>

### <span data-ttu-id="429aa-108">Esempio 1: modificare una cache di redis</span><span class="sxs-lookup"><span data-stu-id="429aa-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
```

<span data-ttu-id="429aa-109">Questo comando Aggiorna i criteri di MaxMemory per la cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="429aa-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="429aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="429aa-110">PARAMETERS</span></span>

### <span data-ttu-id="429aa-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="429aa-111">-EnableNonSslPort</span></span>
<span data-ttu-id="429aa-112">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="429aa-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="429aa-113">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="429aa-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="429aa-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="429aa-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="429aa-115">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="429aa-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="429aa-116">Usa il parametro *RedisConfiguration* per impostare i criteri di MaxMemory.</span><span class="sxs-lookup"><span data-stu-id="429aa-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="429aa-117">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="429aa-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="429aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="429aa-118">-Name</span></span>
<span data-ttu-id="429aa-119">Specifica il nome della cache Redis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="429aa-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="429aa-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="429aa-120">-RedisConfiguration</span></span>
<span data-ttu-id="429aa-121">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="429aa-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="429aa-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="429aa-123">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="429aa-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="429aa-124">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="429aa-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="429aa-125">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-125">Premium tier only.</span></span>
- <span data-ttu-id="429aa-126">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="429aa-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="429aa-127">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="429aa-128">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-128">Premium tier only.</span></span>
- <span data-ttu-id="429aa-129">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="429aa-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="429aa-130">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="429aa-131">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-131">Premium tier only.</span></span> 
- <span data-ttu-id="429aa-132">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="429aa-132">maxmemory-reserved.</span></span>
<span data-ttu-id="429aa-133">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="429aa-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="429aa-134">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-135">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="429aa-135">maxmemory-policy.</span></span>
<span data-ttu-id="429aa-136">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="429aa-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="429aa-137">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="429aa-137">All pricing tiers.</span></span> 
- <span data-ttu-id="429aa-138">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="429aa-138">notify-keyspace-events.</span></span>
<span data-ttu-id="429aa-139">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="429aa-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="429aa-140">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="429aa-141">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="429aa-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="429aa-142">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="429aa-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="429aa-143">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-144">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="429aa-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="429aa-145">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="429aa-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="429aa-146">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-147">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="429aa-147">set-max-intset-entries.</span></span>
<span data-ttu-id="429aa-148">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="429aa-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="429aa-149">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-150">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="429aa-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="429aa-151">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="429aa-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="429aa-152">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-153">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="429aa-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="429aa-154">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="429aa-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="429aa-155">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="429aa-156">database.</span><span class="sxs-lookup"><span data-stu-id="429aa-156">databases.</span></span>
<span data-ttu-id="429aa-157">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="429aa-157">Configures the number of databases.</span></span>
<span data-ttu-id="429aa-158">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="429aa-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="429aa-159">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="429aa-160">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="429aa-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="429aa-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="429aa-161">-ResourceGroupName</span></span>
<span data-ttu-id="429aa-162">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="429aa-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="429aa-163">-ShardCount</span></span>
<span data-ttu-id="429aa-164">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="429aa-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="429aa-165">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="429aa-165">-Size</span></span>
<span data-ttu-id="429aa-166">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="429aa-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="429aa-167">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="429aa-167">Valid values are:</span></span> 

- <span data-ttu-id="429aa-168">P1</span><span class="sxs-lookup"><span data-stu-id="429aa-168">P1</span></span>
- <span data-ttu-id="429aa-169">P2</span><span class="sxs-lookup"><span data-stu-id="429aa-169">P2</span></span>
- <span data-ttu-id="429aa-170">P3</span><span class="sxs-lookup"><span data-stu-id="429aa-170">P3</span></span>
- <span data-ttu-id="429aa-171">P4</span><span class="sxs-lookup"><span data-stu-id="429aa-171">P4</span></span>
- <span data-ttu-id="429aa-172">C0</span><span class="sxs-lookup"><span data-stu-id="429aa-172">C0</span></span>
- <span data-ttu-id="429aa-173">C1</span><span class="sxs-lookup"><span data-stu-id="429aa-173">C1</span></span>
- <span data-ttu-id="429aa-174">C2</span><span class="sxs-lookup"><span data-stu-id="429aa-174">C2</span></span>
- <span data-ttu-id="429aa-175">C3</span><span class="sxs-lookup"><span data-stu-id="429aa-175">C3</span></span>
- <span data-ttu-id="429aa-176">C4</span><span class="sxs-lookup"><span data-stu-id="429aa-176">C4</span></span>
- <span data-ttu-id="429aa-177">C5</span><span class="sxs-lookup"><span data-stu-id="429aa-177">C5</span></span>
- <span data-ttu-id="429aa-178">C6</span><span class="sxs-lookup"><span data-stu-id="429aa-178">C6</span></span>
- <span data-ttu-id="429aa-179">250MB</span><span class="sxs-lookup"><span data-stu-id="429aa-179">250MB</span></span>
- <span data-ttu-id="429aa-180">1 GB</span><span class="sxs-lookup"><span data-stu-id="429aa-180">1GB</span></span>
- <span data-ttu-id="429aa-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="429aa-181">2.5GB</span></span>
- <span data-ttu-id="429aa-182">6GB</span><span class="sxs-lookup"><span data-stu-id="429aa-182">6GB</span></span>
- <span data-ttu-id="429aa-183">13 GB</span><span class="sxs-lookup"><span data-stu-id="429aa-183">13GB</span></span>
- <span data-ttu-id="429aa-184">26GB</span><span class="sxs-lookup"><span data-stu-id="429aa-184">26GB</span></span>
- <span data-ttu-id="429aa-185">53GB</span><span class="sxs-lookup"><span data-stu-id="429aa-185">53GB</span></span>

<span data-ttu-id="429aa-186">Il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="429aa-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429aa-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="429aa-187">-Sku</span></span>
<span data-ttu-id="429aa-188">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="429aa-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="429aa-189">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="429aa-189">Valid values are:</span></span> 

- <span data-ttu-id="429aa-190">Base</span><span class="sxs-lookup"><span data-stu-id="429aa-190">Basic</span></span>
- <span data-ttu-id="429aa-191">Standard</span><span class="sxs-lookup"><span data-stu-id="429aa-191">Standard</span></span>
- <span data-ttu-id="429aa-192">Premium</span><span class="sxs-lookup"><span data-stu-id="429aa-192">Premium</span></span>

<span data-ttu-id="429aa-193">Il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="429aa-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="429aa-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="429aa-194">-TenantSettings</span></span>
<span data-ttu-id="429aa-195">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="429aa-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="429aa-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429aa-196">-DefaultProfile</span></span>
<span data-ttu-id="429aa-197">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="429aa-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429aa-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429aa-198">CommonParameters</span></span>
<span data-ttu-id="429aa-199">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429aa-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429aa-200">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="429aa-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429aa-201">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="429aa-201">INPUTS</span></span>

### <span data-ttu-id="429aa-202">Nessuno</span><span class="sxs-lookup"><span data-stu-id="429aa-202">None</span></span>
<span data-ttu-id="429aa-203">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="429aa-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="429aa-204">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="429aa-204">OUTPUTS</span></span>

### <span data-ttu-id="429aa-205">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="429aa-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="429aa-206">Restituisce tutti gli attributi di una cache di redis, inclusi i tasti di scelta primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="429aa-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="429aa-207">Note</span><span class="sxs-lookup"><span data-stu-id="429aa-207">NOTES</span></span>

## <span data-ttu-id="429aa-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="429aa-208">RELATED LINKS</span></span>

[<span data-ttu-id="429aa-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="429aa-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="429aa-210">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="429aa-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="429aa-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="429aa-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


