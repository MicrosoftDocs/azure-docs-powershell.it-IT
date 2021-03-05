---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986802"
---
# <span data-ttu-id="0f3e6-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0f3e6-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0f3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3e6-103">Ottiene un principalAssignment del database cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0f3e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f3e6-104">SYNTAX</span></span>

### <span data-ttu-id="0f3e6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f3e6-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f3e6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0f3e6-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f3e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f3e6-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f3e6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f3e6-108">DESCRIPTION</span></span>
<span data-ttu-id="0f3e6-109">Ottiene un principalAssignment del database cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0f3e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f3e6-110">EXAMPLES</span></span>

### <span data-ttu-id="0f3e6-111">Esempio 1: Elencare tutte le principalAssignment in un database in base al nome</span><span class="sxs-lookup"><span data-stu-id="0f3e6-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="0f3e6-112">Il comando precedente restituisce tutti gli elementi PrincipalAssignment del database "mykustodatabase" trovati nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0f3e6-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="0f3e6-113">Esempio 2: Ottenere un'assegnazione principale specifica in un database in base al nome</span><span class="sxs-lookup"><span data-stu-id="0f3e6-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="0f3e6-114">Il comando precedente restituisce tutto il principalAssignment denominato "kustoprincipal1" nel database "mykustodatabase" trovato nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0f3e6-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="0f3e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f3e6-115">PARAMETERS</span></span>

### <span data-ttu-id="0f3e6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0f3e6-116">-ClusterName</span></span>
<span data-ttu-id="0f3e6-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0f3e6-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f3e6-118">-DatabaseName</span></span>
<span data-ttu-id="0f3e6-119">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0f3e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3e6-120">-DefaultProfile</span></span>
<span data-ttu-id="0f3e6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f3e6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f3e6-122">-InputObject</span></span>
<span data-ttu-id="0f3e6-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f3e6-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0f3e6-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0f3e6-125">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0f3e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="0f3e6-127">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0f3e6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f3e6-128">-SubscriptionId</span></span>
<span data-ttu-id="0f3e6-129">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f3e6-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0f3e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3e6-131">CommonParameters</span></span>
<span data-ttu-id="0f3e6-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3e6-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3e6-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f3e6-134">INPUTS</span></span>

### <span data-ttu-id="0f3e6-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0f3e6-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0f3e6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f3e6-136">OUTPUTS</span></span>

### <span data-ttu-id="0f3e6-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0f3e6-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0f3e6-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f3e6-138">NOTES</span></span>

<span data-ttu-id="0f3e6-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0f3e6-139">ALIASES</span></span>

<span data-ttu-id="0f3e6-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0f3e6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f3e6-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f3e6-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f3e6-143">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0f3e6-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f3e6-144">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0f3e6-145">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0f3e6-146">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0f3e6-147">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0f3e6-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0f3e6-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f3e6-149">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0f3e6-150">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0f3e6-151">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0f3e6-152">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0f3e6-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0f3e6-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0f3e6-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f3e6-154">RELATED LINKS</span></span>

