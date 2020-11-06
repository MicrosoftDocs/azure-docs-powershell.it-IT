---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514164"
---
# <span data-ttu-id="b2784-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b2784-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="b2784-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2784-102">SYNOPSIS</span></span>
<span data-ttu-id="b2784-103">Modifica una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2784-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2784-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2784-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2784-105">DESCRIPTION</span></span>
<span data-ttu-id="b2784-106">Il cmdlet **set-AzureRmRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="b2784-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2784-107">EXAMPLES</span></span>

### <span data-ttu-id="b2784-108">Esempio 1: modificare una cache di redis</span><span class="sxs-lookup"><span data-stu-id="b2784-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="b2784-109">Questo comando Aggiorna i criteri di MaxMemory per la cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="b2784-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="b2784-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2784-110">PARAMETERS</span></span>

### <span data-ttu-id="b2784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2784-111">-DefaultProfile</span></span>
<span data-ttu-id="b2784-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2784-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b2784-113">-EnableNonSslPort</span></span>
<span data-ttu-id="b2784-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b2784-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b2784-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="b2784-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="b2784-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="b2784-117">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="b2784-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="b2784-118">Usa il parametro *RedisConfiguration* per impostare i criteri di MaxMemory.</span><span class="sxs-lookup"><span data-stu-id="b2784-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="b2784-119">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b2784-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2784-120">-Name</span></span>
<span data-ttu-id="b2784-121">Specifica il nome della cache Redis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b2784-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2784-122">-RedisConfiguration</span></span>
<span data-ttu-id="b2784-123">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b2784-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2784-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2784-125">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="b2784-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="b2784-126">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b2784-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b2784-127">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-127">Premium tier only.</span></span>
- <span data-ttu-id="b2784-128">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="b2784-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b2784-129">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b2784-130">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-130">Premium tier only.</span></span>
- <span data-ttu-id="b2784-131">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="b2784-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="b2784-132">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b2784-133">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-133">Premium tier only.</span></span> 
- <span data-ttu-id="b2784-134">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="b2784-134">maxmemory-reserved.</span></span>
<span data-ttu-id="b2784-135">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="b2784-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b2784-136">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-137">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="b2784-137">maxmemory-policy.</span></span>
<span data-ttu-id="b2784-138">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="b2784-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b2784-139">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="b2784-139">All pricing tiers.</span></span> 
- <span data-ttu-id="b2784-140">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="b2784-140">notify-keyspace-events.</span></span>
<span data-ttu-id="b2784-141">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="b2784-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="b2784-142">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b2784-143">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="b2784-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b2784-144">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="b2784-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b2784-145">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-146">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="b2784-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b2784-147">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="b2784-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b2784-148">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-149">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="b2784-149">set-max-intset-entries.</span></span>
<span data-ttu-id="b2784-150">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="b2784-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b2784-151">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-152">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="b2784-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b2784-153">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="b2784-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b2784-154">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-155">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="b2784-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b2784-156">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="b2784-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b2784-157">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b2784-158">database.</span><span class="sxs-lookup"><span data-stu-id="b2784-158">databases.</span></span>
<span data-ttu-id="b2784-159">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="b2784-159">Configures the number of databases.</span></span>
<span data-ttu-id="b2784-160">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="b2784-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b2784-161">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="b2784-162">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b2784-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2784-163">-ResourceGroupName</span></span>
<span data-ttu-id="b2784-164">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b2784-165">-ShardCount</span></span>
<span data-ttu-id="b2784-166">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="b2784-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-167">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="b2784-167">-Size</span></span>
<span data-ttu-id="b2784-168">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b2784-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b2784-169">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b2784-169">Valid values are:</span></span> 

