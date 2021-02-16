---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209267"
---
# <span data-ttu-id="3c0be-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="3c0be-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="3c0be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0be-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0be-103">Scollega tutti i follower di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="3c0be-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="3c0be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c0be-104">SYNTAX</span></span>

### <span data-ttu-id="3c0be-105">DetachExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c0be-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c0be-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3c0be-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c0be-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c0be-107">DESCRIPTION</span></span>
<span data-ttu-id="3c0be-108">Scollega tutti i follower di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="3c0be-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="3c0be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c0be-109">EXAMPLES</span></span>

### <span data-ttu-id="3c0be-110">Esempio 1: Scollegare un database di follower</span><span class="sxs-lookup"><span data-stu-id="3c0be-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="3c0be-111">Il comando precedente scollega il database di follower definito in AttachedDatabaseConfiguration "myfollowerconfiguration" dal cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="3c0be-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="3c0be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c0be-112">PARAMETERS</span></span>

### <span data-ttu-id="3c0be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c0be-113">-AsJob</span></span>
<span data-ttu-id="3c0be-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3c0be-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3c0be-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3c0be-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="3c0be-116">Nome della risorsa della configurazione di database collegata nel cluster follower.</span><span class="sxs-lookup"><span data-stu-id="3c0be-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="3c0be-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3c0be-117">-ClusterName</span></span>
<span data-ttu-id="3c0be-118">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c0be-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c0be-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="3c0be-119">-ClusterResourceId</span></span>
<span data-ttu-id="3c0be-120">ID risorsa del cluster che segue un database di proprietà del cluster.</span><span class="sxs-lookup"><span data-stu-id="3c0be-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="3c0be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0be-121">-DefaultProfile</span></span>
<span data-ttu-id="3c0be-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0be-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c0be-123">-InputObject</span></span>
<span data-ttu-id="3c0be-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3c0be-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c0be-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c0be-125">-NoWait</span></span>
<span data-ttu-id="3c0be-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3c0be-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c0be-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c0be-127">-PassThru</span></span>
<span data-ttu-id="3c0be-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="3c0be-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c0be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0be-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c0be-130">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c0be-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c0be-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c0be-131">-SubscriptionId</span></span>
<span data-ttu-id="3c0be-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0be-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c0be-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c0be-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c0be-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c0be-134">-Confirm</span></span>
<span data-ttu-id="3c0be-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c0be-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0be-136">-WhatIf</span></span>
<span data-ttu-id="3c0be-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c0be-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c0be-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c0be-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0be-139">CommonParameters</span></span>
<span data-ttu-id="3c0be-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0be-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c0be-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0be-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c0be-142">INPUTS</span></span>

### <span data-ttu-id="3c0be-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3c0be-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3c0be-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c0be-144">OUTPUTS</span></span>

### <span data-ttu-id="3c0be-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c0be-145">System.Boolean</span></span>

## <span data-ttu-id="3c0be-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c0be-146">NOTES</span></span>

<span data-ttu-id="3c0be-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3c0be-147">ALIASES</span></span>

<span data-ttu-id="3c0be-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3c0be-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c0be-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3c0be-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c0be-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c0be-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c0be-151">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="3c0be-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c0be-152">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="3c0be-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3c0be-153">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c0be-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3c0be-154">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="3c0be-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3c0be-155">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c0be-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3c0be-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3c0be-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c0be-157">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0be-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3c0be-158">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3c0be-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3c0be-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c0be-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3c0be-160">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0be-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c0be-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3c0be-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3c0be-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c0be-162">RELATED LINKS</span></span>

