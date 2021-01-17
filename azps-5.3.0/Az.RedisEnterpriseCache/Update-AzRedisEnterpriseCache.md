---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378167"
---
# <span data-ttu-id="d6d26-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="d6d26-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="d6d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6d26-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d26-103">Aggiorna un cluster di RedisEnterprise esistente</span><span class="sxs-lookup"><span data-stu-id="d6d26-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="d6d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6d26-104">SYNTAX</span></span>

### <span data-ttu-id="d6d26-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6d26-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6d26-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d6d26-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6d26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6d26-107">DESCRIPTION</span></span>
<span data-ttu-id="d6d26-108">Aggiorna un cluster di RedisEnterprise esistente</span><span class="sxs-lookup"><span data-stu-id="d6d26-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="d6d26-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6d26-109">EXAMPLES</span></span>

### <span data-ttu-id="d6d26-110">Esempio 1: aggiornare la cache di redis Enterprise</span><span class="sxs-lookup"><span data-stu-id="d6d26-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="d6d26-111">Questo comando Aggiorna la versione minima di TLS e aggiunge un contrassegno alla cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="d6d26-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d6d26-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6d26-112">PARAMETERS</span></span>

### <span data-ttu-id="d6d26-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6d26-113">-AsJob</span></span>
<span data-ttu-id="d6d26-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d6d26-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d6d26-115">-Capacità</span><span class="sxs-lookup"><span data-stu-id="d6d26-115">-Capacity</span></span>
<span data-ttu-id="d6d26-116">Dimensioni del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d6d26-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="d6d26-117">I valori predefiniti sono 2 o 3 a seconda della SKU.</span><span class="sxs-lookup"><span data-stu-id="d6d26-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="d6d26-118">I valori validi sono (2, 4, 6,...) per gli SKU aziendali e (3, 9, 15,...) per le SKU Flash.</span><span class="sxs-lookup"><span data-stu-id="d6d26-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="d6d26-119">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d6d26-119">-ClusterName</span></span>
<span data-ttu-id="d6d26-120">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d6d26-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="d6d26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d26-121">-DefaultProfile</span></span>
<span data-ttu-id="d6d26-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d26-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d26-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d26-123">-InputObject</span></span>
<span data-ttu-id="d6d26-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d6d26-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6d26-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d6d26-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="d6d26-126">Versione TLS minima per il cluster da supportare, ad esempio "1,2"</span><span class="sxs-lookup"><span data-stu-id="d6d26-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="d6d26-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d6d26-127">-NoWait</span></span>
<span data-ttu-id="d6d26-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d6d26-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6d26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6d26-129">-ResourceGroupName</span></span>
<span data-ttu-id="d6d26-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6d26-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6d26-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="d6d26-131">-Sku</span></span>
<span data-ttu-id="d6d26-132">Tipo di cluster RedisEnterprise da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d6d26-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="d6d26-133">Valori possibili: (Enterprise_E10, EnterpriseFlash_F300 e così via)</span><span class="sxs-lookup"><span data-stu-id="d6d26-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="d6d26-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6d26-134">-SubscriptionId</span></span>
<span data-ttu-id="d6d26-135">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d26-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6d26-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d6d26-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6d26-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6d26-137">-Tag</span></span>
<span data-ttu-id="d6d26-138">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d6d26-138">Resource tags.</span></span>

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

### <span data-ttu-id="d6d26-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6d26-139">-Confirm</span></span>
<span data-ttu-id="d6d26-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6d26-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d26-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d26-141">-WhatIf</span></span>
<span data-ttu-id="d6d26-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6d26-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d26-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6d26-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d26-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d26-144">CommonParameters</span></span>
<span data-ttu-id="d6d26-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d26-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d26-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6d26-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d26-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6d26-147">INPUTS</span></span>

### <span data-ttu-id="d6d26-148">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="d6d26-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="d6d26-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6d26-149">OUTPUTS</span></span>

### <span data-ttu-id="d6d26-150">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="d6d26-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="d6d26-151">Note</span><span class="sxs-lookup"><span data-stu-id="d6d26-151">NOTES</span></span>

<span data-ttu-id="d6d26-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d6d26-152">ALIASES</span></span>

<span data-ttu-id="d6d26-153">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6d26-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6d26-154">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d6d26-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6d26-155">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6d26-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6d26-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d6d26-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6d26-157">`[ClusterName <String>]`: Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d6d26-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="d6d26-158">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d6d26-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d6d26-159">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d6d26-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6d26-160">`[Location <String>]`: L'area geografica in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6d26-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="d6d26-161">`[OperationId <String>]`: Identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6d26-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="d6d26-162">`[PrivateEndpointConnectionName <String>]`: Nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="d6d26-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="d6d26-163">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6d26-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d6d26-164">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d26-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d6d26-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d6d26-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6d26-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6d26-166">RELATED LINKS</span></span>

