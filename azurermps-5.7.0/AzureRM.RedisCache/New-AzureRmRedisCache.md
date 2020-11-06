---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512388"
---
# <span data-ttu-id="1bf20-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bf20-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="1bf20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bf20-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf20-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf20-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bf20-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf20-106">Il cmdlet **New-AzureRmRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="1bf20-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf20-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf20-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="1bf20-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="1bf20-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="1bf20-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="1bf20-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="1bf20-111">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="1bf20-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bf20-112">PARAMETERS</span></span>

### <span data-ttu-id="1bf20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf20-113">-DefaultProfile</span></span>
<span data-ttu-id="1bf20-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf20-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="1bf20-115">-EnableNonSslPort</span></span>
<span data-ttu-id="1bf20-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1bf20-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="1bf20-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="1bf20-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="1bf20-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bf20-118">-Location</span></span>
<span data-ttu-id="1bf20-119">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="1bf20-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1bf20-120">Valid values are:</span></span> 

- <span data-ttu-id="1bf20-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="1bf20-121">North Central US</span></span>
- <span data-ttu-id="1bf20-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="1bf20-122">South Central US</span></span>
- <span data-ttu-id="1bf20-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="1bf20-123">Central US</span></span>
- <span data-ttu-id="1bf20-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="1bf20-124">West Europe</span></span>
- <span data-ttu-id="1bf20-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="1bf20-125">North Europe</span></span>
- <span data-ttu-id="1bf20-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="1bf20-126">West US</span></span>
- <span data-ttu-id="1bf20-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="1bf20-127">East US</span></span>
- <span data-ttu-id="1bf20-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="1bf20-128">East US 2</span></span>
- <span data-ttu-id="1bf20-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="1bf20-129">Japan East</span></span>
- <span data-ttu-id="1bf20-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="1bf20-130">Japan West</span></span>
- <span data-ttu-id="1bf20-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="1bf20-131">Brazil South</span></span>
- <span data-ttu-id="1bf20-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="1bf20-132">Southeast Asia</span></span>
- <span data-ttu-id="1bf20-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="1bf20-133">East Asia</span></span>
- <span data-ttu-id="1bf20-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="1bf20-134">Australia East</span></span>
- <span data-ttu-id="1bf20-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="1bf20-135">Australia Southeast</span></span>

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

### <span data-ttu-id="1bf20-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="1bf20-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="1bf20-137">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="1bf20-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="1bf20-138">Usa il parametro *RedisConfiguration* per impostare i criteri di MaxMemory.</span><span class="sxs-lookup"><span data-stu-id="1bf20-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="1bf20-139">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="1bf20-139">For example:</span></span> 

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

