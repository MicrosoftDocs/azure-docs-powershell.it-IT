---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855590"
---
# <span data-ttu-id="1238d-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1238d-101">New-AzRedisCache</span></span>

## <span data-ttu-id="1238d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1238d-102">SYNOPSIS</span></span>
<span data-ttu-id="1238d-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="1238d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1238d-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1238d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1238d-105">DESCRIPTION</span></span>
<span data-ttu-id="1238d-106">Il cmdlet **New-AzRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="1238d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1238d-107">EXAMPLES</span></span>

### <span data-ttu-id="1238d-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="1238d-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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

<span data-ttu-id="1238d-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="1238d-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="1238d-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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

<span data-ttu-id="1238d-111">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="1238d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1238d-112">PARAMETERS</span></span>

### <span data-ttu-id="1238d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1238d-113">-DefaultProfile</span></span>
<span data-ttu-id="1238d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1238d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1238d-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="1238d-115">-EnableNonSslPort</span></span>
<span data-ttu-id="1238d-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1238d-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="1238d-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="1238d-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="1238d-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1238d-118">-Location</span></span>
<span data-ttu-id="1238d-119">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="1238d-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1238d-120">Valid values are:</span></span> 
- <span data-ttu-id="1238d-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="1238d-121">North Central US</span></span>
- <span data-ttu-id="1238d-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="1238d-122">South Central US</span></span>
- <span data-ttu-id="1238d-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="1238d-123">Central US</span></span>
- <span data-ttu-id="1238d-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="1238d-124">West Europe</span></span>
- <span data-ttu-id="1238d-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="1238d-125">North Europe</span></span>
- <span data-ttu-id="1238d-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="1238d-126">West US</span></span>
- <span data-ttu-id="1238d-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="1238d-127">East US</span></span>
- <span data-ttu-id="1238d-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="1238d-128">East US 2</span></span>
- <span data-ttu-id="1238d-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="1238d-129">Japan East</span></span>
- <span data-ttu-id="1238d-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="1238d-130">Japan West</span></span>
- <span data-ttu-id="1238d-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="1238d-131">Brazil South</span></span>
- <span data-ttu-id="1238d-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="1238d-132">Southeast Asia</span></span>
- <span data-ttu-id="1238d-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="1238d-133">East Asia</span></span>
- <span data-ttu-id="1238d-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="1238d-134">Australia East</span></span>
- <span data-ttu-id="1238d-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="1238d-135">Australia Southeast</span></span>

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

### <span data-ttu-id="1238d-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="1238d-136">-Name</span></span>
<span data-ttu-id="1238d-137">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="1238d-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="1238d-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="1238d-138">-RedisConfiguration</span></span>
<span data-ttu-id="1238d-139">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="1238d-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1238d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1238d-141">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="1238d-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="1238d-142">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1238d-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="1238d-143">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-143">Premium tier only.</span></span>
- <span data-ttu-id="1238d-144">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="1238d-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="1238d-145">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="1238d-146">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-146">Premium tier only.</span></span>
- <span data-ttu-id="1238d-147">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="1238d-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="1238d-148">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="1238d-149">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-149">Premium tier only.</span></span> 
- <span data-ttu-id="1238d-150">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="1238d-150">maxmemory-reserved.</span></span>
<span data-ttu-id="1238d-151">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="1238d-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="1238d-152">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-153">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="1238d-153">maxmemory-policy.</span></span>
<span data-ttu-id="1238d-154">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="1238d-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="1238d-155">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="1238d-155">All pricing tiers.</span></span> 
- <span data-ttu-id="1238d-156">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="1238d-156">notify-keyspace-events.</span></span>
<span data-ttu-id="1238d-157">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="1238d-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="1238d-158">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="1238d-159">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="1238d-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="1238d-160">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1238d-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1238d-161">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-162">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="1238d-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="1238d-163">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1238d-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1238d-164">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-165">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="1238d-165">set-max-intset-entries.</span></span>
<span data-ttu-id="1238d-166">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1238d-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1238d-167">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-168">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="1238d-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="1238d-169">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1238d-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1238d-170">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-171">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="1238d-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="1238d-172">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="1238d-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1238d-173">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1238d-174">database.</span><span class="sxs-lookup"><span data-stu-id="1238d-174">databases.</span></span>
<span data-ttu-id="1238d-175">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="1238d-175">Configures the number of databases.</span></span>
<span data-ttu-id="1238d-176">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="1238d-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="1238d-177">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="1238d-178">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="1238d-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="1238d-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1238d-179">-ResourceGroupName</span></span>
<span data-ttu-id="1238d-180">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="1238d-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="1238d-181">-ShardCount</span></span>
<span data-ttu-id="1238d-182">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="1238d-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="1238d-183">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1238d-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1238d-184">1</span><span class="sxs-lookup"><span data-stu-id="1238d-184">1</span></span>
- <span data-ttu-id="1238d-185">2</span><span class="sxs-lookup"><span data-stu-id="1238d-185">2</span></span>
- <span data-ttu-id="1238d-186">3</span><span class="sxs-lookup"><span data-stu-id="1238d-186">3</span></span>
- <span data-ttu-id="1238d-187">4</span><span class="sxs-lookup"><span data-stu-id="1238d-187">4</span></span>
- <span data-ttu-id="1238d-188">5</span><span class="sxs-lookup"><span data-stu-id="1238d-188">5</span></span>
- <span data-ttu-id="1238d-189">6</span><span class="sxs-lookup"><span data-stu-id="1238d-189">6</span></span>
- <span data-ttu-id="1238d-190">7</span><span class="sxs-lookup"><span data-stu-id="1238d-190">7</span></span>
- <span data-ttu-id="1238d-191">8</span><span class="sxs-lookup"><span data-stu-id="1238d-191">8</span></span>
- <span data-ttu-id="1238d-192">9</span><span class="sxs-lookup"><span data-stu-id="1238d-192">9</span></span> 
- <span data-ttu-id="1238d-193">10</span><span class="sxs-lookup"><span data-stu-id="1238d-193">10</span></span>

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

