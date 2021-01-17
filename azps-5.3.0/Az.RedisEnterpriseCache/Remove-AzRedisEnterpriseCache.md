---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378181"
---
# <span data-ttu-id="e38d6-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="e38d6-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="e38d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e38d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e38d6-103">Elimina un cluster di cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="e38d6-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="e38d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e38d6-104">SYNTAX</span></span>

### <span data-ttu-id="e38d6-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e38d6-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e38d6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e38d6-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e38d6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e38d6-107">DESCRIPTION</span></span>
<span data-ttu-id="e38d6-108">Elimina un cluster di cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="e38d6-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="e38d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e38d6-109">EXAMPLES</span></span>

### <span data-ttu-id="e38d6-110">Esempio 1: rimuovere una cache di redis Enterprise e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="e38d6-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="e38d6-111">Questo comando rimuove una cache di redis Enterprise e visualizza se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e38d6-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="e38d6-112">Esempio 2: rimuovere una cache di redis Enterprise e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="e38d6-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="e38d6-113">Questo comando rimuove una cache di redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e38d6-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="e38d6-114">Poiché il parametro PassThru non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e38d6-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="e38d6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e38d6-115">PARAMETERS</span></span>

### <span data-ttu-id="e38d6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e38d6-116">-AsJob</span></span>
<span data-ttu-id="e38d6-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e38d6-117">Run the command as a job</span></span>

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

### <span data-ttu-id="e38d6-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e38d6-118">-ClusterName</span></span>
<span data-ttu-id="e38d6-119">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="e38d6-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38d6-120">-DefaultProfile</span></span>
<span data-ttu-id="e38d6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e38d6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38d6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e38d6-122">-InputObject</span></span>
<span data-ttu-id="e38d6-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e38d6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38d6-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e38d6-124">-NoWait</span></span>
<span data-ttu-id="e38d6-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e38d6-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e38d6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e38d6-126">-PassThru</span></span>
<span data-ttu-id="e38d6-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e38d6-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e38d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="e38d6-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e38d6-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38d6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e38d6-130">-SubscriptionId</span></span>
<span data-ttu-id="e38d6-131">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e38d6-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e38d6-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e38d6-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38d6-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e38d6-133">-Confirm</span></span>
<span data-ttu-id="e38d6-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38d6-135">-WhatIf</span></span>
<span data-ttu-id="e38d6-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e38d6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38d6-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e38d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38d6-138">CommonParameters</span></span>
<span data-ttu-id="e38d6-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38d6-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e38d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38d6-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e38d6-141">INPUTS</span></span>

### <span data-ttu-id="e38d6-142">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="e38d6-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="e38d6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e38d6-143">OUTPUTS</span></span>

### <span data-ttu-id="e38d6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e38d6-144">System.Boolean</span></span>

## <span data-ttu-id="e38d6-145">Note</span><span class="sxs-lookup"><span data-stu-id="e38d6-145">NOTES</span></span>

<span data-ttu-id="e38d6-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e38d6-146">ALIASES</span></span>

<span data-ttu-id="e38d6-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e38d6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e38d6-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e38d6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e38d6-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e38d6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e38d6-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e38d6-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e38d6-151">`[ClusterName <String>]`: Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="e38d6-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="e38d6-152">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="e38d6-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e38d6-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e38d6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e38d6-154">`[Location <String>]`: L'area geografica in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e38d6-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="e38d6-155">`[OperationId <String>]`: Identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e38d6-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="e38d6-156">`[PrivateEndpointConnectionName <String>]`: Nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="e38d6-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="e38d6-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e38d6-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e38d6-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e38d6-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e38d6-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e38d6-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e38d6-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e38d6-160">RELATED LINKS</span></span>

