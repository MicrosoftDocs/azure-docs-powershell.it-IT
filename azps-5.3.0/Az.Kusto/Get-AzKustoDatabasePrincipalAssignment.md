---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474108"
---
# <span data-ttu-id="c5732-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c5732-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c5732-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5732-102">SYNOPSIS</span></span>
<span data-ttu-id="c5732-103">Ottiene un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c5732-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c5732-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5732-104">SYNTAX</span></span>

### <span data-ttu-id="c5732-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5732-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5732-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c5732-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5732-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5732-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5732-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5732-108">DESCRIPTION</span></span>
<span data-ttu-id="c5732-109">Ottiene un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c5732-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c5732-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5732-110">EXAMPLES</span></span>

### <span data-ttu-id="c5732-111">Esempio 1: elencare tutti i PrincipalAssignment in un database per nome</span><span class="sxs-lookup"><span data-stu-id="c5732-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c5732-112">Il comando precedente restituisce tutti tutti i PrincipalAssignment nel database "mykustodatabase" trovati nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c5732-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c5732-113">Esempio 2: ottenere un PrincipalAssignment specifico in un database per nome</span><span class="sxs-lookup"><span data-stu-id="c5732-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c5732-114">Il comando precedente restituisce tutti tutti i PrincipalAssignment denominati "kustoprincipal1" nel database "mykustodatabase" trovato nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c5732-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c5732-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5732-115">PARAMETERS</span></span>

### <span data-ttu-id="c5732-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c5732-116">-ClusterName</span></span>
<span data-ttu-id="c5732-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5732-118">-DatabaseName</span></span>
<span data-ttu-id="c5732-119">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5732-120">-DefaultProfile</span></span>
<span data-ttu-id="c5732-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5732-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5732-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5732-122">-InputObject</span></span>
<span data-ttu-id="c5732-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c5732-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c5732-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c5732-125">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5732-126">-ResourceGroupName</span></span>
<span data-ttu-id="c5732-127">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5732-128">-SubscriptionId</span></span>
<span data-ttu-id="c5732-129">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5732-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5732-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c5732-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5732-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5732-131">CommonParameters</span></span>
<span data-ttu-id="c5732-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5732-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5732-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5732-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5732-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5732-134">INPUTS</span></span>

### <span data-ttu-id="c5732-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c5732-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c5732-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5732-136">OUTPUTS</span></span>

### <span data-ttu-id="c5732-137">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c5732-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c5732-138">Note</span><span class="sxs-lookup"><span data-stu-id="c5732-138">NOTES</span></span>

<span data-ttu-id="c5732-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c5732-139">ALIASES</span></span>

<span data-ttu-id="c5732-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5732-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5732-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c5732-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5732-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c5732-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5732-143">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c5732-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5732-144">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="c5732-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c5732-145">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c5732-146">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="c5732-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c5732-147">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c5732-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c5732-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5732-149">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5732-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c5732-150">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c5732-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c5732-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c5732-152">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5732-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c5732-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c5732-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c5732-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5732-154">RELATED LINKS</span></span>

