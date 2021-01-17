---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474360"
---
# <span data-ttu-id="28b1f-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="28b1f-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="28b1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="28b1f-103">Modifica una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="28b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28b1f-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="28b1f-106">Il cmdlet **set-AzRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="28b1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="28b1f-108">Esempio 1: modificare una cache di redis</span><span class="sxs-lookup"><span data-stu-id="28b1f-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="28b1f-109">Questo comando Aggiorna i criteri di MaxMemory per la cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="28b1f-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="28b1f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="28b1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b1f-111">-DefaultProfile</span></span>
<span data-ttu-id="28b1f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28b1f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b1f-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="28b1f-113">-EnableNonSslPort</span></span>
<span data-ttu-id="28b1f-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="28b1f-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="28b1f-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="28b1f-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="28b1f-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="28b1f-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="28b1f-117">Specifica la versione TLS richiesta dai client per la connessione alla cache.</span><span class="sxs-lookup"><span data-stu-id="28b1f-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="28b1f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="28b1f-118">-Name</span></span>
<span data-ttu-id="28b1f-119">Specifica il nome della cache Redis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="28b1f-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="28b1f-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="28b1f-120">-RedisConfiguration</span></span>
<span data-ttu-id="28b1f-121">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="28b1f-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="28b1f-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28b1f-123">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="28b1f-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="28b1f-124">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="28b1f-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="28b1f-125">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-125">Premium tier only.</span></span>
- <span data-ttu-id="28b1f-126">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="28b1f-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="28b1f-127">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="28b1f-128">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-128">Premium tier only.</span></span>
- <span data-ttu-id="28b1f-129">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="28b1f-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="28b1f-130">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="28b1f-131">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-131">Premium tier only.</span></span> 
- <span data-ttu-id="28b1f-132">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="28b1f-132">maxmemory-reserved.</span></span>
<span data-ttu-id="28b1f-133">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="28b1f-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="28b1f-134">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-135">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="28b1f-135">maxmemory-policy.</span></span>
<span data-ttu-id="28b1f-136">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="28b1f-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="28b1f-137">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="28b1f-137">All pricing tiers.</span></span> 
- <span data-ttu-id="28b1f-138">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="28b1f-138">notify-keyspace-events.</span></span>
<span data-ttu-id="28b1f-139">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="28b1f-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="28b1f-140">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="28b1f-141">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="28b1f-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="28b1f-142">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="28b1f-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="28b1f-143">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-144">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="28b1f-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="28b1f-145">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="28b1f-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="28b1f-146">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-147">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="28b1f-147">set-max-intset-entries.</span></span>
<span data-ttu-id="28b1f-148">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="28b1f-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="28b1f-149">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-150">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="28b1f-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="28b1f-151">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="28b1f-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="28b1f-152">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-153">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="28b1f-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="28b1f-154">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="28b1f-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="28b1f-155">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="28b1f-156">database.</span><span class="sxs-lookup"><span data-stu-id="28b1f-156">databases.</span></span>
<span data-ttu-id="28b1f-157">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="28b1f-157">Configures the number of databases.</span></span>
<span data-ttu-id="28b1f-158">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="28b1f-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="28b1f-159">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="28b1f-160">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="28b1f-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="28b1f-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b1f-161">-ResourceGroupName</span></span>
<span data-ttu-id="28b1f-162">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="28b1f-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="28b1f-163">-ShardCount</span></span>
<span data-ttu-id="28b1f-164">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="28b1f-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="28b1f-165">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="28b1f-165">-Size</span></span>
<span data-ttu-id="28b1f-166">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="28b1f-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="28b1f-167">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="28b1f-167">Valid values are:</span></span> 
- <span data-ttu-id="28b1f-168">P1</span><span class="sxs-lookup"><span data-stu-id="28b1f-168">P1</span></span>
- <span data-ttu-id="28b1f-169">P2</span><span class="sxs-lookup"><span data-stu-id="28b1f-169">P2</span></span>
- <span data-ttu-id="28b1f-170">P3</span><span class="sxs-lookup"><span data-stu-id="28b1f-170">P3</span></span>
- <span data-ttu-id="28b1f-171">P4</span><span class="sxs-lookup"><span data-stu-id="28b1f-171">P4</span></span>
- <span data-ttu-id="28b1f-172">P5</span><span class="sxs-lookup"><span data-stu-id="28b1f-172">P5</span></span>
- <span data-ttu-id="28b1f-173">C0</span><span class="sxs-lookup"><span data-stu-id="28b1f-173">C0</span></span>
- <span data-ttu-id="28b1f-174">C1</span><span class="sxs-lookup"><span data-stu-id="28b1f-174">C1</span></span>
- <span data-ttu-id="28b1f-175">C2</span><span class="sxs-lookup"><span data-stu-id="28b1f-175">C2</span></span>
- <span data-ttu-id="28b1f-176">C3</span><span class="sxs-lookup"><span data-stu-id="28b1f-176">C3</span></span>
- <span data-ttu-id="28b1f-177">C4</span><span class="sxs-lookup"><span data-stu-id="28b1f-177">C4</span></span>
- <span data-ttu-id="28b1f-178">C5</span><span class="sxs-lookup"><span data-stu-id="28b1f-178">C5</span></span>
- <span data-ttu-id="28b1f-179">C6</span><span class="sxs-lookup"><span data-stu-id="28b1f-179">C6</span></span>
- <span data-ttu-id="28b1f-180">250MB</span><span class="sxs-lookup"><span data-stu-id="28b1f-180">250MB</span></span>
- <span data-ttu-id="28b1f-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-181">1GB</span></span>
- <span data-ttu-id="28b1f-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-182">2.5GB</span></span>
- <span data-ttu-id="28b1f-183">6GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-183">6GB</span></span>
- <span data-ttu-id="28b1f-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-184">13GB</span></span>
- <span data-ttu-id="28b1f-185">26GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-185">26GB</span></span>
- <span data-ttu-id="28b1f-186">53GB</span><span class="sxs-lookup"><span data-stu-id="28b1f-186">53GB</span></span>
- <span data-ttu-id="28b1f-187">120GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="28b1f-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="28b1f-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="28b1f-188">-Sku</span></span>
<span data-ttu-id="28b1f-189">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="28b1f-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="28b1f-190">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="28b1f-190">Valid values are:</span></span> 
- <span data-ttu-id="28b1f-191">Base</span><span class="sxs-lookup"><span data-stu-id="28b1f-191">Basic</span></span>
- <span data-ttu-id="28b1f-192">Standard</span><span class="sxs-lookup"><span data-stu-id="28b1f-192">Standard</span></span>
- <span data-ttu-id="28b1f-193">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="28b1f-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="28b1f-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="28b1f-194">-Tag</span></span>
<span data-ttu-id="28b1f-195">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="28b1f-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="28b1f-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="28b1f-196">-TenantSettings</span></span>
<span data-ttu-id="28b1f-197">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="28b1f-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="28b1f-198">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28b1f-198">-Confirm</span></span>
<span data-ttu-id="28b1f-199">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b1f-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b1f-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b1f-200">-WhatIf</span></span>
<span data-ttu-id="28b1f-201">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28b1f-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28b1f-202">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28b1f-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b1f-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b1f-203">CommonParameters</span></span>
<span data-ttu-id="28b1f-204">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b1f-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b1f-205">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28b1f-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b1f-206">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28b1f-206">INPUTS</span></span>

### <span data-ttu-id="28b1f-207">System. String</span><span class="sxs-lookup"><span data-stu-id="28b1f-207">System.String</span></span>

### <span data-ttu-id="28b1f-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="28b1f-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="28b1f-209">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="28b1f-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="28b1f-210">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="28b1f-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="28b1f-211">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28b1f-211">OUTPUTS</span></span>

### <span data-ttu-id="28b1f-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="28b1f-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="28b1f-213">Note</span><span class="sxs-lookup"><span data-stu-id="28b1f-213">NOTES</span></span>

## <span data-ttu-id="28b1f-214">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28b1f-214">RELATED LINKS</span></span>

[<span data-ttu-id="28b1f-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="28b1f-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="28b1f-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="28b1f-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="28b1f-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="28b1f-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