- <span data-ttu-id="b2784-170">P1</span><span class="sxs-lookup"><span data-stu-id="b2784-170">P1</span></span>
- <span data-ttu-id="b2784-171">P2</span><span class="sxs-lookup"><span data-stu-id="b2784-171">P2</span></span>
- <span data-ttu-id="b2784-172">P3</span><span class="sxs-lookup"><span data-stu-id="b2784-172">P3</span></span>
- <span data-ttu-id="b2784-173">P4</span><span class="sxs-lookup"><span data-stu-id="b2784-173">P4</span></span>
- <span data-ttu-id="b2784-174">C0</span><span class="sxs-lookup"><span data-stu-id="b2784-174">C0</span></span>
- <span data-ttu-id="b2784-175">C1</span><span class="sxs-lookup"><span data-stu-id="b2784-175">C1</span></span>
- <span data-ttu-id="b2784-176">C2</span><span class="sxs-lookup"><span data-stu-id="b2784-176">C2</span></span>
- <span data-ttu-id="b2784-177">C3</span><span class="sxs-lookup"><span data-stu-id="b2784-177">C3</span></span>
- <span data-ttu-id="b2784-178">C4</span><span class="sxs-lookup"><span data-stu-id="b2784-178">C4</span></span>
- <span data-ttu-id="b2784-179">C5</span><span class="sxs-lookup"><span data-stu-id="b2784-179">C5</span></span>
- <span data-ttu-id="b2784-180">C6</span><span class="sxs-lookup"><span data-stu-id="b2784-180">C6</span></span>
- <span data-ttu-id="b2784-181">250MB</span><span class="sxs-lookup"><span data-stu-id="b2784-181">250MB</span></span>
- <span data-ttu-id="b2784-182">1 GB</span><span class="sxs-lookup"><span data-stu-id="b2784-182">1GB</span></span>
- <span data-ttu-id="b2784-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="b2784-183">2.5GB</span></span>
- <span data-ttu-id="b2784-184">6GB</span><span class="sxs-lookup"><span data-stu-id="b2784-184">6GB</span></span>
- <span data-ttu-id="b2784-185">13 GB</span><span class="sxs-lookup"><span data-stu-id="b2784-185">13GB</span></span>
- <span data-ttu-id="b2784-186">26GB</span><span class="sxs-lookup"><span data-stu-id="b2784-186">26GB</span></span>
- <span data-ttu-id="b2784-187">53GB</span><span class="sxs-lookup"><span data-stu-id="b2784-187">53GB</span></span>

<span data-ttu-id="b2784-188">Il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="b2784-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="b2784-189">-Sku</span></span>
<span data-ttu-id="b2784-190">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="b2784-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b2784-191">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b2784-191">Valid values are:</span></span> 

- <span data-ttu-id="b2784-192">Base</span><span class="sxs-lookup"><span data-stu-id="b2784-192">Basic</span></span>
- <span data-ttu-id="b2784-193">Standard</span><span class="sxs-lookup"><span data-stu-id="b2784-193">Standard</span></span>
- <span data-ttu-id="b2784-194">Premium</span><span class="sxs-lookup"><span data-stu-id="b2784-194">Premium</span></span>

<span data-ttu-id="b2784-195">Il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="b2784-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-196">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2784-196">-Tag</span></span>
<span data-ttu-id="b2784-197">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="b2784-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b2784-198">-TenantSettings</span></span>
<span data-ttu-id="b2784-199">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="b2784-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2784-200">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2784-200">-Confirm</span></span>
<span data-ttu-id="b2784-201">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2784-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2784-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2784-202">-WhatIf</span></span>
<span data-ttu-id="b2784-203">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2784-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2784-204">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2784-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2784-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2784-205">CommonParameters</span></span>
<span data-ttu-id="b2784-206">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2784-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2784-207">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2784-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2784-208">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2784-208">INPUTS</span></span>

### <span data-ttu-id="b2784-209">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2784-209">None</span></span>
<span data-ttu-id="b2784-210">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="b2784-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b2784-211">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2784-211">OUTPUTS</span></span>

### <span data-ttu-id="b2784-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b2784-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="b2784-213">Restituisce tutti gli attributi di una cache di redis, inclusi i tasti di scelta primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="b2784-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="b2784-214">Note</span><span class="sxs-lookup"><span data-stu-id="b2784-214">NOTES</span></span>

## <span data-ttu-id="b2784-215">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2784-215">RELATED LINKS</span></span>

[<span data-ttu-id="b2784-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b2784-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b2784-217">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b2784-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b2784-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b2784-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


