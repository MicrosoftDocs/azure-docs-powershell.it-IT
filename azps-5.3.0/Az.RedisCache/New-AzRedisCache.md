---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474380"
---
# <span data-ttu-id="f91e5-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f91e5-101">New-AzRedisCache</span></span>

## <span data-ttu-id="f91e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f91e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f91e5-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="f91e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f91e5-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f91e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f91e5-105">DESCRIPTION</span></span>
<span data-ttu-id="f91e5-106">Il cmdlet **New-AzRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="f91e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f91e5-107">EXAMPLES</span></span>

### <span data-ttu-id="f91e5-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="f91e5-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="f91e5-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="f91e5-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="f91e5-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="f91e5-111">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="f91e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f91e5-112">PARAMETERS</span></span>

### <span data-ttu-id="f91e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91e5-113">-DefaultProfile</span></span>
<span data-ttu-id="f91e5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f91e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f91e5-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f91e5-115">-EnableNonSslPort</span></span>
<span data-ttu-id="f91e5-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f91e5-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f91e5-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="f91e5-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f91e5-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f91e5-118">-Location</span></span>
<span data-ttu-id="f91e5-119">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="f91e5-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f91e5-120">Valid values are:</span></span> 
- <span data-ttu-id="f91e5-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="f91e5-121">North Central US</span></span>
- <span data-ttu-id="f91e5-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="f91e5-122">South Central US</span></span>
- <span data-ttu-id="f91e5-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="f91e5-123">Central US</span></span>
- <span data-ttu-id="f91e5-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="f91e5-124">West Europe</span></span>
- <span data-ttu-id="f91e5-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="f91e5-125">North Europe</span></span>
- <span data-ttu-id="f91e5-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="f91e5-126">West US</span></span>
- <span data-ttu-id="f91e5-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="f91e5-127">East US</span></span>
- <span data-ttu-id="f91e5-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="f91e5-128">East US 2</span></span>
- <span data-ttu-id="f91e5-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="f91e5-129">Japan East</span></span>
- <span data-ttu-id="f91e5-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="f91e5-130">Japan West</span></span>
- <span data-ttu-id="f91e5-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="f91e5-131">Brazil South</span></span>
- <span data-ttu-id="f91e5-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="f91e5-132">Southeast Asia</span></span>
- <span data-ttu-id="f91e5-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="f91e5-133">East Asia</span></span>
- <span data-ttu-id="f91e5-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="f91e5-134">Australia East</span></span>
- <span data-ttu-id="f91e5-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="f91e5-135">Australia Southeast</span></span>

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

