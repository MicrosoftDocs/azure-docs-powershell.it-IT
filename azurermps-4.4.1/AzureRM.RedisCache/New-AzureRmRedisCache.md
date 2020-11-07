---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685882"
---
# <span data-ttu-id="40bb5-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="40bb5-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="40bb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="40bb5-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40bb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40bb5-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40bb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="40bb5-106">Il cmdlet **New-AzureRmRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="40bb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40bb5-107">EXAMPLES</span></span>

### <span data-ttu-id="40bb5-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="40bb5-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="40bb5-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="40bb5-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="40bb5-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="40bb5-111">Questo comando crea una cache Redis o aggiorna la cache Redis se esiste già.</span><span class="sxs-lookup"><span data-stu-id="40bb5-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="40bb5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40bb5-112">PARAMETERS</span></span>

### <span data-ttu-id="40bb5-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="40bb5-113">-EnableNonSslPort</span></span>
<span data-ttu-id="40bb5-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="40bb5-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="40bb5-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="40bb5-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="40bb5-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="40bb5-116">-Location</span></span>
<span data-ttu-id="40bb5-117">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="40bb5-118">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="40bb5-118">Valid values are:</span></span> 

- <span data-ttu-id="40bb5-119">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="40bb5-119">North Central US</span></span>
- <span data-ttu-id="40bb5-120">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="40bb5-120">South Central US</span></span>
- <span data-ttu-id="40bb5-121">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="40bb5-121">Central US</span></span>
- <span data-ttu-id="40bb5-122">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="40bb5-122">West Europe</span></span>
- <span data-ttu-id="40bb5-123">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="40bb5-123">North Europe</span></span>
- <span data-ttu-id="40bb5-124">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="40bb5-124">West US</span></span>
- <span data-ttu-id="40bb5-125">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="40bb5-125">East US</span></span>
- <span data-ttu-id="40bb5-126">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="40bb5-126">East US 2</span></span>
- <span data-ttu-id="40bb5-127">Giappone est</span><span class="sxs-lookup"><span data-stu-id="40bb5-127">Japan East</span></span>
- <span data-ttu-id="40bb5-128">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="40bb5-128">Japan West</span></span>
- <span data-ttu-id="40bb5-129">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="40bb5-129">Brazil South</span></span>
- <span data-ttu-id="40bb5-130">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="40bb5-130">Southeast Asia</span></span>
- <span data-ttu-id="40bb5-131">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="40bb5-131">East Asia</span></span>
- <span data-ttu-id="40bb5-132">Australia Est</span><span class="sxs-lookup"><span data-stu-id="40bb5-132">Australia East</span></span>
- <span data-ttu-id="40bb5-133">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="40bb5-133">Australia Southeast</span></span>

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

### <span data-ttu-id="40bb5-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="40bb5-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="40bb5-135">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="40bb5-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="40bb5-136">Usa il parametro *RedisConfiguration* per impostare i criteri di MaxMemory.</span><span class="sxs-lookup"><span data-stu-id="40bb5-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="40bb5-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="40bb5-137">For example:</span></span> 

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

