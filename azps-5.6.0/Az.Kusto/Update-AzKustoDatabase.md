---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 76e712a881c88490a71933056f82fe1959df2948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955838"
---
# <span data-ttu-id="cc44c-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="cc44c-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="cc44c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc44c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc44c-103">Aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="cc44c-103">Updates a database.</span></span>

## <span data-ttu-id="cc44c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc44c-104">SYNTAX</span></span>

### <span data-ttu-id="cc44c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc44c-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc44c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cc44c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc44c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc44c-107">DESCRIPTION</span></span>
<span data-ttu-id="cc44c-108">Aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="cc44c-108">Updates a database.</span></span>

## <span data-ttu-id="cc44c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc44c-109">EXAMPLES</span></span>

### <span data-ttu-id="cc44c-110">Esempio 1: Aggiornare un database esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="cc44c-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="cc44c-111">Il comando precedente aggiorna il periodo di eliminazione soft e il periodo di cache a scelta rapida del database Kusto "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="cc44c-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="cc44c-112">Esempio 2: Aggiornare un database esistente con l'identità</span><span class="sxs-lookup"><span data-stu-id="cc44c-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="cc44c-113">Il comando precedente aggiorna il periodo di eliminazione soft e il periodo di cache a scelta rapida del database Kusto "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="cc44c-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="cc44c-114">Esempio 3: Aggiornare un database ReadOnly esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="cc44c-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="cc44c-115">Il comando precedente aggiorna il periodo di cache a scelta rapida del database Kusto "mykustodatabase" nel cluster "myfollowercluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="cc44c-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="cc44c-116">Esempio 4: Aggiornare un database ReadOnly esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="cc44c-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="cc44c-117">Il comando precedente aggiorna il periodo di cache a scelta rapida del database Kusto "mykustodatabase" nel cluster "myfollowercluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="cc44c-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="cc44c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc44c-118">PARAMETERS</span></span>

### <span data-ttu-id="cc44c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc44c-119">-AsJob</span></span>
<span data-ttu-id="cc44c-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cc44c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="cc44c-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cc44c-121">-ClusterName</span></span>
<span data-ttu-id="cc44c-122">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cc44c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc44c-123">-DefaultProfile</span></span>
<span data-ttu-id="cc44c-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc44c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc44c-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="cc44c-125">-HotCachePeriod</span></span>
<span data-ttu-id="cc44c-126">Ora in cui i dati devono essere mantenuti nella cache per le query veloci in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="cc44c-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc44c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc44c-127">-InputObject</span></span>
<span data-ttu-id="cc44c-128">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cc44c-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc44c-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="cc44c-129">-Kind</span></span>
<span data-ttu-id="cc44c-130">Tipo di database</span><span class="sxs-lookup"><span data-stu-id="cc44c-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc44c-131">-Location</span><span class="sxs-lookup"><span data-stu-id="cc44c-131">-Location</span></span>
<span data-ttu-id="cc44c-132">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cc44c-132">Resource location.</span></span>

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

### <span data-ttu-id="cc44c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="cc44c-133">-Name</span></span>
<span data-ttu-id="cc44c-134">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc44c-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc44c-135">-NoWait</span></span>
<span data-ttu-id="cc44c-136">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cc44c-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc44c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc44c-137">-ResourceGroupName</span></span>
<span data-ttu-id="cc44c-138">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cc44c-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="cc44c-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="cc44c-140">Il tempo che i dati devono mantenere prima di non essere più accessibili alle query nell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="cc44c-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc44c-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc44c-141">-SubscriptionId</span></span>
<span data-ttu-id="cc44c-142">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc44c-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc44c-143">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cc44c-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cc44c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc44c-144">-Confirm</span></span>
<span data-ttu-id="cc44c-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc44c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc44c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc44c-146">-WhatIf</span></span>
<span data-ttu-id="cc44c-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc44c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc44c-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc44c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc44c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc44c-149">CommonParameters</span></span>
<span data-ttu-id="cc44c-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc44c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc44c-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc44c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc44c-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc44c-152">INPUTS</span></span>

### <span data-ttu-id="cc44c-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cc44c-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cc44c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc44c-154">OUTPUTS</span></span>

### <span data-ttu-id="cc44c-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="cc44c-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="cc44c-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc44c-156">NOTES</span></span>

<span data-ttu-id="cc44c-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc44c-157">ALIASES</span></span>

<span data-ttu-id="cc44c-158">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cc44c-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc44c-159">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cc44c-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc44c-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc44c-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc44c-161">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cc44c-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc44c-162">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="cc44c-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cc44c-163">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cc44c-164">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="cc44c-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cc44c-165">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cc44c-166">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cc44c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc44c-167">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cc44c-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cc44c-168">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cc44c-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cc44c-169">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cc44c-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cc44c-170">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc44c-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cc44c-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cc44c-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cc44c-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc44c-172">RELATED LINKS</span></span>

