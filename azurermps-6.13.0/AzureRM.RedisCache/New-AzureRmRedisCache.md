---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686903"
---
# <span data-ttu-id="f4b62-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4b62-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="f4b62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4b62-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b62-103">Crea una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4b62-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b62-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4b62-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b62-106">Il cmdlet **New-AzureRmRedisCache** crea una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="f4b62-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4b62-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b62-108">Esempio 1: creare una cache Redis</span><span class="sxs-lookup"><span data-stu-id="f4b62-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="f4b62-109">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="f4b62-110">Esempio 2: creare una cache di redis standard SKU</span><span class="sxs-lookup"><span data-stu-id="f4b62-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="f4b62-111">Questo comando crea una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="f4b62-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4b62-112">PARAMETERS</span></span>

### <span data-ttu-id="f4b62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b62-113">-DefaultProfile</span></span>
<span data-ttu-id="f4b62-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b62-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f4b62-115">-EnableNonSslPort</span></span>
<span data-ttu-id="f4b62-116">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f4b62-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f4b62-117">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="f4b62-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f4b62-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f4b62-118">-Location</span></span>
<span data-ttu-id="f4b62-119">Specifica la posizione in cui creare una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="f4b62-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f4b62-120">Valid values are:</span></span> 
- <span data-ttu-id="f4b62-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="f4b62-121">North Central US</span></span>
- <span data-ttu-id="f4b62-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="f4b62-122">South Central US</span></span>
- <span data-ttu-id="f4b62-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="f4b62-123">Central US</span></span>
- <span data-ttu-id="f4b62-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="f4b62-124">West Europe</span></span>
- <span data-ttu-id="f4b62-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="f4b62-125">North Europe</span></span>
- <span data-ttu-id="f4b62-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="f4b62-126">West US</span></span>
- <span data-ttu-id="f4b62-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="f4b62-127">East US</span></span>
- <span data-ttu-id="f4b62-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="f4b62-128">East US 2</span></span>
- <span data-ttu-id="f4b62-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="f4b62-129">Japan East</span></span>
- <span data-ttu-id="f4b62-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="f4b62-130">Japan West</span></span>
- <span data-ttu-id="f4b62-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="f4b62-131">Brazil South</span></span>
- <span data-ttu-id="f4b62-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="f4b62-132">Southeast Asia</span></span>
- <span data-ttu-id="f4b62-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="f4b62-133">East Asia</span></span>
- <span data-ttu-id="f4b62-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="f4b62-134">Australia East</span></span>
- <span data-ttu-id="f4b62-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="f4b62-135">Australia Southeast</span></span>

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

