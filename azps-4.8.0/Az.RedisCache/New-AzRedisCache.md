---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031139"
---
# <span data-ttu-id="6a988-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6a988-101">New-AzRedisCache</span></span>

## <span data-ttu-id="6a988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a988-102">SYNOPSIS</span></span>
<span data-ttu-id="6a988-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="6a988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a988-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a988-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a988-105">DESCRIPTION</span></span>
<span data-ttu-id="6a988-106">Il cmdlet **New-AzRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="6a988-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a988-107">EXAMPLES</span></span>

### <span data-ttu-id="6a988-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="6a988-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="6a988-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="6a988-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="6a988-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="6a988-111">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="6a988-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a988-112">PARAMETERS</span></span>

### <span data-ttu-id="6a988-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a988-113">-DefaultProfile</span></span>
<span data-ttu-id="6a988-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a988-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a988-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="6a988-115">-EnableNonSslPort</span></span>
<span data-ttu-id="6a988-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6a988-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="6a988-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="6a988-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="6a988-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6a988-118">-Location</span></span>
<span data-ttu-id="6a988-119">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="6a988-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6a988-120">Valid values are:</span></span> 
- <span data-ttu-id="6a988-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="6a988-121">North Central US</span></span>
- <span data-ttu-id="6a988-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="6a988-122">South Central US</span></span>
- <span data-ttu-id="6a988-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="6a988-123">Central US</span></span>
- <span data-ttu-id="6a988-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="6a988-124">West Europe</span></span>
- <span data-ttu-id="6a988-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="6a988-125">North Europe</span></span>
- <span data-ttu-id="6a988-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="6a988-126">West US</span></span>
- <span data-ttu-id="6a988-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="6a988-127">East US</span></span>
- <span data-ttu-id="6a988-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="6a988-128">East US 2</span></span>
- <span data-ttu-id="6a988-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="6a988-129">Japan East</span></span>
- <span data-ttu-id="6a988-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="6a988-130">Japan West</span></span>
- <span data-ttu-id="6a988-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="6a988-131">Brazil South</span></span>
- <span data-ttu-id="6a988-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="6a988-132">Southeast Asia</span></span>
- <span data-ttu-id="6a988-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="6a988-133">East Asia</span></span>
- <span data-ttu-id="6a988-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="6a988-134">Australia East</span></span>
- <span data-ttu-id="6a988-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="6a988-135">Australia Southeast</span></span>

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

### <span data-ttu-id="6a988-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6a988-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="6a988-137">Specifica la versione TLS richiesta dai client per la connessione alla cache.</span><span class="sxs-lookup"><span data-stu-id="6a988-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="6a988-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a988-138">-Name</span></span>
<span data-ttu-id="6a988-139">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="6a988-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="6a988-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a988-140">-RedisConfiguration</span></span>
<span data-ttu-id="6a988-141">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="6a988-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a988-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a988-143">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="6a988-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="6a988-144">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6a988-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="6a988-145">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-145">Premium tier only.</span></span>
- <span data-ttu-id="6a988-146">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="6a988-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="6a988-147">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="6a988-148">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-148">Premium tier only.</span></span>
- <span data-ttu-id="6a988-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="6a988-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="6a988-150">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="6a988-151">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-151">Premium tier only.</span></span> 
- <span data-ttu-id="6a988-152">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="6a988-152">maxmemory-reserved.</span></span>
<span data-ttu-id="6a988-153">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="6a988-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="6a988-154">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-155">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="6a988-155">maxmemory-policy.</span></span>
<span data-ttu-id="6a988-156">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="6a988-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="6a988-157">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="6a988-157">All pricing tiers.</span></span> 
- <span data-ttu-id="6a988-158">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="6a988-158">notify-keyspace-events.</span></span>
<span data-ttu-id="6a988-159">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="6a988-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="6a988-160">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="6a988-161">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="6a988-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="6a988-162">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="6a988-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6a988-163">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-164">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="6a988-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="6a988-165">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="6a988-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6a988-166">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-167">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="6a988-167">set-max-intset-entries.</span></span>
<span data-ttu-id="6a988-168">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="6a988-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6a988-169">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-170">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="6a988-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="6a988-171">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="6a988-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6a988-172">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-173">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="6a988-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="6a988-174">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="6a988-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6a988-175">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6a988-176">database.</span><span class="sxs-lookup"><span data-stu-id="6a988-176">databases.</span></span>
<span data-ttu-id="6a988-177">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="6a988-177">Configures the number of databases.</span></span>
<span data-ttu-id="6a988-178">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="6a988-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="6a988-179">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="6a988-180">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="6a988-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="6a988-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a988-181">-ResourceGroupName</span></span>
<span data-ttu-id="6a988-182">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="6a988-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="6a988-183">-ShardCount</span></span>
<span data-ttu-id="6a988-184">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="6a988-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="6a988-185">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a988-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a988-186">1</span><span class="sxs-lookup"><span data-stu-id="6a988-186">1</span></span>
- <span data-ttu-id="6a988-187">2</span><span class="sxs-lookup"><span data-stu-id="6a988-187">2</span></span>
- <span data-ttu-id="6a988-188">3</span><span class="sxs-lookup"><span data-stu-id="6a988-188">3</span></span>
- <span data-ttu-id="6a988-189">4</span><span class="sxs-lookup"><span data-stu-id="6a988-189">4</span></span>
- <span data-ttu-id="6a988-190">5</span><span class="sxs-lookup"><span data-stu-id="6a988-190">5</span></span>
- <span data-ttu-id="6a988-191">6</span><span class="sxs-lookup"><span data-stu-id="6a988-191">6</span></span>
- <span data-ttu-id="6a988-192">7</span><span class="sxs-lookup"><span data-stu-id="6a988-192">7</span></span>
- <span data-ttu-id="6a988-193">8</span><span class="sxs-lookup"><span data-stu-id="6a988-193">8</span></span>
- <span data-ttu-id="6a988-194">9</span><span class="sxs-lookup"><span data-stu-id="6a988-194">9</span></span> 
- <span data-ttu-id="6a988-195">10</span><span class="sxs-lookup"><span data-stu-id="6a988-195">10</span></span>

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

