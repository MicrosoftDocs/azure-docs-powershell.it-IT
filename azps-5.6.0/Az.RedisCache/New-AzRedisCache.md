---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997371"
---
# <span data-ttu-id="78ce3-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="78ce3-101">New-AzRedisCache</span></span>

## <span data-ttu-id="78ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="78ce3-103">Crea una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="78ce3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78ce3-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78ce3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="78ce3-106">Il cmdlet **New-AzRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="78ce3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="78ce3-108">Esempio 1: Creare una cache di Ridis</span><span class="sxs-lookup"><span data-stu-id="78ce3-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="78ce3-109">Questo comando crea una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="78ce3-110">Esempio 2: Creare una cache di ridisposizione SKU standard</span><span class="sxs-lookup"><span data-stu-id="78ce3-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="78ce3-111">Questo comando crea una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="78ce3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78ce3-112">PARAMETERS</span></span>

### <span data-ttu-id="78ce3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ce3-113">-DefaultProfile</span></span>
<span data-ttu-id="78ce3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78ce3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ce3-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="78ce3-115">-EnableNonSslPort</span></span>
<span data-ttu-id="78ce3-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="78ce3-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="78ce3-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="78ce3-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="78ce3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="78ce3-118">-Location</span></span>
<span data-ttu-id="78ce3-119">Specifica la posizione in cui creare una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="78ce3-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="78ce3-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78ce3-120">Valid values are:</span></span> 
- <span data-ttu-id="78ce3-121">Stati Uniti centro settersi</span><span class="sxs-lookup"><span data-stu-id="78ce3-121">North Central US</span></span>
- <span data-ttu-id="78ce3-122">Stati Uniti centro meridionali</span><span class="sxs-lookup"><span data-stu-id="78ce3-122">South Central US</span></span>
- <span data-ttu-id="78ce3-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="78ce3-123">Central US</span></span>
- <span data-ttu-id="78ce3-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="78ce3-124">West Europe</span></span>
- <span data-ttu-id="78ce3-125">Europa settentrionale</span><span class="sxs-lookup"><span data-stu-id="78ce3-125">North Europe</span></span>
- <span data-ttu-id="78ce3-126">Stati Uniti occidentali</span><span class="sxs-lookup"><span data-stu-id="78ce3-126">West US</span></span>
- <span data-ttu-id="78ce3-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="78ce3-127">East US</span></span>
- <span data-ttu-id="78ce3-128">Stati Uniti orientali 2</span><span class="sxs-lookup"><span data-stu-id="78ce3-128">East US 2</span></span>
- <span data-ttu-id="78ce3-129">Giappone orientale</span><span class="sxs-lookup"><span data-stu-id="78ce3-129">Japan East</span></span>
- <span data-ttu-id="78ce3-130">Giappone occidentale</span><span class="sxs-lookup"><span data-stu-id="78ce3-130">Japan West</span></span>
- <span data-ttu-id="78ce3-131">Brasile meridionale</span><span class="sxs-lookup"><span data-stu-id="78ce3-131">Brazil South</span></span>
- <span data-ttu-id="78ce3-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="78ce3-132">Southeast Asia</span></span>
- <span data-ttu-id="78ce3-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="78ce3-133">East Asia</span></span>
- <span data-ttu-id="78ce3-134">Australia orientale</span><span class="sxs-lookup"><span data-stu-id="78ce3-134">Australia East</span></span>
- <span data-ttu-id="78ce3-135">Australia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="78ce3-135">Australia Southeast</span></span>

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