### <span data-ttu-id="1238d-194">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="1238d-194">-Size</span></span>
<span data-ttu-id="1238d-195">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="1238d-196">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1238d-196">Valid values are:</span></span> 
- <span data-ttu-id="1238d-197">P1</span><span class="sxs-lookup"><span data-stu-id="1238d-197">P1</span></span>
- <span data-ttu-id="1238d-198">P2</span><span class="sxs-lookup"><span data-stu-id="1238d-198">P2</span></span>
- <span data-ttu-id="1238d-199">P3</span><span class="sxs-lookup"><span data-stu-id="1238d-199">P3</span></span>
- <span data-ttu-id="1238d-200">P4</span><span class="sxs-lookup"><span data-stu-id="1238d-200">P4</span></span>
- <span data-ttu-id="1238d-201">C0</span><span class="sxs-lookup"><span data-stu-id="1238d-201">C0</span></span>
- <span data-ttu-id="1238d-202">C1</span><span class="sxs-lookup"><span data-stu-id="1238d-202">C1</span></span>
- <span data-ttu-id="1238d-203">C2</span><span class="sxs-lookup"><span data-stu-id="1238d-203">C2</span></span>
- <span data-ttu-id="1238d-204">C3</span><span class="sxs-lookup"><span data-stu-id="1238d-204">C3</span></span>
- <span data-ttu-id="1238d-205">C4</span><span class="sxs-lookup"><span data-stu-id="1238d-205">C4</span></span>
- <span data-ttu-id="1238d-206">C5</span><span class="sxs-lookup"><span data-stu-id="1238d-206">C5</span></span>
- <span data-ttu-id="1238d-207">C6</span><span class="sxs-lookup"><span data-stu-id="1238d-207">C6</span></span>
- <span data-ttu-id="1238d-208">250MB</span><span class="sxs-lookup"><span data-stu-id="1238d-208">250MB</span></span>
- <span data-ttu-id="1238d-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="1238d-209">1GB</span></span>
- <span data-ttu-id="1238d-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="1238d-210">2.5GB</span></span>
- <span data-ttu-id="1238d-211">6GB</span><span class="sxs-lookup"><span data-stu-id="1238d-211">6GB</span></span>
- <span data-ttu-id="1238d-212">13 GB</span><span class="sxs-lookup"><span data-stu-id="1238d-212">13GB</span></span>
- <span data-ttu-id="1238d-213">26GB</span><span class="sxs-lookup"><span data-stu-id="1238d-213">26GB</span></span>
- <span data-ttu-id="1238d-214">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="1238d-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="1238d-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="1238d-215">-Sku</span></span>
<span data-ttu-id="1238d-216">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="1238d-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="1238d-217">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1238d-217">Valid values are:</span></span> 
- <span data-ttu-id="1238d-218">Base</span><span class="sxs-lookup"><span data-stu-id="1238d-218">Basic</span></span>
- <span data-ttu-id="1238d-219">Standard</span><span class="sxs-lookup"><span data-stu-id="1238d-219">Standard</span></span>
- <span data-ttu-id="1238d-220">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="1238d-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="1238d-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="1238d-221">-StaticIP</span></span>
<span data-ttu-id="1238d-222">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1238d-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="1238d-223">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="1238d-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="1238d-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1238d-224">-SubnetId</span></span>
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

### <span data-ttu-id="1238d-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="1238d-225">-Tag</span></span>
<span data-ttu-id="1238d-226">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="1238d-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="1238d-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="1238d-227">-TenantSettings</span></span>
<span data-ttu-id="1238d-228">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="1238d-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="1238d-229">-Zona</span><span class="sxs-lookup"><span data-stu-id="1238d-229">-Zone</span></span>
<span data-ttu-id="1238d-230">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="1238d-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1238d-231">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1238d-231">-Confirm</span></span>
<span data-ttu-id="1238d-232">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1238d-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1238d-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1238d-233">-WhatIf</span></span>
<span data-ttu-id="1238d-234">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1238d-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1238d-235">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1238d-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1238d-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1238d-236">CommonParameters</span></span>
<span data-ttu-id="1238d-237">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1238d-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1238d-238">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1238d-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1238d-239">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1238d-239">INPUTS</span></span>

### <span data-ttu-id="1238d-240">System. String</span><span class="sxs-lookup"><span data-stu-id="1238d-240">System.String</span></span>

### <span data-ttu-id="1238d-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1238d-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1238d-242">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1238d-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1238d-243">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1238d-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1238d-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="1238d-244">System.String[]</span></span>

## <span data-ttu-id="1238d-245">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1238d-245">OUTPUTS</span></span>

### <span data-ttu-id="1238d-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1238d-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="1238d-247">Note</span><span class="sxs-lookup"><span data-stu-id="1238d-247">NOTES</span></span>

## <span data-ttu-id="1238d-248">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1238d-248">RELATED LINKS</span></span>

[<span data-ttu-id="1238d-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1238d-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1238d-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1238d-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1238d-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1238d-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