### <span data-ttu-id="f4b62-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4b62-136">-Name</span></span>
<span data-ttu-id="f4b62-137">Specifica il nome della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="f4b62-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="f4b62-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4b62-138">-RedisConfiguration</span></span>
<span data-ttu-id="f4b62-139">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f4b62-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4b62-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4b62-141">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="f4b62-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="f4b62-142">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f4b62-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f4b62-143">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-143">Premium tier only.</span></span>
- <span data-ttu-id="f4b62-144">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="f4b62-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f4b62-145">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f4b62-146">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-146">Premium tier only.</span></span>
- <span data-ttu-id="f4b62-147">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="f4b62-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="f4b62-148">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f4b62-149">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-149">Premium tier only.</span></span> 
- <span data-ttu-id="f4b62-150">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="f4b62-150">maxmemory-reserved.</span></span>
<span data-ttu-id="f4b62-151">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="f4b62-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f4b62-152">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-153">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="f4b62-153">maxmemory-policy.</span></span>
<span data-ttu-id="f4b62-154">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="f4b62-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f4b62-155">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="f4b62-155">All pricing tiers.</span></span> 
- <span data-ttu-id="f4b62-156">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="f4b62-156">notify-keyspace-events.</span></span>
<span data-ttu-id="f4b62-157">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="f4b62-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="f4b62-158">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f4b62-159">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="f4b62-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f4b62-160">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f4b62-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f4b62-161">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-162">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="f4b62-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f4b62-163">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f4b62-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f4b62-164">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-165">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="f4b62-165">set-max-intset-entries.</span></span>
<span data-ttu-id="f4b62-166">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f4b62-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f4b62-167">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-168">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="f4b62-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f4b62-169">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f4b62-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f4b62-170">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-171">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="f4b62-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f4b62-172">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="f4b62-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f4b62-173">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f4b62-174">database.</span><span class="sxs-lookup"><span data-stu-id="f4b62-174">databases.</span></span>
<span data-ttu-id="f4b62-175">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="f4b62-175">Configures the number of databases.</span></span>
<span data-ttu-id="f4b62-176">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="f4b62-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f4b62-177">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="f4b62-178">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f4b62-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f4b62-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b62-179">-ResourceGroupName</span></span>
<span data-ttu-id="f4b62-180">Specifica il nome del gruppo di risorse in cui creare la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="f4b62-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f4b62-181">-ShardCount</span></span>
<span data-ttu-id="f4b62-182">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="f4b62-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="f4b62-183">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4b62-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4b62-184">1</span><span class="sxs-lookup"><span data-stu-id="f4b62-184">1</span></span>
- <span data-ttu-id="f4b62-185">2</span><span class="sxs-lookup"><span data-stu-id="f4b62-185">2</span></span>
- <span data-ttu-id="f4b62-186">3</span><span class="sxs-lookup"><span data-stu-id="f4b62-186">3</span></span>
- <span data-ttu-id="f4b62-187">4</span><span class="sxs-lookup"><span data-stu-id="f4b62-187">4</span></span>
- <span data-ttu-id="f4b62-188">5</span><span class="sxs-lookup"><span data-stu-id="f4b62-188">5</span></span>
- <span data-ttu-id="f4b62-189">6</span><span class="sxs-lookup"><span data-stu-id="f4b62-189">6</span></span>
- <span data-ttu-id="f4b62-190">7</span><span class="sxs-lookup"><span data-stu-id="f4b62-190">7</span></span>
- <span data-ttu-id="f4b62-191">8</span><span class="sxs-lookup"><span data-stu-id="f4b62-191">8</span></span>
- <span data-ttu-id="f4b62-192">9</span><span class="sxs-lookup"><span data-stu-id="f4b62-192">9</span></span> 
- <span data-ttu-id="f4b62-193">10</span><span class="sxs-lookup"><span data-stu-id="f4b62-193">10</span></span>

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