### <span data-ttu-id="78ce3-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="78ce3-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="78ce3-137">Specificare la versione di TLS richiesta dai client per connettersi alla cache.</span><span class="sxs-lookup"><span data-stu-id="78ce3-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="78ce3-138">-Name</span><span class="sxs-lookup"><span data-stu-id="78ce3-138">-Name</span></span>
<span data-ttu-id="78ce3-139">Specifica il nome della cache di Ridis da creare.</span><span class="sxs-lookup"><span data-stu-id="78ce3-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="78ce3-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="78ce3-140">-RedisConfiguration</span></span>
<span data-ttu-id="78ce3-141">Specifica le impostazioni di configurazione di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="78ce3-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="78ce3-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="78ce3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78ce3-143">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="78ce3-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="78ce3-144">Specifica che la persistenza dei dati di Ridisposizione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="78ce3-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="78ce3-145">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-145">Premium tier only.</span></span>
- <span data-ttu-id="78ce3-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="78ce3-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="78ce3-147">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="78ce3-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="78ce3-148">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-148">Premium tier only.</span></span>
- <span data-ttu-id="78ce3-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="78ce3-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="78ce3-150">Specifica la frequenza di backup per la persistenza dei dati ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="78ce3-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="78ce3-151">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-151">Premium tier only.</span></span> 
- <span data-ttu-id="78ce3-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="78ce3-152">maxmemory-reserved.</span></span>
<span data-ttu-id="78ce3-153">Configura la memoria riservata ai processi non nella cache.</span><span class="sxs-lookup"><span data-stu-id="78ce3-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="78ce3-154">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="78ce3-155">maxmemory-policy.</span></span>
<span data-ttu-id="78ce3-156">Configura i criteri di sgombero per la cache.</span><span class="sxs-lookup"><span data-stu-id="78ce3-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="78ce3-157">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="78ce3-157">All pricing tiers.</span></span> 
- <span data-ttu-id="78ce3-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="78ce3-158">notify-keyspace-events.</span></span>
<span data-ttu-id="78ce3-159">Configura le notifiche di keyspace.</span><span class="sxs-lookup"><span data-stu-id="78ce3-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="78ce3-160">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="78ce3-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="78ce3-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="78ce3-162">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="78ce3-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="78ce3-163">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="78ce3-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="78ce3-165">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="78ce3-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="78ce3-166">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="78ce3-167">set-max-intset-entries.</span></span>
<span data-ttu-id="78ce3-168">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="78ce3-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="78ce3-169">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="78ce3-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="78ce3-171">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="78ce3-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="78ce3-172">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="78ce3-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="78ce3-174">Configura l'ottimizzazione della memoria per piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="78ce3-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="78ce3-175">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="78ce3-176">database.</span><span class="sxs-lookup"><span data-stu-id="78ce3-176">databases.</span></span>
<span data-ttu-id="78ce3-177">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="78ce3-177">Configures the number of databases.</span></span>
<span data-ttu-id="78ce3-178">Questa proprietà può essere configurata solo durante la creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="78ce3-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="78ce3-179">Livelli Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="78ce3-180">Per altre informazioni, vedere Gestire la cache di Azure Redis con Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="78ce3-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="78ce3-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ce3-181">-ResourceGroupName</span></span>
<span data-ttu-id="78ce3-182">Specifica il nome del gruppo di risorse in cui creare la cache di ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="78ce3-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="78ce3-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="78ce3-183">-ShardCount</span></span>
<span data-ttu-id="78ce3-184">Specifica il numero di parti da creare in una cache cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="78ce3-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="78ce3-185">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="78ce3-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78ce3-186">1</span><span class="sxs-lookup"><span data-stu-id="78ce3-186">1</span></span>
- <span data-ttu-id="78ce3-187">2</span><span class="sxs-lookup"><span data-stu-id="78ce3-187">2</span></span>
- <span data-ttu-id="78ce3-188">3</span><span class="sxs-lookup"><span data-stu-id="78ce3-188">3</span></span>
- <span data-ttu-id="78ce3-189">4</span><span class="sxs-lookup"><span data-stu-id="78ce3-189">4</span></span>
- <span data-ttu-id="78ce3-190">5</span><span class="sxs-lookup"><span data-stu-id="78ce3-190">5</span></span>
- <span data-ttu-id="78ce3-191">6</span><span class="sxs-lookup"><span data-stu-id="78ce3-191">6</span></span>
- <span data-ttu-id="78ce3-192">7</span><span class="sxs-lookup"><span data-stu-id="78ce3-192">7</span></span>
- <span data-ttu-id="78ce3-193">8</span><span class="sxs-lookup"><span data-stu-id="78ce3-193">8</span></span>
- <span data-ttu-id="78ce3-194">9</span><span class="sxs-lookup"><span data-stu-id="78ce3-194">9</span></span> 
- <span data-ttu-id="78ce3-195">10</span><span class="sxs-lookup"><span data-stu-id="78ce3-195">10</span></span>

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

