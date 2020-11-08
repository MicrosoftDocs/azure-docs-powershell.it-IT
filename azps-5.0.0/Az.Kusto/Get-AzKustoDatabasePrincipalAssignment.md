---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202471"
---
# <span data-ttu-id="17fea-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="17fea-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="17fea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17fea-102">SYNOPSIS</span></span>
<span data-ttu-id="17fea-103">Ottiene un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="17fea-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="17fea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17fea-104">SYNTAX</span></span>

### <span data-ttu-id="17fea-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17fea-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17fea-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="17fea-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17fea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17fea-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="17fea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17fea-108">DESCRIPTION</span></span>
<span data-ttu-id="17fea-109">Ottiene un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="17fea-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="17fea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17fea-110">EXAMPLES</span></span>

### <span data-ttu-id="17fea-111">Esempio 1: elencare tutti i PrincipalAssignment in un database per nome</span><span class="sxs-lookup"><span data-stu-id="17fea-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="17fea-112">Il comando precedente restituisce tutti tutti i PrincipalAssignment nel database "mykustodatabase" trovati nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="17fea-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="17fea-113">Esempio 2: ottenere un PrincipalAssignment specifico in un database per nome</span><span class="sxs-lookup"><span data-stu-id="17fea-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="17fea-114">Il comando precedente restituisce tutti tutti i PrincipalAssignment denominati "kustoprincipal1" nel database "mykustodatabase" trovato nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="17fea-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="17fea-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17fea-115">PARAMETERS</span></span>

### <span data-ttu-id="17fea-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="17fea-116">-ClusterName</span></span>
<span data-ttu-id="17fea-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="17fea-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17fea-118">-DatabaseName</span></span>
<span data-ttu-id="17fea-119">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="17fea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fea-120">-DefaultProfile</span></span>
<span data-ttu-id="17fea-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17fea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17fea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17fea-122">-InputObject</span></span>
<span data-ttu-id="17fea-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="17fea-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17fea-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="17fea-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="17fea-125">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="17fea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fea-126">-ResourceGroupName</span></span>
<span data-ttu-id="17fea-127">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="17fea-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17fea-128">-SubscriptionId</span></span>
<span data-ttu-id="17fea-129">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17fea-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="17fea-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="17fea-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="17fea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fea-131">CommonParameters</span></span>
<span data-ttu-id="17fea-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fea-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17fea-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fea-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17fea-134">INPUTS</span></span>

### <span data-ttu-id="17fea-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="17fea-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="17fea-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17fea-136">OUTPUTS</span></span>

### <span data-ttu-id="17fea-137">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="17fea-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="17fea-138">Note</span><span class="sxs-lookup"><span data-stu-id="17fea-138">NOTES</span></span>

<span data-ttu-id="17fea-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="17fea-139">ALIASES</span></span>

<span data-ttu-id="17fea-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17fea-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17fea-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="17fea-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17fea-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17fea-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17fea-143">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="17fea-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17fea-144">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="17fea-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="17fea-145">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="17fea-146">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="17fea-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="17fea-147">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="17fea-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="17fea-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17fea-149">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="17fea-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="17fea-150">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="17fea-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="17fea-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="17fea-152">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17fea-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="17fea-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="17fea-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="17fea-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17fea-154">RELATED LINKS</span></span>