### <span data-ttu-id="1bf20-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bf20-140">-Name</span></span>
<span data-ttu-id="1bf20-141">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="1bf20-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="1bf20-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bf20-142">-RedisConfiguration</span></span>
<span data-ttu-id="1bf20-143">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="1bf20-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1bf20-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bf20-145">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="1bf20-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="1bf20-146">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1bf20-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="1bf20-147">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-147">Premium tier only.</span></span>
- <span data-ttu-id="1bf20-148">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="1bf20-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="1bf20-149">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="1bf20-150">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-150">Premium tier only.</span></span>
- <span data-ttu-id="1bf20-151">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="1bf20-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="1bf20-152">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="1bf20-153">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-153">Premium tier only.</span></span> 
- <span data-ttu-id="1bf20-154">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="1bf20-154">maxmemory-reserved.</span></span>
<span data-ttu-id="1bf20-155">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="1bf20-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="1bf20-156">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-157">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="1bf20-157">maxmemory-policy.</span></span>
<span data-ttu-id="1bf20-158">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="1bf20-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="1bf20-159">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="1bf20-159">All pricing tiers.</span></span> 
- <span data-ttu-id="1bf20-160">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="1bf20-160">notify-keyspace-events.</span></span>
<span data-ttu-id="1bf20-161">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="1bf20-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="1bf20-162">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="1bf20-163">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="1bf20-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="1bf20-164">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1bf20-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bf20-165">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-166">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="1bf20-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="1bf20-167">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1bf20-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bf20-168">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-169">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="1bf20-169">set-max-intset-entries.</span></span>
<span data-ttu-id="1bf20-170">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1bf20-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bf20-171">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-172">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="1bf20-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="1bf20-173">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1bf20-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bf20-174">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-175">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="1bf20-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="1bf20-176">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1bf20-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bf20-177">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bf20-178">database.</span><span class="sxs-lookup"><span data-stu-id="1bf20-178">databases.</span></span>
<span data-ttu-id="1bf20-179">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="1bf20-179">Configures the number of databases.</span></span>
<span data-ttu-id="1bf20-180">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="1bf20-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="1bf20-181">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="1bf20-182">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="1bf20-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="1bf20-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="1bf20-183">-RedisVersion</span></span>
<span data-ttu-id="1bf20-184">Questo parametro è deprecato e verrà rimosso dalle versioni future.</span><span class="sxs-lookup"><span data-stu-id="1bf20-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="1bf20-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf20-185">-ResourceGroupName</span></span>
<span data-ttu-id="1bf20-186">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="1bf20-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="1bf20-187">-ShardCount</span></span>
<span data-ttu-id="1bf20-188">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="1bf20-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="1bf20-189">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1bf20-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bf20-190">1</span><span class="sxs-lookup"><span data-stu-id="1bf20-190">1</span></span>
- <span data-ttu-id="1bf20-191">2</span><span class="sxs-lookup"><span data-stu-id="1bf20-191">2</span></span>
- <span data-ttu-id="1bf20-192">3</span><span class="sxs-lookup"><span data-stu-id="1bf20-192">3</span></span>
- <span data-ttu-id="1bf20-193">4</span><span class="sxs-lookup"><span data-stu-id="1bf20-193">4</span></span>
- <span data-ttu-id="1bf20-194">5</span><span class="sxs-lookup"><span data-stu-id="1bf20-194">5</span></span>
- <span data-ttu-id="1bf20-195">6</span><span class="sxs-lookup"><span data-stu-id="1bf20-195">6</span></span>
- <span data-ttu-id="1bf20-196">7</span><span class="sxs-lookup"><span data-stu-id="1bf20-196">7</span></span>
- <span data-ttu-id="1bf20-197">8</span><span class="sxs-lookup"><span data-stu-id="1bf20-197">8</span></span>
- <span data-ttu-id="1bf20-198">9</span><span class="sxs-lookup"><span data-stu-id="1bf20-198">9</span></span> 
- <span data-ttu-id="1bf20-199">10</span><span class="sxs-lookup"><span data-stu-id="1bf20-199">10</span></span>

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

### <span data-ttu-id="1bf20-200">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="1bf20-200">-Size</span></span>
<span data-ttu-id="1bf20-201">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="1bf20-202">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1bf20-202">Valid values are:</span></span> 

- <span data-ttu-id="1bf20-203">P1</span><span class="sxs-lookup"><span data-stu-id="1bf20-203">P1</span></span>
- <span data-ttu-id="1bf20-204">P2</span><span class="sxs-lookup"><span data-stu-id="1bf20-204">P2</span></span>
- <span data-ttu-id="1bf20-205">P3</span><span class="sxs-lookup"><span data-stu-id="1bf20-205">P3</span></span>
- <span data-ttu-id="1bf20-206">P4</span><span class="sxs-lookup"><span data-stu-id="1bf20-206">P4</span></span>
- <span data-ttu-id="1bf20-207">C0</span><span class="sxs-lookup"><span data-stu-id="1bf20-207">C0</span></span>
- <span data-ttu-id="1bf20-208">C1</span><span class="sxs-lookup"><span data-stu-id="1bf20-208">C1</span></span>
- <span data-ttu-id="1bf20-209">C2</span><span class="sxs-lookup"><span data-stu-id="1bf20-209">C2</span></span>
- <span data-ttu-id="1bf20-210">C3</span><span class="sxs-lookup"><span data-stu-id="1bf20-210">C3</span></span>
- <span data-ttu-id="1bf20-211">C4</span><span class="sxs-lookup"><span data-stu-id="1bf20-211">C4</span></span>
- <span data-ttu-id="1bf20-212">C5</span><span class="sxs-lookup"><span data-stu-id="1bf20-212">C5</span></span>
- <span data-ttu-id="1bf20-213">C6</span><span class="sxs-lookup"><span data-stu-id="1bf20-213">C6</span></span>
- <span data-ttu-id="1bf20-214">250MB</span><span class="sxs-lookup"><span data-stu-id="1bf20-214">250MB</span></span>
- <span data-ttu-id="1bf20-215">1 GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-215">1GB</span></span>
- <span data-ttu-id="1bf20-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-216">2.5GB</span></span>
- <span data-ttu-id="1bf20-217">6GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-217">6GB</span></span>
- <span data-ttu-id="1bf20-218">13 GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-218">13GB</span></span>
- <span data-ttu-id="1bf20-219">26GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-219">26GB</span></span>
- <span data-ttu-id="1bf20-220">53GB</span><span class="sxs-lookup"><span data-stu-id="1bf20-220">53GB</span></span>

