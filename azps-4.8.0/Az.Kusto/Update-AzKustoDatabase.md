---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192455"
---
# <span data-ttu-id="223cb-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="223cb-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="223cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="223cb-102">SYNOPSIS</span></span>
<span data-ttu-id="223cb-103">Aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="223cb-103">Updates a database.</span></span>

## <span data-ttu-id="223cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="223cb-104">SYNTAX</span></span>

### <span data-ttu-id="223cb-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="223cb-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="223cb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="223cb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="223cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="223cb-107">DESCRIPTION</span></span>
<span data-ttu-id="223cb-108">Aggiorna un database.</span><span class="sxs-lookup"><span data-stu-id="223cb-108">Updates a database.</span></span>

## <span data-ttu-id="223cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="223cb-109">EXAMPLES</span></span>

### <span data-ttu-id="223cb-110">Esempio 1: aggiornare un database esistente per nome</span><span class="sxs-lookup"><span data-stu-id="223cb-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="223cb-111">Il comando precedente aggiorna il periodo di eliminazione morbida e la cache calda del database kusto "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="223cb-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="223cb-112">Esempio 2: aggiornare un database esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="223cb-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="223cb-113">Il comando precedente aggiorna il periodo di eliminazione morbida e la cache calda del database kusto "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="223cb-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="223cb-114">Esempio 3: aggiornare un database ReadOnly esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="223cb-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="223cb-115">Il comando precedente aggiorna il periodo di cache caldo del database kusto "mykustodatabase" nel cluster "myfollowercluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="223cb-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="223cb-116">Esempio 4: aggiornare un database ReadOnly esistente tramite l'identità</span><span class="sxs-lookup"><span data-stu-id="223cb-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="223cb-117">Il comando precedente aggiorna il periodo di cache caldo del database kusto "mykustodatabase" nel cluster "myfollowercluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="223cb-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="223cb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="223cb-118">PARAMETERS</span></span>

### <span data-ttu-id="223cb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="223cb-119">-AsJob</span></span>
<span data-ttu-id="223cb-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="223cb-120">Run the command as a job</span></span>

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

### <span data-ttu-id="223cb-121">-Clustername</span><span class="sxs-lookup"><span data-stu-id="223cb-121">-ClusterName</span></span>
<span data-ttu-id="223cb-122">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="223cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223cb-123">-DefaultProfile</span></span>
<span data-ttu-id="223cb-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="223cb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="223cb-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="223cb-125">-HotCachePeriod</span></span>
<span data-ttu-id="223cb-126">Data e ora in cui i dati devono essere conservati nella cache per le query veloci in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="223cb-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="223cb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="223cb-127">-InputObject</span></span>
<span data-ttu-id="223cb-128">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="223cb-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="223cb-129">-Tipo</span><span class="sxs-lookup"><span data-stu-id="223cb-129">-Kind</span></span>
<span data-ttu-id="223cb-130">Tipo di database</span><span class="sxs-lookup"><span data-stu-id="223cb-130">Kind of the database</span></span>

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

### <span data-ttu-id="223cb-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="223cb-131">-Location</span></span>
<span data-ttu-id="223cb-132">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="223cb-132">Resource location.</span></span>

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

### <span data-ttu-id="223cb-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="223cb-133">-Name</span></span>
<span data-ttu-id="223cb-134">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="223cb-135">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="223cb-135">-NoWait</span></span>
<span data-ttu-id="223cb-136">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="223cb-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="223cb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="223cb-137">-ResourceGroupName</span></span>
<span data-ttu-id="223cb-138">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="223cb-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="223cb-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="223cb-140">Il tempo di permanenza dei dati prima che venga impedito l'accessibilità alle query in TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="223cb-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="223cb-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="223cb-141">-SubscriptionId</span></span>
<span data-ttu-id="223cb-142">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="223cb-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="223cb-143">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="223cb-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="223cb-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="223cb-144">-Confirm</span></span>
<span data-ttu-id="223cb-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="223cb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="223cb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="223cb-146">-WhatIf</span></span>
<span data-ttu-id="223cb-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="223cb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="223cb-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="223cb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="223cb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223cb-149">CommonParameters</span></span>
<span data-ttu-id="223cb-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223cb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223cb-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="223cb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223cb-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="223cb-152">INPUTS</span></span>

### <span data-ttu-id="223cb-153">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="223cb-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="223cb-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="223cb-154">OUTPUTS</span></span>

### <span data-ttu-id="223cb-155">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="223cb-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="223cb-156">Note</span><span class="sxs-lookup"><span data-stu-id="223cb-156">NOTES</span></span>

<span data-ttu-id="223cb-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="223cb-157">ALIASES</span></span>

<span data-ttu-id="223cb-158">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="223cb-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="223cb-159">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="223cb-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="223cb-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="223cb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="223cb-161">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="223cb-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="223cb-162">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="223cb-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="223cb-163">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="223cb-164">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="223cb-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="223cb-165">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="223cb-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="223cb-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="223cb-167">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="223cb-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="223cb-168">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="223cb-169">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="223cb-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="223cb-170">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="223cb-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="223cb-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="223cb-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="223cb-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="223cb-172">RELATED LINKS</span></span>