### <span data-ttu-id="f4b62-194">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="f4b62-194">-Size</span></span>
<span data-ttu-id="f4b62-195">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f4b62-196">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f4b62-196">Valid values are:</span></span> 
- <span data-ttu-id="f4b62-197">P1</span><span class="sxs-lookup"><span data-stu-id="f4b62-197">P1</span></span>
- <span data-ttu-id="f4b62-198">P2</span><span class="sxs-lookup"><span data-stu-id="f4b62-198">P2</span></span>
- <span data-ttu-id="f4b62-199">P3</span><span class="sxs-lookup"><span data-stu-id="f4b62-199">P3</span></span>
- <span data-ttu-id="f4b62-200">P4</span><span class="sxs-lookup"><span data-stu-id="f4b62-200">P4</span></span>
- <span data-ttu-id="f4b62-201">C0</span><span class="sxs-lookup"><span data-stu-id="f4b62-201">C0</span></span>
- <span data-ttu-id="f4b62-202">C1</span><span class="sxs-lookup"><span data-stu-id="f4b62-202">C1</span></span>
- <span data-ttu-id="f4b62-203">C2</span><span class="sxs-lookup"><span data-stu-id="f4b62-203">C2</span></span>
- <span data-ttu-id="f4b62-204">C3</span><span class="sxs-lookup"><span data-stu-id="f4b62-204">C3</span></span>
- <span data-ttu-id="f4b62-205">C4</span><span class="sxs-lookup"><span data-stu-id="f4b62-205">C4</span></span>
- <span data-ttu-id="f4b62-206">C5</span><span class="sxs-lookup"><span data-stu-id="f4b62-206">C5</span></span>
- <span data-ttu-id="f4b62-207">C6</span><span class="sxs-lookup"><span data-stu-id="f4b62-207">C6</span></span>
- <span data-ttu-id="f4b62-208">250MB</span><span class="sxs-lookup"><span data-stu-id="f4b62-208">250MB</span></span>
- <span data-ttu-id="f4b62-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="f4b62-209">1GB</span></span>
- <span data-ttu-id="f4b62-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f4b62-210">2.5GB</span></span>
- <span data-ttu-id="f4b62-211">6GB</span><span class="sxs-lookup"><span data-stu-id="f4b62-211">6GB</span></span>
- <span data-ttu-id="f4b62-212">13 GB</span><span class="sxs-lookup"><span data-stu-id="f4b62-212">13GB</span></span>
- <span data-ttu-id="f4b62-213">26GB</span><span class="sxs-lookup"><span data-stu-id="f4b62-213">26GB</span></span>
- <span data-ttu-id="f4b62-214">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="f4b62-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f4b62-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="f4b62-215">-Sku</span></span>
<span data-ttu-id="f4b62-216">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="f4b62-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f4b62-217">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f4b62-217">Valid values are:</span></span> 
- <span data-ttu-id="f4b62-218">Base</span><span class="sxs-lookup"><span data-stu-id="f4b62-218">Basic</span></span>
- <span data-ttu-id="f4b62-219">Standard</span><span class="sxs-lookup"><span data-stu-id="f4b62-219">Standard</span></span>
- <span data-ttu-id="f4b62-220">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="f4b62-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="f4b62-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="f4b62-221">-StaticIP</span></span>
<span data-ttu-id="f4b62-222">Specifica un indirizzo IP univoco nella subnet per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f4b62-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="f4b62-223">Se non specifichi un valore per questo parametro, questo cmdlet sceglie un indirizzo IP dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="f4b62-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="f4b62-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f4b62-224">-SubnetId</span></span>
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

### <span data-ttu-id="f4b62-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4b62-225">-Tag</span></span>
<span data-ttu-id="f4b62-226">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="f4b62-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="f4b62-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f4b62-227">-TenantSettings</span></span>
<span data-ttu-id="f4b62-228">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="f4b62-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f4b62-229">-Zona</span><span class="sxs-lookup"><span data-stu-id="f4b62-229">-Zone</span></span>
<span data-ttu-id="f4b62-230">Elenco di aree.</span><span class="sxs-lookup"><span data-stu-id="f4b62-230">List of zones.</span></span>

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

### <span data-ttu-id="f4b62-231">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4b62-231">-Confirm</span></span>
<span data-ttu-id="f4b62-232">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b62-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b62-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b62-233">-WhatIf</span></span>
<span data-ttu-id="f4b62-234">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4b62-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4b62-235">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4b62-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b62-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b62-236">CommonParameters</span></span>
<span data-ttu-id="f4b62-237">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b62-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b62-238">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b62-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b62-239">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4b62-239">INPUTS</span></span>

### <span data-ttu-id="f4b62-240">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b62-240">System.String</span></span>

### <span data-ttu-id="f4b62-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4b62-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f4b62-242">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f4b62-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f4b62-243">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f4b62-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f4b62-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="f4b62-244">System.String[]</span></span>

## <span data-ttu-id="f4b62-245">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4b62-245">OUTPUTS</span></span>

### <span data-ttu-id="f4b62-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f4b62-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f4b62-247">Note</span><span class="sxs-lookup"><span data-stu-id="f4b62-247">NOTES</span></span>

## <span data-ttu-id="f4b62-248">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4b62-248">RELATED LINKS</span></span>

[<span data-ttu-id="f4b62-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4b62-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="f4b62-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4b62-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f4b62-251">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4b62-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


