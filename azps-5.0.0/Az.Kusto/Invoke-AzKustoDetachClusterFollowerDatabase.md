---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202463"
---
# <span data-ttu-id="421a0-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="421a0-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="421a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="421a0-102">SYNOPSIS</span></span>
<span data-ttu-id="421a0-103">Disconnette tutti i seguaci di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="421a0-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="421a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="421a0-104">SYNTAX</span></span>

### <span data-ttu-id="421a0-105">DetachExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="421a0-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="421a0-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="421a0-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="421a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="421a0-107">DESCRIPTION</span></span>
<span data-ttu-id="421a0-108">Disconnette tutti i seguaci di un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="421a0-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="421a0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="421a0-109">EXAMPLES</span></span>

### <span data-ttu-id="421a0-110">Esempio 1: scollegare un database di follower</span><span class="sxs-lookup"><span data-stu-id="421a0-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="421a0-111">Il comando precedente disconnette il database di follower definito in AttachedDatabaseConfiguration "myfollowerconfiguration" dal cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="421a0-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="421a0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="421a0-112">PARAMETERS</span></span>

### <span data-ttu-id="421a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="421a0-113">-AsJob</span></span>
<span data-ttu-id="421a0-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="421a0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="421a0-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="421a0-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="421a0-116">Nome risorsa della configurazione del database allegato nel cluster di follower.</span><span class="sxs-lookup"><span data-stu-id="421a0-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="421a0-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="421a0-117">-ClusterName</span></span>
<span data-ttu-id="421a0-118">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="421a0-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="421a0-119">-ClusterResourceId</span></span>
<span data-ttu-id="421a0-120">ID risorsa del cluster che segue un database di proprietà di questo cluster.</span><span class="sxs-lookup"><span data-stu-id="421a0-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="421a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421a0-121">-DefaultProfile</span></span>
<span data-ttu-id="421a0-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="421a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421a0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="421a0-123">-InputObject</span></span>
<span data-ttu-id="421a0-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="421a0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="421a0-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="421a0-125">-NoWait</span></span>
<span data-ttu-id="421a0-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="421a0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="421a0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="421a0-127">-PassThru</span></span>
<span data-ttu-id="421a0-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="421a0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="421a0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="421a0-129">-ResourceGroupName</span></span>
<span data-ttu-id="421a0-130">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="421a0-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="421a0-131">-SubscriptionId</span></span>
<span data-ttu-id="421a0-132">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="421a0-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="421a0-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="421a0-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="421a0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="421a0-134">-Confirm</span></span>
<span data-ttu-id="421a0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="421a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="421a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421a0-136">-WhatIf</span></span>
<span data-ttu-id="421a0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="421a0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="421a0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="421a0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="421a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421a0-139">CommonParameters</span></span>
<span data-ttu-id="421a0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421a0-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="421a0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421a0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="421a0-142">INPUTS</span></span>

### <span data-ttu-id="421a0-143">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="421a0-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="421a0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="421a0-144">OUTPUTS</span></span>

### <span data-ttu-id="421a0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="421a0-145">System.Boolean</span></span>

## <span data-ttu-id="421a0-146">Note</span><span class="sxs-lookup"><span data-stu-id="421a0-146">NOTES</span></span>

<span data-ttu-id="421a0-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="421a0-147">ALIASES</span></span>

<span data-ttu-id="421a0-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="421a0-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="421a0-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="421a0-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="421a0-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="421a0-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="421a0-151">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="421a0-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="421a0-152">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="421a0-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="421a0-153">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="421a0-154">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="421a0-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="421a0-155">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="421a0-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="421a0-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="421a0-157">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="421a0-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="421a0-158">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="421a0-159">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="421a0-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="421a0-160">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="421a0-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="421a0-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="421a0-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="421a0-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="421a0-162">RELATED LINKS</span></span>