### <span data-ttu-id="40bb5-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="40bb5-138">-Name</span></span>
<span data-ttu-id="40bb5-139">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="40bb5-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="40bb5-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="40bb5-140">-RedisConfiguration</span></span>
<span data-ttu-id="40bb5-141">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="40bb5-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="40bb5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40bb5-143">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="40bb5-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="40bb5-144">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="40bb5-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="40bb5-145">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-145">Premium tier only.</span></span>
- <span data-ttu-id="40bb5-146">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="40bb5-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="40bb5-147">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="40bb5-148">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-148">Premium tier only.</span></span>
- <span data-ttu-id="40bb5-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="40bb5-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="40bb5-150">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="40bb5-151">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-151">Premium tier only.</span></span> 
- <span data-ttu-id="40bb5-152">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="40bb5-152">maxmemory-reserved.</span></span>
<span data-ttu-id="40bb5-153">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="40bb5-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="40bb5-154">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-155">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="40bb5-155">maxmemory-policy.</span></span>
<span data-ttu-id="40bb5-156">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="40bb5-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="40bb5-157">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="40bb5-157">All pricing tiers.</span></span> 
- <span data-ttu-id="40bb5-158">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="40bb5-158">notify-keyspace-events.</span></span>
<span data-ttu-id="40bb5-159">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="40bb5-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="40bb5-160">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="40bb5-161">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="40bb5-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="40bb5-162">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="40bb5-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="40bb5-163">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-164">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="40bb5-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="40bb5-165">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="40bb5-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="40bb5-166">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-167">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="40bb5-167">set-max-intset-entries.</span></span>
<span data-ttu-id="40bb5-168">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="40bb5-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="40bb5-169">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-170">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="40bb5-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="40bb5-171">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="40bb5-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="40bb5-172">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-173">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="40bb5-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="40bb5-174">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="40bb5-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="40bb5-175">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="40bb5-176">database.</span><span class="sxs-lookup"><span data-stu-id="40bb5-176">databases.</span></span>
<span data-ttu-id="40bb5-177">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="40bb5-177">Configures the number of databases.</span></span>
<span data-ttu-id="40bb5-178">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="40bb5-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="40bb5-179">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="40bb5-180">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="40bb5-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="40bb5-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="40bb5-181">-RedisVersion</span></span>
<span data-ttu-id="40bb5-182">Questo parametro è deprecato e verrà rimosso dalle versioni future.</span><span class="sxs-lookup"><span data-stu-id="40bb5-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="40bb5-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bb5-183">-ResourceGroupName</span></span>
<span data-ttu-id="40bb5-184">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="40bb5-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="40bb5-185">-ShardCount</span></span>
<span data-ttu-id="40bb5-186">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="40bb5-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="40bb5-187">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="40bb5-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40bb5-188">1</span><span class="sxs-lookup"><span data-stu-id="40bb5-188">1</span></span>
- <span data-ttu-id="40bb5-189">2</span><span class="sxs-lookup"><span data-stu-id="40bb5-189">2</span></span>
- <span data-ttu-id="40bb5-190">3</span><span class="sxs-lookup"><span data-stu-id="40bb5-190">3</span></span>
- <span data-ttu-id="40bb5-191">4</span><span class="sxs-lookup"><span data-stu-id="40bb5-191">4</span></span>
- <span data-ttu-id="40bb5-192">5</span><span class="sxs-lookup"><span data-stu-id="40bb5-192">5</span></span>
- <span data-ttu-id="40bb5-193">6</span><span class="sxs-lookup"><span data-stu-id="40bb5-193">6</span></span>
- <span data-ttu-id="40bb5-194">7</span><span class="sxs-lookup"><span data-stu-id="40bb5-194">7</span></span>
- <span data-ttu-id="40bb5-195">8</span><span class="sxs-lookup"><span data-stu-id="40bb5-195">8</span></span>
- <span data-ttu-id="40bb5-196">9</span><span class="sxs-lookup"><span data-stu-id="40bb5-196">9</span></span> 
- <span data-ttu-id="40bb5-197">10</span><span class="sxs-lookup"><span data-stu-id="40bb5-197">10</span></span>

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

### <span data-ttu-id="40bb5-198">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="40bb5-198">-Size</span></span>
<span data-ttu-id="40bb5-199">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="40bb5-200">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="40bb5-200">Valid values are:</span></span> 

