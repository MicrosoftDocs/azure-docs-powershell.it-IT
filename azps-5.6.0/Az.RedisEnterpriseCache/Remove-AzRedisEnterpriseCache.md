---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000734"
---
# <span data-ttu-id="cfc82-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="cfc82-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="cfc82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfc82-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc82-103">Elimina un cluster di cache di RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cfc82-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="cfc82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfc82-104">SYNTAX</span></span>

### <span data-ttu-id="cfc82-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfc82-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cfc82-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cfc82-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cfc82-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfc82-107">DESCRIPTION</span></span>
<span data-ttu-id="cfc82-108">Elimina un cluster di cache di RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cfc82-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="cfc82-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfc82-109">EXAMPLES</span></span>

### <span data-ttu-id="cfc82-110">Esempio 1: Rimuovere una cache aziendale di Redis e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="cfc82-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="cfc82-111">Questo comando rimuove una cache dell'organizzazione di Redis e indica se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="cfc82-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="cfc82-112">Esempio 2: Rimuovere una cache aziendale di Redis e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="cfc82-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="cfc82-113">Questo comando rimuove una cache aziendale di Redis.</span><span class="sxs-lookup"><span data-stu-id="cfc82-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="cfc82-114">Poiché il parametro PassThru non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="cfc82-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="cfc82-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfc82-115">PARAMETERS</span></span>

### <span data-ttu-id="cfc82-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfc82-116">-AsJob</span></span>
<span data-ttu-id="cfc82-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cfc82-117">Run the command as a job</span></span>

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

### <span data-ttu-id="cfc82-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cfc82-118">-ClusterName</span></span>
<span data-ttu-id="cfc82-119">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cfc82-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="cfc82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc82-120">-DefaultProfile</span></span>
<span data-ttu-id="cfc82-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc82-122">-InputObject</span></span>
<span data-ttu-id="cfc82-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cfc82-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cfc82-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cfc82-124">-NoWait</span></span>
<span data-ttu-id="cfc82-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cfc82-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cfc82-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfc82-126">-PassThru</span></span>
<span data-ttu-id="cfc82-127">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="cfc82-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cfc82-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc82-128">-ResourceGroupName</span></span>
<span data-ttu-id="cfc82-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfc82-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="cfc82-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cfc82-130">-SubscriptionId</span></span>
<span data-ttu-id="cfc82-131">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc82-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cfc82-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cfc82-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cfc82-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfc82-133">-Confirm</span></span>
<span data-ttu-id="cfc82-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc82-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc82-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc82-135">-WhatIf</span></span>
<span data-ttu-id="cfc82-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfc82-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfc82-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfc82-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc82-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc82-138">CommonParameters</span></span>
<span data-ttu-id="cfc82-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc82-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc82-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cfc82-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc82-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfc82-141">INPUTS</span></span>

### <span data-ttu-id="cfc82-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="cfc82-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="cfc82-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfc82-143">OUTPUTS</span></span>

### <span data-ttu-id="cfc82-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cfc82-144">System.Boolean</span></span>

## <span data-ttu-id="cfc82-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfc82-145">NOTES</span></span>

<span data-ttu-id="cfc82-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cfc82-146">ALIASES</span></span>

<span data-ttu-id="cfc82-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cfc82-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cfc82-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cfc82-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cfc82-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cfc82-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cfc82-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cfc82-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cfc82-151">`[ClusterName <String>]`: nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="cfc82-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="cfc82-152">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="cfc82-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cfc82-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cfc82-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cfc82-154">`[Location <String>]`: l'area in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cfc82-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="cfc82-155">`[OperationId <String>]`: l'identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cfc82-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="cfc82-156">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato associata alla risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="cfc82-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="cfc82-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfc82-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cfc82-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc82-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cfc82-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cfc82-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cfc82-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfc82-160">RELATED LINKS</span></span>

