---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: f410ba5dc89f29c3a928ed459be87769bf5ffca7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960717"
---
# <span data-ttu-id="a240f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="a240f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="a240f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a240f-102">SYNOPSIS</span></span>
<span data-ttu-id="a240f-103">Scollega tutti i follower di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="a240f-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="a240f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a240f-104">SYNTAX</span></span>

### <span data-ttu-id="a240f-105">DetachExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a240f-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a240f-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a240f-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a240f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a240f-107">DESCRIPTION</span></span>
<span data-ttu-id="a240f-108">Scollega tutti i follower di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="a240f-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="a240f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a240f-109">EXAMPLES</span></span>

### <span data-ttu-id="a240f-110">Esempio 1: Scollegare un database di follower</span><span class="sxs-lookup"><span data-stu-id="a240f-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="a240f-111">Il comando precedente scollega il database di follower definito in AttachedDatabaseConfiguration "myfollowerconfiguration" dal cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="a240f-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="a240f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a240f-112">PARAMETERS</span></span>

### <span data-ttu-id="a240f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a240f-113">-AsJob</span></span>
<span data-ttu-id="a240f-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a240f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a240f-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a240f-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="a240f-116">Nome della risorsa della configurazione di database collegata nel cluster follower.</span><span class="sxs-lookup"><span data-stu-id="a240f-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="a240f-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a240f-117">-ClusterName</span></span>
<span data-ttu-id="a240f-118">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a240f-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a240f-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="a240f-119">-ClusterResourceId</span></span>
<span data-ttu-id="a240f-120">ID risorsa del cluster che segue un database di proprietà del cluster.</span><span class="sxs-lookup"><span data-stu-id="a240f-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="a240f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a240f-121">-DefaultProfile</span></span>
<span data-ttu-id="a240f-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a240f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a240f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a240f-123">-InputObject</span></span>
<span data-ttu-id="a240f-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a240f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a240f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a240f-125">-NoWait</span></span>
<span data-ttu-id="a240f-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a240f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a240f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a240f-127">-PassThru</span></span>
<span data-ttu-id="a240f-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="a240f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a240f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a240f-129">-ResourceGroupName</span></span>
<span data-ttu-id="a240f-130">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a240f-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a240f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a240f-131">-SubscriptionId</span></span>
<span data-ttu-id="a240f-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a240f-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a240f-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a240f-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a240f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a240f-134">-Confirm</span></span>
<span data-ttu-id="a240f-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a240f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a240f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a240f-136">-WhatIf</span></span>
<span data-ttu-id="a240f-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a240f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a240f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a240f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a240f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a240f-139">CommonParameters</span></span>
<span data-ttu-id="a240f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a240f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a240f-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a240f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a240f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="a240f-142">INPUTS</span></span>

### <span data-ttu-id="a240f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a240f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a240f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a240f-144">OUTPUTS</span></span>

### <span data-ttu-id="a240f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a240f-145">System.Boolean</span></span>

## <span data-ttu-id="a240f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="a240f-146">NOTES</span></span>

<span data-ttu-id="a240f-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a240f-147">ALIASES</span></span>

<span data-ttu-id="a240f-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a240f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a240f-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a240f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a240f-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a240f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a240f-151">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a240f-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a240f-152">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="a240f-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a240f-153">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a240f-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a240f-154">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="a240f-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a240f-155">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a240f-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a240f-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a240f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a240f-157">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a240f-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a240f-158">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a240f-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a240f-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a240f-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a240f-160">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a240f-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a240f-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a240f-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a240f-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a240f-162">RELATED LINKS</span></span>