### <span data-ttu-id="6a988-196">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="6a988-196">-Size</span></span>
<span data-ttu-id="6a988-197">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="6a988-198">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6a988-198">Valid values are:</span></span> 
- <span data-ttu-id="6a988-199">P1</span><span class="sxs-lookup"><span data-stu-id="6a988-199">P1</span></span>
- <span data-ttu-id="6a988-200">P2</span><span class="sxs-lookup"><span data-stu-id="6a988-200">P2</span></span>
- <span data-ttu-id="6a988-201">P3</span><span class="sxs-lookup"><span data-stu-id="6a988-201">P3</span></span>
- <span data-ttu-id="6a988-202">P4</span><span class="sxs-lookup"><span data-stu-id="6a988-202">P4</span></span>
- <span data-ttu-id="6a988-203">P5</span><span class="sxs-lookup"><span data-stu-id="6a988-203">P5</span></span>
- <span data-ttu-id="6a988-204">C0</span><span class="sxs-lookup"><span data-stu-id="6a988-204">C0</span></span>
- <span data-ttu-id="6a988-205">C1</span><span class="sxs-lookup"><span data-stu-id="6a988-205">C1</span></span>
- <span data-ttu-id="6a988-206">C2</span><span class="sxs-lookup"><span data-stu-id="6a988-206">C2</span></span>
- <span data-ttu-id="6a988-207">C3</span><span class="sxs-lookup"><span data-stu-id="6a988-207">C3</span></span>
- <span data-ttu-id="6a988-208">C4</span><span class="sxs-lookup"><span data-stu-id="6a988-208">C4</span></span>
- <span data-ttu-id="6a988-209">C5</span><span class="sxs-lookup"><span data-stu-id="6a988-209">C5</span></span>
- <span data-ttu-id="6a988-210">C6</span><span class="sxs-lookup"><span data-stu-id="6a988-210">C6</span></span>
- <span data-ttu-id="6a988-211">250MB</span><span class="sxs-lookup"><span data-stu-id="6a988-211">250MB</span></span>
- <span data-ttu-id="6a988-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="6a988-212">1GB</span></span>
- <span data-ttu-id="6a988-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="6a988-213">2.5GB</span></span>
- <span data-ttu-id="6a988-214">6GB</span><span class="sxs-lookup"><span data-stu-id="6a988-214">6GB</span></span>
- <span data-ttu-id="6a988-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="6a988-215">13GB</span></span>
- <span data-ttu-id="6a988-216">26GB</span><span class="sxs-lookup"><span data-stu-id="6a988-216">26GB</span></span>
- <span data-ttu-id="6a988-217">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="6a988-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="6a988-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="6a988-218">-Sku</span></span>
<span data-ttu-id="6a988-219">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="6a988-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="6a988-220">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6a988-220">Valid values are:</span></span> 
- <span data-ttu-id="6a988-221">Base</span><span class="sxs-lookup"><span data-stu-id="6a988-221">Basic</span></span>
- <span data-ttu-id="6a988-222">Standard</span><span class="sxs-lookup"><span data-stu-id="6a988-222">Standard</span></span>
- <span data-ttu-id="6a988-223">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="6a988-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="6a988-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="6a988-224">-StaticIP</span></span>
<span data-ttu-id="6a988-225">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6a988-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="6a988-226">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="6a988-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="6a988-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6a988-227">-SubnetId</span></span>
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

### <span data-ttu-id="6a988-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a988-228">-Tag</span></span>
<span data-ttu-id="6a988-229">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="6a988-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="6a988-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="6a988-230">-TenantSettings</span></span>
<span data-ttu-id="6a988-231">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="6a988-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="6a988-232">-Zona</span><span class="sxs-lookup"><span data-stu-id="6a988-232">-Zone</span></span>
<span data-ttu-id="6a988-233">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="6a988-233">List of zones.</span></span>

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

### <span data-ttu-id="6a988-234">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a988-234">-Confirm</span></span>
<span data-ttu-id="6a988-235">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a988-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a988-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a988-236">-WhatIf</span></span>
<span data-ttu-id="6a988-237">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a988-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a988-238">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a988-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a988-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a988-239">CommonParameters</span></span>
<span data-ttu-id="6a988-240">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a988-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a988-241">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a988-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a988-242">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a988-242">INPUTS</span></span>

### <span data-ttu-id="6a988-243">System. String</span><span class="sxs-lookup"><span data-stu-id="6a988-243">System.String</span></span>

### <span data-ttu-id="6a988-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a988-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6a988-245">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a988-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a988-246">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a988-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a988-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="6a988-247">System.String[]</span></span>

## <span data-ttu-id="6a988-248">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a988-248">OUTPUTS</span></span>

### <span data-ttu-id="6a988-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6a988-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="6a988-250">Note</span><span class="sxs-lookup"><span data-stu-id="6a988-250">NOTES</span></span>

## <span data-ttu-id="6a988-251">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a988-251">RELATED LINKS</span></span>

[<span data-ttu-id="6a988-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6a988-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6a988-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6a988-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6a988-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6a988-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