### <span data-ttu-id="f91e5-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f91e5-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="f91e5-137">Specifica la versione TLS richiesta dai client per la connessione alla cache.</span><span class="sxs-lookup"><span data-stu-id="f91e5-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="f91e5-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="f91e5-138">-Name</span></span>
<span data-ttu-id="f91e5-139">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="f91e5-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="f91e5-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f91e5-140">-RedisConfiguration</span></span>
<span data-ttu-id="f91e5-141">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f91e5-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f91e5-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f91e5-143">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="f91e5-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="f91e5-144">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f91e5-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f91e5-145">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-145">Premium tier only.</span></span>
- <span data-ttu-id="f91e5-146">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="f91e5-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f91e5-147">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f91e5-148">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-148">Premium tier only.</span></span>
- <span data-ttu-id="f91e5-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="f91e5-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="f91e5-150">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f91e5-151">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-151">Premium tier only.</span></span> 
- <span data-ttu-id="f91e5-152">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="f91e5-152">maxmemory-reserved.</span></span>
<span data-ttu-id="f91e5-153">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="f91e5-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f91e5-154">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-155">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="f91e5-155">maxmemory-policy.</span></span>
<span data-ttu-id="f91e5-156">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="f91e5-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f91e5-157">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="f91e5-157">All pricing tiers.</span></span> 
- <span data-ttu-id="f91e5-158">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="f91e5-158">notify-keyspace-events.</span></span>
<span data-ttu-id="f91e5-159">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="f91e5-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="f91e5-160">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f91e5-161">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="f91e5-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f91e5-162">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f91e5-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f91e5-163">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-164">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="f91e5-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f91e5-165">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f91e5-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f91e5-166">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-167">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="f91e5-167">set-max-intset-entries.</span></span>
<span data-ttu-id="f91e5-168">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f91e5-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f91e5-169">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-170">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="f91e5-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f91e5-171">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f91e5-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f91e5-172">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-173">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="f91e5-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f91e5-174">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f91e5-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f91e5-175">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f91e5-176">database.</span><span class="sxs-lookup"><span data-stu-id="f91e5-176">databases.</span></span>
<span data-ttu-id="f91e5-177">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="f91e5-177">Configures the number of databases.</span></span>
<span data-ttu-id="f91e5-178">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="f91e5-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f91e5-179">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="f91e5-180">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f91e5-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f91e5-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91e5-181">-ResourceGroupName</span></span>
<span data-ttu-id="f91e5-182">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="f91e5-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f91e5-183">-ShardCount</span></span>
<span data-ttu-id="f91e5-184">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="f91e5-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="f91e5-185">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f91e5-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f91e5-186">1</span><span class="sxs-lookup"><span data-stu-id="f91e5-186">1</span></span>
- <span data-ttu-id="f91e5-187">2</span><span class="sxs-lookup"><span data-stu-id="f91e5-187">2</span></span>
- <span data-ttu-id="f91e5-188">3</span><span class="sxs-lookup"><span data-stu-id="f91e5-188">3</span></span>
- <span data-ttu-id="f91e5-189">4</span><span class="sxs-lookup"><span data-stu-id="f91e5-189">4</span></span>
- <span data-ttu-id="f91e5-190">5</span><span class="sxs-lookup"><span data-stu-id="f91e5-190">5</span></span>
- <span data-ttu-id="f91e5-191">6</span><span class="sxs-lookup"><span data-stu-id="f91e5-191">6</span></span>
- <span data-ttu-id="f91e5-192">7</span><span class="sxs-lookup"><span data-stu-id="f91e5-192">7</span></span>
- <span data-ttu-id="f91e5-193">8</span><span class="sxs-lookup"><span data-stu-id="f91e5-193">8</span></span>
- <span data-ttu-id="f91e5-194">9</span><span class="sxs-lookup"><span data-stu-id="f91e5-194">9</span></span> 
- <span data-ttu-id="f91e5-195">10</span><span class="sxs-lookup"><span data-stu-id="f91e5-195">10</span></span>

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

