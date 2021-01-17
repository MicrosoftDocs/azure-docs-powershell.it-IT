---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378223"
---
# <span data-ttu-id="80453-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="80453-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="80453-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80453-102">SYNOPSIS</span></span>
<span data-ttu-id="80453-103">Crea un cluster di cache Redis Enterpise e un database associato</span><span class="sxs-lookup"><span data-stu-id="80453-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="80453-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80453-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80453-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80453-105">DESCRIPTION</span></span>
<span data-ttu-id="80453-106">Crea o aggiorna un cluster di cache esistente (sovrascrivere/ricreare, con potenziale downtime) e un database associato denominato "default"</span><span class="sxs-lookup"><span data-stu-id="80453-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="80453-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80453-107">EXAMPLES</span></span>

### <span data-ttu-id="80453-108">Esempio 1: creare una cache aziendale di redis</span><span class="sxs-lookup"><span data-stu-id="80453-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="80453-109">Questo comando crea una cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="80453-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="80453-110">Esempio 2: creare una cache di redis Enterprise usando alcuni parametri facoltativi</span><span class="sxs-lookup"><span data-stu-id="80453-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="80453-111">Questo comando crea una cache di redis Enterprise denominata cache con alcuni parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="80453-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="80453-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80453-112">PARAMETERS</span></span>

### <span data-ttu-id="80453-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80453-113">-AsJob</span></span>
<span data-ttu-id="80453-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="80453-114">Run the command as a job</span></span>

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

### <span data-ttu-id="80453-115">-Capacità</span><span class="sxs-lookup"><span data-stu-id="80453-115">-Capacity</span></span>
<span data-ttu-id="80453-116">Dimensioni del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="80453-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="80453-117">I valori predefiniti sono 2 o 3 a seconda della SKU.</span><span class="sxs-lookup"><span data-stu-id="80453-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="80453-118">I valori validi sono (2, 4, 6,...) per gli SKU aziendali e (3, 9, 15,...) per le SKU Flash.</span><span class="sxs-lookup"><span data-stu-id="80453-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="80453-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="80453-119">-ClientProtocol</span></span>
<span data-ttu-id="80453-120">Specifica se i client Redis possono connettersi usando i protocolli di redis crittografati in TLS o in chiaro.</span><span class="sxs-lookup"><span data-stu-id="80453-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="80453-121">Il valore predefinito è TLS-crittografato.</span><span class="sxs-lookup"><span data-stu-id="80453-121">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="80453-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="80453-122">-ClusteringPolicy</span></span>
<span data-ttu-id="80453-123">Criteri di clustering: l'impostazione predefinita è OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="80453-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="80453-124">Specificato in Crea ora.</span><span class="sxs-lookup"><span data-stu-id="80453-124">Specified at create time.</span></span>

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

### <span data-ttu-id="80453-125">-Clustername</span><span class="sxs-lookup"><span data-stu-id="80453-125">-ClusterName</span></span>
<span data-ttu-id="80453-126">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="80453-126">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="80453-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80453-127">-DefaultProfile</span></span>
<span data-ttu-id="80453-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80453-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80453-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="80453-129">-EvictionPolicy</span></span>
<span data-ttu-id="80453-130">Criteri di eliminazione di redis-l'impostazione predefinita è VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="80453-130">Redis eviction policy - default is VolatileLRU.</span></span>

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

### <span data-ttu-id="80453-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="80453-131">-Location</span></span>
<span data-ttu-id="80453-132">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="80453-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="80453-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="80453-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="80453-134">Versione TLS minima per il cluster da supportare, ad esempio 1,2</span><span class="sxs-lookup"><span data-stu-id="80453-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

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

### <span data-ttu-id="80453-135">-Module</span><span class="sxs-lookup"><span data-stu-id="80453-135">-Module</span></span>
<span data-ttu-id="80453-136">Set facoltativo di moduli Redis per l'abilitazione in questo database-i moduli possono essere aggiunti solo in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="80453-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="80453-137">Per creare una tabella hash, vedere la sezione Note per le proprietà del modulo.</span><span class="sxs-lookup"><span data-stu-id="80453-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="80453-138">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="80453-138">-NoWait</span></span>
<span data-ttu-id="80453-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="80453-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80453-140">-Porta</span><span class="sxs-lookup"><span data-stu-id="80453-140">-Port</span></span>
<span data-ttu-id="80453-141">Porta TCP dell'endpoint di database.</span><span class="sxs-lookup"><span data-stu-id="80453-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="80453-142">Specificato in Crea ora.</span><span class="sxs-lookup"><span data-stu-id="80453-142">Specified at create time.</span></span>
<span data-ttu-id="80453-143">Impostazione predefinita per una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="80453-143">Defaults to an available port.</span></span>

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

### <span data-ttu-id="80453-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80453-144">-ResourceGroupName</span></span>
<span data-ttu-id="80453-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80453-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="80453-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="80453-146">-Sku</span></span>
<span data-ttu-id="80453-147">Tipo di cluster RedisEnterprise da distribuire.</span><span class="sxs-lookup"><span data-stu-id="80453-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="80453-148">Valori possibili: (Enterprise_E10, EnterpriseFlash_F300 e così via)</span><span class="sxs-lookup"><span data-stu-id="80453-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="80453-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80453-149">-SubscriptionId</span></span>
<span data-ttu-id="80453-150">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80453-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="80453-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="80453-151">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="80453-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="80453-152">-Tag</span></span>
<span data-ttu-id="80453-153">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="80453-153">Resource tags.</span></span>

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

### <span data-ttu-id="80453-154">-Zona</span><span class="sxs-lookup"><span data-stu-id="80453-154">-Zone</span></span>
<span data-ttu-id="80453-155">Aree in cui verrà distribuito il cluster.</span><span class="sxs-lookup"><span data-stu-id="80453-155">The zones where this cluster will be deployed.</span></span>

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

### <span data-ttu-id="80453-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80453-156">-Confirm</span></span>
<span data-ttu-id="80453-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80453-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80453-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80453-158">-WhatIf</span></span>
<span data-ttu-id="80453-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80453-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80453-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80453-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80453-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80453-161">CommonParameters</span></span>
<span data-ttu-id="80453-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80453-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80453-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80453-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80453-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80453-164">INPUTS</span></span>

## <span data-ttu-id="80453-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80453-165">OUTPUTS</span></span>

### <span data-ttu-id="80453-166">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="80453-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="80453-167">Note</span><span class="sxs-lookup"><span data-stu-id="80453-167">NOTES</span></span>

<span data-ttu-id="80453-168">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80453-168">ALIASES</span></span>

<span data-ttu-id="80453-169">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80453-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80453-170">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="80453-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80453-171">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80453-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80453-172">MODULE <IModule [] >: set facoltativo di moduli Redis per l'abilitazione in questo database-i moduli possono essere aggiunti solo in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="80453-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="80453-173">`Name <String>`: Nome del modulo, ad esempio "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="80453-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="80453-174">`[Arg <String>]`: Opzioni di configurazione per il modulo, ad esempio "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="80453-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="80453-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80453-175">RELATED LINKS</span></span>

