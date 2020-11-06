---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520873"
---
# <span data-ttu-id="9a093-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9a093-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="9a093-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a093-102">SYNOPSIS</span></span>
<span data-ttu-id="9a093-103">Modifica una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a093-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a093-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a093-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a093-105">DESCRIPTION</span></span>
<span data-ttu-id="9a093-106">Il cmdlet **set-AzureRmRedisCache** modifica una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="9a093-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a093-107">EXAMPLES</span></span>

### <span data-ttu-id="9a093-108">Esempio 1: modificare una cache di redis</span><span class="sxs-lookup"><span data-stu-id="9a093-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="9a093-109">Questo comando Aggiorna i criteri di MaxMemory per la cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="9a093-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="9a093-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a093-110">PARAMETERS</span></span>

### <span data-ttu-id="9a093-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a093-111">-DefaultProfile</span></span>
<span data-ttu-id="9a093-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a093-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a093-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="9a093-113">-EnableNonSslPort</span></span>
<span data-ttu-id="9a093-114">Indica se la porta non SSL è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9a093-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="9a093-115">Il valore predefinito è $False (la porta non SSL è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="9a093-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="9a093-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a093-116">-Name</span></span>
<span data-ttu-id="9a093-117">Specifica il nome della cache Redis da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9a093-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="9a093-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a093-118">-RedisConfiguration</span></span>
<span data-ttu-id="9a093-119">Specifica le impostazioni di configurazione di Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="9a093-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a093-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a093-121">RDB-backup-Enabled.</span><span class="sxs-lookup"><span data-stu-id="9a093-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="9a093-122">Specifica che la persistenza dei dati di redis è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9a093-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="9a093-123">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-123">Premium tier only.</span></span>
- <span data-ttu-id="9a093-124">RDB-storage-Connection-String.</span><span class="sxs-lookup"><span data-stu-id="9a093-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="9a093-125">Specifica la stringa di connessione all'account di archiviazione per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="9a093-126">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-126">Premium tier only.</span></span>
- <span data-ttu-id="9a093-127">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="9a093-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="9a093-128">Specifica la frequenza di backup per la persistenza dei dati Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="9a093-129">Solo livello Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-129">Premium tier only.</span></span> 
- <span data-ttu-id="9a093-130">MaxMemory-riservato.</span><span class="sxs-lookup"><span data-stu-id="9a093-130">maxmemory-reserved.</span></span>
<span data-ttu-id="9a093-131">Configura la memoria riservata per i processi non della cache.</span><span class="sxs-lookup"><span data-stu-id="9a093-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="9a093-132">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-133">MaxMemory-Policy.</span><span class="sxs-lookup"><span data-stu-id="9a093-133">maxmemory-policy.</span></span>
<span data-ttu-id="9a093-134">Configura i criteri di eliminazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="9a093-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="9a093-135">Tutti i livelli di prezzo.</span><span class="sxs-lookup"><span data-stu-id="9a093-135">All pricing tiers.</span></span> 
- <span data-ttu-id="9a093-136">Notify-barra spaziatrice-eventi.</span><span class="sxs-lookup"><span data-stu-id="9a093-136">notify-keyspace-events.</span></span>
<span data-ttu-id="9a093-137">Configura le notifiche di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="9a093-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="9a093-138">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="9a093-139">hash-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="9a093-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="9a093-140">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="9a093-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9a093-141">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-142">hash-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="9a093-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="9a093-143">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="9a093-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9a093-144">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-145">set-max-intert-voci.</span><span class="sxs-lookup"><span data-stu-id="9a093-145">set-max-intset-entries.</span></span>
<span data-ttu-id="9a093-146">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="9a093-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9a093-147">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-148">Zset-max-ZipList-voci.</span><span class="sxs-lookup"><span data-stu-id="9a093-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="9a093-149">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="9a093-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9a093-150">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-151">Zset-max-ZipList-valore.</span><span class="sxs-lookup"><span data-stu-id="9a093-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="9a093-152">Configura l'ottimizzazione della memoria per i piccoli tipi di dati aggregati.</span><span class="sxs-lookup"><span data-stu-id="9a093-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9a093-153">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9a093-154">database.</span><span class="sxs-lookup"><span data-stu-id="9a093-154">databases.</span></span>
<span data-ttu-id="9a093-155">Configura il numero di database.</span><span class="sxs-lookup"><span data-stu-id="9a093-155">Configures the number of databases.</span></span>
<span data-ttu-id="9a093-156">Questa proprietà può essere configurata solo in fase di creazione della cache.</span><span class="sxs-lookup"><span data-stu-id="9a093-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="9a093-157">Livelli standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="9a093-158">Per altre informazioni, vedere gestire la cache di Azure Redis con Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="9a093-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="9a093-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a093-159">-ResourceGroupName</span></span>
<span data-ttu-id="9a093-160">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="9a093-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="9a093-161">-ShardCount</span></span>
<span data-ttu-id="9a093-162">Specifica il numero di frammenti da creare in una cache di cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="9a093-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="9a093-163">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="9a093-163">-Size</span></span>
<span data-ttu-id="9a093-164">Specifica le dimensioni della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9a093-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="9a093-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9a093-165">Valid values are:</span></span> 
- <span data-ttu-id="9a093-166">P1</span><span class="sxs-lookup"><span data-stu-id="9a093-166">P1</span></span>
- <span data-ttu-id="9a093-167">P2</span><span class="sxs-lookup"><span data-stu-id="9a093-167">P2</span></span>
- <span data-ttu-id="9a093-168">P3</span><span class="sxs-lookup"><span data-stu-id="9a093-168">P3</span></span>
- <span data-ttu-id="9a093-169">P4</span><span class="sxs-lookup"><span data-stu-id="9a093-169">P4</span></span>
- <span data-ttu-id="9a093-170">C0</span><span class="sxs-lookup"><span data-stu-id="9a093-170">C0</span></span>
- <span data-ttu-id="9a093-171">C1</span><span class="sxs-lookup"><span data-stu-id="9a093-171">C1</span></span>
- <span data-ttu-id="9a093-172">C2</span><span class="sxs-lookup"><span data-stu-id="9a093-172">C2</span></span>
- <span data-ttu-id="9a093-173">C3</span><span class="sxs-lookup"><span data-stu-id="9a093-173">C3</span></span>
- <span data-ttu-id="9a093-174">C4</span><span class="sxs-lookup"><span data-stu-id="9a093-174">C4</span></span>
- <span data-ttu-id="9a093-175">C5</span><span class="sxs-lookup"><span data-stu-id="9a093-175">C5</span></span>
- <span data-ttu-id="9a093-176">C6</span><span class="sxs-lookup"><span data-stu-id="9a093-176">C6</span></span>
- <span data-ttu-id="9a093-177">250MB</span><span class="sxs-lookup"><span data-stu-id="9a093-177">250MB</span></span>
- <span data-ttu-id="9a093-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="9a093-178">1GB</span></span>
- <span data-ttu-id="9a093-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9a093-179">2.5GB</span></span>
- <span data-ttu-id="9a093-180">6GB</span><span class="sxs-lookup"><span data-stu-id="9a093-180">6GB</span></span>
- <span data-ttu-id="9a093-181">13 GB</span><span class="sxs-lookup"><span data-stu-id="9a093-181">13GB</span></span>
- <span data-ttu-id="9a093-182">26GB</span><span class="sxs-lookup"><span data-stu-id="9a093-182">26GB</span></span>
- <span data-ttu-id="9a093-183">53GB il valore predefinito è 1GB o C1.</span><span class="sxs-lookup"><span data-stu-id="9a093-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="9a093-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="9a093-184">-Sku</span></span>
<span data-ttu-id="9a093-185">Specifica l'USK della cache Redis da creare.</span><span class="sxs-lookup"><span data-stu-id="9a093-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="9a093-186">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9a093-186">Valid values are:</span></span> 
- <span data-ttu-id="9a093-187">Base</span><span class="sxs-lookup"><span data-stu-id="9a093-187">Basic</span></span>
- <span data-ttu-id="9a093-188">Standard</span><span class="sxs-lookup"><span data-stu-id="9a093-188">Standard</span></span>
- <span data-ttu-id="9a093-189">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="9a093-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="9a093-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a093-190">-Tag</span></span>
<span data-ttu-id="9a093-191">Tabella hash che rappresenta i tag.</span><span class="sxs-lookup"><span data-stu-id="9a093-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="9a093-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="9a093-192">-TenantSettings</span></span>
<span data-ttu-id="9a093-193">Questo parametro è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="9a093-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="9a093-194">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a093-194">-Confirm</span></span>
<span data-ttu-id="9a093-195">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a093-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a093-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a093-196">-WhatIf</span></span>
<span data-ttu-id="9a093-197">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a093-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a093-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a093-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a093-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a093-199">CommonParameters</span></span>
<span data-ttu-id="9a093-200">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a093-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a093-201">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a093-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a093-202">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a093-202">INPUTS</span></span>

### <span data-ttu-id="9a093-203">System. String</span><span class="sxs-lookup"><span data-stu-id="9a093-203">System.String</span></span>

### <span data-ttu-id="9a093-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9a093-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9a093-205">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9a093-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9a093-206">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9a093-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9a093-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a093-207">OUTPUTS</span></span>

### <span data-ttu-id="9a093-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9a093-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="9a093-209">Note</span><span class="sxs-lookup"><span data-stu-id="9a093-209">NOTES</span></span>

## <span data-ttu-id="9a093-210">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a093-210">RELATED LINKS</span></span>

[<span data-ttu-id="9a093-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9a093-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="9a093-212">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9a093-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="9a093-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9a093-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


