---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191231"
---
# <span data-ttu-id="03724-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="03724-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="03724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03724-102">SYNOPSIS</span></span>
<span data-ttu-id="03724-103">Aggiorna un cluster RedisEnterprise esistente</span><span class="sxs-lookup"><span data-stu-id="03724-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="03724-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03724-104">SYNTAX</span></span>

### <span data-ttu-id="03724-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03724-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03724-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="03724-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03724-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03724-107">DESCRIPTION</span></span>
<span data-ttu-id="03724-108">Aggiorna un cluster RedisEnterprise esistente</span><span class="sxs-lookup"><span data-stu-id="03724-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="03724-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03724-109">EXAMPLES</span></span>

### <span data-ttu-id="03724-110">Esempio 1: Aggiornare la cache di Ridis Enterprise</span><span class="sxs-lookup"><span data-stu-id="03724-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="03724-111">Questo comando aggiorna la versione minima di TLS e aggiunge un tag alla cache dell'organizzazione di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="03724-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="03724-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03724-112">PARAMETERS</span></span>

### <span data-ttu-id="03724-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03724-113">-AsJob</span></span>
<span data-ttu-id="03724-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="03724-114">Run the command as a job</span></span>

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

### <span data-ttu-id="03724-115">-Capacità</span><span class="sxs-lookup"><span data-stu-id="03724-115">-Capacity</span></span>
<span data-ttu-id="03724-116">Dimensioni del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="03724-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="03724-117">Il valore predefinito è 2 o 3 a seconda dello SKU.</span><span class="sxs-lookup"><span data-stu-id="03724-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="03724-118">I valori validi sono (2, 4, 6, ...) per SKU Enterprise e (3, 9, 15, ...) per gli SKU Flash.</span><span class="sxs-lookup"><span data-stu-id="03724-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="03724-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="03724-119">-ClusterName</span></span>
<span data-ttu-id="03724-120">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="03724-120">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03724-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03724-121">-DefaultProfile</span></span>
<span data-ttu-id="03724-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03724-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03724-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03724-123">-InputObject</span></span>
<span data-ttu-id="03724-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="03724-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03724-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="03724-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="03724-126">La versione minima di TLS che il cluster deve supportare, ad esempio "1.2"</span><span class="sxs-lookup"><span data-stu-id="03724-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="03724-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03724-127">-NoWait</span></span>
<span data-ttu-id="03724-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="03724-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03724-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03724-129">-ResourceGroupName</span></span>
<span data-ttu-id="03724-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03724-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03724-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="03724-131">-Sku</span></span>
<span data-ttu-id="03724-132">Il tipo di cluster RedisEnterprise da distribuire.</span><span class="sxs-lookup"><span data-stu-id="03724-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="03724-133">Valori possibili: (Enterprise_E10, EnterpriseFlash_F300 e così via)</span><span class="sxs-lookup"><span data-stu-id="03724-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03724-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03724-134">-SubscriptionId</span></span>
<span data-ttu-id="03724-135">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03724-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="03724-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="03724-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03724-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="03724-137">-Tag</span></span>
<span data-ttu-id="03724-138">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="03724-138">Resource tags.</span></span>

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

### <span data-ttu-id="03724-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03724-139">-Confirm</span></span>
<span data-ttu-id="03724-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03724-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03724-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03724-141">-WhatIf</span></span>
<span data-ttu-id="03724-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03724-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03724-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03724-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03724-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03724-144">CommonParameters</span></span>
<span data-ttu-id="03724-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03724-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03724-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03724-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03724-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="03724-147">INPUTS</span></span>

### <span data-ttu-id="03724-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="03724-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="03724-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03724-149">OUTPUTS</span></span>

### <span data-ttu-id="03724-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="03724-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="03724-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="03724-151">NOTES</span></span>

<span data-ttu-id="03724-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="03724-152">ALIASES</span></span>

<span data-ttu-id="03724-153">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="03724-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03724-154">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="03724-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03724-155">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03724-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03724-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="03724-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03724-157">`[ClusterName <String>]`: nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="03724-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="03724-158">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="03724-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="03724-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="03724-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03724-160">`[Location <String>]`: l'area in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="03724-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="03724-161">`[OperationId <String>]`: l'identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="03724-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="03724-162">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="03724-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="03724-163">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03724-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="03724-164">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03724-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="03724-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="03724-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="03724-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03724-166">RELATED LINKS</span></span>