- <span data-ttu-id="40bb5-201">P1</span><span class="sxs-lookup"><span data-stu-id="40bb5-201">P1</span></span>
- <span data-ttu-id="40bb5-202">P2</span><span class="sxs-lookup"><span data-stu-id="40bb5-202">P2</span></span>
- <span data-ttu-id="40bb5-203">P3</span><span class="sxs-lookup"><span data-stu-id="40bb5-203">P3</span></span>
- <span data-ttu-id="40bb5-204">P4</span><span class="sxs-lookup"><span data-stu-id="40bb5-204">P4</span></span>
- <span data-ttu-id="40bb5-205">C0</span><span class="sxs-lookup"><span data-stu-id="40bb5-205">C0</span></span>
- <span data-ttu-id="40bb5-206">C1</span><span class="sxs-lookup"><span data-stu-id="40bb5-206">C1</span></span>
- <span data-ttu-id="40bb5-207">C2</span><span class="sxs-lookup"><span data-stu-id="40bb5-207">C2</span></span>
- <span data-ttu-id="40bb5-208">C3</span><span class="sxs-lookup"><span data-stu-id="40bb5-208">C3</span></span>
- <span data-ttu-id="40bb5-209">C4</span><span class="sxs-lookup"><span data-stu-id="40bb5-209">C4</span></span>
- <span data-ttu-id="40bb5-210">C5</span><span class="sxs-lookup"><span data-stu-id="40bb5-210">C5</span></span>
- <span data-ttu-id="40bb5-211">C6</span><span class="sxs-lookup"><span data-stu-id="40bb5-211">C6</span></span>
- <span data-ttu-id="40bb5-212">250MB</span><span class="sxs-lookup"><span data-stu-id="40bb5-212">250MB</span></span>
- <span data-ttu-id="40bb5-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-213">1GB</span></span>
- <span data-ttu-id="40bb5-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-214">2.5GB</span></span>
- <span data-ttu-id="40bb5-215">6GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-215">6GB</span></span>
- <span data-ttu-id="40bb5-216">13 GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-216">13GB</span></span>
- <span data-ttu-id="40bb5-217">26GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-217">26GB</span></span>
- <span data-ttu-id="40bb5-218">53GB</span><span class="sxs-lookup"><span data-stu-id="40bb5-218">53GB</span></span>

<span data-ttu-id="40bb5-219">Il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="40bb5-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="40bb5-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="40bb5-220">-Sku</span></span>
<span data-ttu-id="40bb5-221">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="40bb5-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="40bb5-222">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="40bb5-222">Valid values are:</span></span> 

- <span data-ttu-id="40bb5-223">Base</span><span class="sxs-lookup"><span data-stu-id="40bb5-223">Basic</span></span>
- <span data-ttu-id="40bb5-224">Standard</span><span class="sxs-lookup"><span data-stu-id="40bb5-224">Standard</span></span>
- <span data-ttu-id="40bb5-225">Premium</span><span class="sxs-lookup"><span data-stu-id="40bb5-225">Premium</span></span>

<span data-ttu-id="40bb5-226">Il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="40bb5-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="40bb5-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="40bb5-227">-StaticIP</span></span>
<span data-ttu-id="40bb5-228">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="40bb5-229">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="40bb5-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="40bb5-230">-Subnet</span><span class="sxs-lookup"><span data-stu-id="40bb5-230">-Subnet</span></span>
<span data-ttu-id="40bb5-231">Specifica il nome della subnet in cui distribuire la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="40bb5-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="40bb5-232">-SubnetId</span></span>
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

### <span data-ttu-id="40bb5-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="40bb5-233">-TenantSettings</span></span>
<span data-ttu-id="40bb5-234">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="40bb5-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="40bb5-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40bb5-235">-VirtualNetwork</span></span>
<span data-ttu-id="40bb5-236">Specifica l'ID risorsa della rete virtuale in cui distribuire la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="40bb5-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="40bb5-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bb5-237">-DefaultProfile</span></span>
<span data-ttu-id="40bb5-238">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40bb5-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40bb5-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bb5-239">CommonParameters</span></span>
<span data-ttu-id="40bb5-240">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bb5-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bb5-241">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bb5-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bb5-242">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40bb5-242">INPUTS</span></span>

### <span data-ttu-id="40bb5-243">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40bb5-243">None</span></span>
<span data-ttu-id="40bb5-244">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="40bb5-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="40bb5-245">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40bb5-245">OUTPUTS</span></span>

### <span data-ttu-id="40bb5-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="40bb5-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="40bb5-247">Questo cmdlet restituisce tutti gli attributi di una cache Redis, inclusi i tasti di scelta primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="40bb5-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="40bb5-248">Note</span><span class="sxs-lookup"><span data-stu-id="40bb5-248">NOTES</span></span>

## <span data-ttu-id="40bb5-249">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40bb5-249">RELATED LINKS</span></span>

[<span data-ttu-id="40bb5-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="40bb5-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="40bb5-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="40bb5-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="40bb5-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="40bb5-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