### <span data-ttu-id="78ce3-196">-Size</span><span class="sxs-lookup"><span data-stu-id="78ce3-196">-Size</span></span>
<span data-ttu-id="78ce3-197">Specifica le dimensioni della cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="78ce3-198">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78ce3-198">Valid values are:</span></span> 
- <span data-ttu-id="78ce3-199">P1</span><span class="sxs-lookup"><span data-stu-id="78ce3-199">P1</span></span>
- <span data-ttu-id="78ce3-200">P2</span><span class="sxs-lookup"><span data-stu-id="78ce3-200">P2</span></span>
- <span data-ttu-id="78ce3-201">P3</span><span class="sxs-lookup"><span data-stu-id="78ce3-201">P3</span></span>
- <span data-ttu-id="78ce3-202">P4</span><span class="sxs-lookup"><span data-stu-id="78ce3-202">P4</span></span>
- <span data-ttu-id="78ce3-203">P5</span><span class="sxs-lookup"><span data-stu-id="78ce3-203">P5</span></span>
- <span data-ttu-id="78ce3-204">C0</span><span class="sxs-lookup"><span data-stu-id="78ce3-204">C0</span></span>
- <span data-ttu-id="78ce3-205">C1</span><span class="sxs-lookup"><span data-stu-id="78ce3-205">C1</span></span>
- <span data-ttu-id="78ce3-206">C2</span><span class="sxs-lookup"><span data-stu-id="78ce3-206">C2</span></span>
- <span data-ttu-id="78ce3-207">C3</span><span class="sxs-lookup"><span data-stu-id="78ce3-207">C3</span></span>
- <span data-ttu-id="78ce3-208">C4</span><span class="sxs-lookup"><span data-stu-id="78ce3-208">C4</span></span>
- <span data-ttu-id="78ce3-209">C5</span><span class="sxs-lookup"><span data-stu-id="78ce3-209">C5</span></span>
- <span data-ttu-id="78ce3-210">C6</span><span class="sxs-lookup"><span data-stu-id="78ce3-210">C6</span></span>
- <span data-ttu-id="78ce3-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="78ce3-211">250MB</span></span>
- <span data-ttu-id="78ce3-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="78ce3-212">1GB</span></span>
- <span data-ttu-id="78ce3-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="78ce3-213">2.5GB</span></span>
- <span data-ttu-id="78ce3-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="78ce3-214">6GB</span></span>
- <span data-ttu-id="78ce3-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="78ce3-215">13GB</span></span>
- <span data-ttu-id="78ce3-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="78ce3-216">26GB</span></span>
- <span data-ttu-id="78ce3-217">53 GB Il valore predefinito è 1 GB o C1.</span><span class="sxs-lookup"><span data-stu-id="78ce3-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="78ce3-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="78ce3-218">-Sku</span></span>
<span data-ttu-id="78ce3-219">Specifica lo SKU della cache di Ridis da creare.</span><span class="sxs-lookup"><span data-stu-id="78ce3-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="78ce3-220">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78ce3-220">Valid values are:</span></span> 
- <span data-ttu-id="78ce3-221">Di base</span><span class="sxs-lookup"><span data-stu-id="78ce3-221">Basic</span></span>
- <span data-ttu-id="78ce3-222">Standard</span><span class="sxs-lookup"><span data-stu-id="78ce3-222">Standard</span></span>
- <span data-ttu-id="78ce3-223">Premium Il valore predefinito è Standard.</span><span class="sxs-lookup"><span data-stu-id="78ce3-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="78ce3-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="78ce3-224">-StaticIP</span></span>
<span data-ttu-id="78ce3-225">Specifica un indirizzo IP univoco nella subnet per la cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="78ce3-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="78ce3-226">Se non si specifica alcun valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="78ce3-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="78ce3-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="78ce3-227">-SubnetId</span></span>
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

### <span data-ttu-id="78ce3-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="78ce3-228">-Tag</span></span>
<span data-ttu-id="78ce3-229">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="78ce3-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="78ce3-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="78ce3-230">-TenantSettings</span></span>
<span data-ttu-id="78ce3-231">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="78ce3-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="78ce3-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="78ce3-232">-Zone</span></span>
<span data-ttu-id="78ce3-233">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="78ce3-233">List of zones.</span></span>

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

### <span data-ttu-id="78ce3-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78ce3-234">-Confirm</span></span>
<span data-ttu-id="78ce3-235">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ce3-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ce3-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ce3-236">-WhatIf</span></span>
<span data-ttu-id="78ce3-237">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78ce3-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78ce3-238">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78ce3-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ce3-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ce3-239">CommonParameters</span></span>
<span data-ttu-id="78ce3-240">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ce3-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ce3-241">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78ce3-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ce3-242">INPUT</span><span class="sxs-lookup"><span data-stu-id="78ce3-242">INPUTS</span></span>

### <span data-ttu-id="78ce3-243">System.String</span><span class="sxs-lookup"><span data-stu-id="78ce3-243">System.String</span></span>

### <span data-ttu-id="78ce3-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78ce3-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="78ce3-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78ce3-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78ce3-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78ce3-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78ce3-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="78ce3-247">System.String[]</span></span>

## <span data-ttu-id="78ce3-248">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78ce3-248">OUTPUTS</span></span>

### <span data-ttu-id="78ce3-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="78ce3-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="78ce3-250">NOTE</span><span class="sxs-lookup"><span data-stu-id="78ce3-250">NOTES</span></span>

## <span data-ttu-id="78ce3-251">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78ce3-251">RELATED LINKS</span></span>

[<span data-ttu-id="78ce3-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="78ce3-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="78ce3-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="78ce3-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="78ce3-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="78ce3-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