<span data-ttu-id="1bf20-221">Il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="1bf20-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="1bf20-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bf20-222">-Sku</span></span>
<span data-ttu-id="1bf20-223">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="1bf20-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="1bf20-224">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1bf20-224">Valid values are:</span></span> 

- <span data-ttu-id="1bf20-225">Base</span><span class="sxs-lookup"><span data-stu-id="1bf20-225">Basic</span></span>
- <span data-ttu-id="1bf20-226">Standard</span><span class="sxs-lookup"><span data-stu-id="1bf20-226">Standard</span></span>
- <span data-ttu-id="1bf20-227">Premium</span><span class="sxs-lookup"><span data-stu-id="1bf20-227">Premium</span></span>

<span data-ttu-id="1bf20-228">Il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="1bf20-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="1bf20-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="1bf20-229">-StaticIP</span></span>
<span data-ttu-id="1bf20-230">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="1bf20-231">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="1bf20-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="1bf20-232">-Subnet</span><span class="sxs-lookup"><span data-stu-id="1bf20-232">-Subnet</span></span>
<span data-ttu-id="1bf20-233">Specifica il nome della subnet in cui distribuire la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="1bf20-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1bf20-234">-SubnetId</span></span>
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

### <span data-ttu-id="1bf20-235">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bf20-235">-Tag</span></span>
<span data-ttu-id="1bf20-236">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="1bf20-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="1bf20-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="1bf20-237">-TenantSettings</span></span>
<span data-ttu-id="1bf20-238">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="1bf20-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="1bf20-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1bf20-239">-VirtualNetwork</span></span>
<span data-ttu-id="1bf20-240">Specifica l'ID risorsa della rete virtuale in cui distribuire la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1bf20-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="1bf20-241">-Zona</span><span class="sxs-lookup"><span data-stu-id="1bf20-241">-Zone</span></span>
<span data-ttu-id="1bf20-242">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="1bf20-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf20-243">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bf20-243">-Confirm</span></span>
<span data-ttu-id="1bf20-244">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf20-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf20-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf20-245">-WhatIf</span></span>
<span data-ttu-id="1bf20-246">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf20-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bf20-247">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf20-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf20-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf20-248">CommonParameters</span></span>
<span data-ttu-id="1bf20-249">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf20-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf20-250">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf20-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf20-251">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bf20-251">INPUTS</span></span>

### <span data-ttu-id="1bf20-252">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1bf20-252">None</span></span>
<span data-ttu-id="1bf20-253">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="1bf20-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="1bf20-254">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf20-254">OUTPUTS</span></span>

### <span data-ttu-id="1bf20-255">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1bf20-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="1bf20-256">Questo cmdlet restituisce tutti gli attributi di una cache Redis, inclusi i tasti di scelta primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="1bf20-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="1bf20-257">Note</span><span class="sxs-lookup"><span data-stu-id="1bf20-257">NOTES</span></span>

## <span data-ttu-id="1bf20-258">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf20-258">RELATED LINKS</span></span>

[<span data-ttu-id="1bf20-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bf20-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1bf20-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bf20-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="1bf20-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bf20-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


