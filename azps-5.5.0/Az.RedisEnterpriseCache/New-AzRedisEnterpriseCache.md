---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201966"
---
# <span data-ttu-id="446ec-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="446ec-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="446ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446ec-102">SYNOPSIS</span></span>
<span data-ttu-id="446ec-103">Crea un cluster di cache di Ridisposizione e un database associato</span><span class="sxs-lookup"><span data-stu-id="446ec-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="446ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="446ec-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="446ec-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="446ec-105">DESCRIPTION</span></span>
<span data-ttu-id="446ec-106">Crea o aggiorna un cluster di cache esistente (sovrascrive/ricrea con potenziale tempo di inattività) e un database associato denominato "predefinito"</span><span class="sxs-lookup"><span data-stu-id="446ec-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="446ec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="446ec-107">EXAMPLES</span></span>

### <span data-ttu-id="446ec-108">Esempio 1: Creare una cache aziendale di Ridis</span><span class="sxs-lookup"><span data-stu-id="446ec-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="446ec-109">Questo comando crea una cache dell'organizzazione di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="446ec-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="446ec-110">Esempio 2: Creare una cache aziendale di Redis usando alcuni parametri facoltativi</span><span class="sxs-lookup"><span data-stu-id="446ec-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="446ec-111">Questo comando crea una cache dell'organizzazione di Redis denominata MyCache usando alcuni parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="446ec-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="446ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="446ec-112">PARAMETERS</span></span>

### <span data-ttu-id="446ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="446ec-113">-AsJob</span></span>
<span data-ttu-id="446ec-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="446ec-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-115">-Capacità</span><span class="sxs-lookup"><span data-stu-id="446ec-115">-Capacity</span></span>
<span data-ttu-id="446ec-116">Dimensioni del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="446ec-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="446ec-117">Il valore predefinito è 2 o 3 a seconda dello SKU.</span><span class="sxs-lookup"><span data-stu-id="446ec-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="446ec-118">I valori validi sono (2, 4, 6, ...) per SKU Enterprise e (3, 9, 15, ...) per gli SKU Flash.</span><span class="sxs-lookup"><span data-stu-id="446ec-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="446ec-119">-ClientProtocol</span></span>
<span data-ttu-id="446ec-120">Specifica se i client ridisposizione possono connettersi usando protocolli didis con crittografia TLS o testo normale.</span><span class="sxs-lookup"><span data-stu-id="446ec-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="446ec-121">Il valore predefinito è TLS-encrypted.</span><span class="sxs-lookup"><span data-stu-id="446ec-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="446ec-122">-ClusteringPolicy</span></span>
<span data-ttu-id="446ec-123">Criterio di clustering: il valore predefinito è OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="446ec-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="446ec-124">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="446ec-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="446ec-125">-ClusterName</span></span>
<span data-ttu-id="446ec-126">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="446ec-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446ec-127">-DefaultProfile</span></span>
<span data-ttu-id="446ec-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="446ec-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="446ec-129">-EvictionPolicy</span></span>
<span data-ttu-id="446ec-130">Criterio di ridisposizione: il valore predefinito è VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="446ec-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-131">-Location</span><span class="sxs-lookup"><span data-stu-id="446ec-131">-Location</span></span>
<span data-ttu-id="446ec-132">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="446ec-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="446ec-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="446ec-134">La versione minima di TLS supportata dal cluster, ad esempio 1.2</span><span class="sxs-lookup"><span data-stu-id="446ec-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-135">-Module</span><span class="sxs-lookup"><span data-stu-id="446ec-135">-Module</span></span>
<span data-ttu-id="446ec-136">Set facoltativo di ridisposizione dei moduli da abilitare in questo database: i moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="446ec-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="446ec-137">Per creare, vedere la sezione NOTE per le proprietà MODULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="446ec-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="446ec-138">-NoWait</span></span>
<span data-ttu-id="446ec-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="446ec-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-140">-Porta</span><span class="sxs-lookup"><span data-stu-id="446ec-140">-Port</span></span>
<span data-ttu-id="446ec-141">Porta TCP dell'endpoint di database.</span><span class="sxs-lookup"><span data-stu-id="446ec-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="446ec-142">Specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="446ec-142">Specified at create time.</span></span>
<span data-ttu-id="446ec-143">L'impostazione predefinita è una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="446ec-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="446ec-144">-ResourceGroupName</span></span>
<span data-ttu-id="446ec-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="446ec-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="446ec-146">-Sku</span></span>
<span data-ttu-id="446ec-147">Il tipo di cluster RedisEnterprise da distribuire.</span><span class="sxs-lookup"><span data-stu-id="446ec-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="446ec-148">Valori possibili: (Enterprise_E10, EnterpriseFlash_F300 e così via)</span><span class="sxs-lookup"><span data-stu-id="446ec-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="446ec-149">-SubscriptionId</span></span>
<span data-ttu-id="446ec-150">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="446ec-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="446ec-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="446ec-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="446ec-152">-Tag</span></span>
<span data-ttu-id="446ec-153">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="446ec-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="446ec-154">-Zone</span></span>
<span data-ttu-id="446ec-155">Le aree in cui verrà distribuito il cluster.</span><span class="sxs-lookup"><span data-stu-id="446ec-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446ec-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="446ec-156">-Confirm</span></span>
<span data-ttu-id="446ec-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="446ec-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="446ec-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="446ec-158">-WhatIf</span></span>
<span data-ttu-id="446ec-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="446ec-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446ec-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="446ec-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="446ec-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446ec-161">CommonParameters</span></span>
<span data-ttu-id="446ec-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446ec-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446ec-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="446ec-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446ec-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="446ec-164">INPUTS</span></span>

## <span data-ttu-id="446ec-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="446ec-165">OUTPUTS</span></span>

### <span data-ttu-id="446ec-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="446ec-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="446ec-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="446ec-167">NOTES</span></span>

<span data-ttu-id="446ec-168">ALIAS</span><span class="sxs-lookup"><span data-stu-id="446ec-168">ALIASES</span></span>

<span data-ttu-id="446ec-169">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="446ec-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="446ec-170">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="446ec-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="446ec-171">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="446ec-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="446ec-172">MODULE <IModule[]>: set facoltativo di ridisposizione dei moduli da abilitare nel database. I moduli possono essere aggiunti solo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="446ec-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="446ec-173">`Name <String>`: il nome del modulo, ad esempio "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="446ec-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="446ec-174">`[Arg <String>]`: le opzioni di configurazione per il modulo, ad esempio "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="446ec-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="446ec-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="446ec-175">RELATED LINKS</span></span>