### <span data-ttu-id="f91e5-196">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="f91e5-196">-Size</span></span>
<span data-ttu-id="f91e5-197">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f91e5-198">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f91e5-198">Valid values are:</span></span> 
- <span data-ttu-id="f91e5-199">P1</span><span class="sxs-lookup"><span data-stu-id="f91e5-199">P1</span></span>
- <span data-ttu-id="f91e5-200">P2</span><span class="sxs-lookup"><span data-stu-id="f91e5-200">P2</span></span>
- <span data-ttu-id="f91e5-201">P3</span><span class="sxs-lookup"><span data-stu-id="f91e5-201">P3</span></span>
- <span data-ttu-id="f91e5-202">P4</span><span class="sxs-lookup"><span data-stu-id="f91e5-202">P4</span></span>
- <span data-ttu-id="f91e5-203">P5</span><span class="sxs-lookup"><span data-stu-id="f91e5-203">P5</span></span>
- <span data-ttu-id="f91e5-204">C0</span><span class="sxs-lookup"><span data-stu-id="f91e5-204">C0</span></span>
- <span data-ttu-id="f91e5-205">C1</span><span class="sxs-lookup"><span data-stu-id="f91e5-205">C1</span></span>
- <span data-ttu-id="f91e5-206">C2</span><span class="sxs-lookup"><span data-stu-id="f91e5-206">C2</span></span>
- <span data-ttu-id="f91e5-207">C3</span><span class="sxs-lookup"><span data-stu-id="f91e5-207">C3</span></span>
- <span data-ttu-id="f91e5-208">C4</span><span class="sxs-lookup"><span data-stu-id="f91e5-208">C4</span></span>
- <span data-ttu-id="f91e5-209">C5</span><span class="sxs-lookup"><span data-stu-id="f91e5-209">C5</span></span>
- <span data-ttu-id="f91e5-210">C6</span><span class="sxs-lookup"><span data-stu-id="f91e5-210">C6</span></span>
- <span data-ttu-id="f91e5-211">250MB</span><span class="sxs-lookup"><span data-stu-id="f91e5-211">250MB</span></span>
- <span data-ttu-id="f91e5-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="f91e5-212">1GB</span></span>
- <span data-ttu-id="f91e5-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f91e5-213">2.5GB</span></span>
- <span data-ttu-id="f91e5-214">6GB</span><span class="sxs-lookup"><span data-stu-id="f91e5-214">6GB</span></span>
- <span data-ttu-id="f91e5-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="f91e5-215">13GB</span></span>
- <span data-ttu-id="f91e5-216">26GB</span><span class="sxs-lookup"><span data-stu-id="f91e5-216">26GB</span></span>
- <span data-ttu-id="f91e5-217">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="f91e5-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f91e5-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="f91e5-218">-Sku</span></span>
<span data-ttu-id="f91e5-219">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="f91e5-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f91e5-220">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f91e5-220">Valid values are:</span></span> 
- <span data-ttu-id="f91e5-221">Base</span><span class="sxs-lookup"><span data-stu-id="f91e5-221">Basic</span></span>
- <span data-ttu-id="f91e5-222">Standard</span><span class="sxs-lookup"><span data-stu-id="f91e5-222">Standard</span></span>
- <span data-ttu-id="f91e5-223">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="f91e5-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="f91e5-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="f91e5-224">-StaticIP</span></span>
<span data-ttu-id="f91e5-225">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f91e5-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="f91e5-226">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="f91e5-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="f91e5-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f91e5-227">-SubnetId</span></span>
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

### <span data-ttu-id="f91e5-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="f91e5-228">-Tag</span></span>
<span data-ttu-id="f91e5-229">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="f91e5-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="f91e5-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f91e5-230">-TenantSettings</span></span>
<span data-ttu-id="f91e5-231">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="f91e5-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f91e5-232">-Zona</span><span class="sxs-lookup"><span data-stu-id="f91e5-232">-Zone</span></span>
<span data-ttu-id="f91e5-233">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="f91e5-233">List of zones.</span></span>

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

### <span data-ttu-id="f91e5-234">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f91e5-234">-Confirm</span></span>
<span data-ttu-id="f91e5-235">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f91e5-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91e5-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91e5-236">-WhatIf</span></span>
<span data-ttu-id="f91e5-237">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f91e5-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f91e5-238">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f91e5-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91e5-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91e5-239">CommonParameters</span></span>
<span data-ttu-id="f91e5-240">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f91e5-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91e5-241">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f91e5-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91e5-242">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f91e5-242">INPUTS</span></span>

### <span data-ttu-id="f91e5-243">System. String</span><span class="sxs-lookup"><span data-stu-id="f91e5-243">System.String</span></span>

### <span data-ttu-id="f91e5-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f91e5-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f91e5-245">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f91e5-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f91e5-246">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f91e5-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f91e5-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="f91e5-247">System.String[]</span></span>

## <span data-ttu-id="f91e5-248">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f91e5-248">OUTPUTS</span></span>

### <span data-ttu-id="f91e5-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f91e5-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f91e5-250">Note</span><span class="sxs-lookup"><span data-stu-id="f91e5-250">NOTES</span></span>

## <span data-ttu-id="f91e5-251">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f91e5-251">RELATED LINKS</span></span>

[<span data-ttu-id="f91e5-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f91e5-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f91e5-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f91e5-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f91e5-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f91e5-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


