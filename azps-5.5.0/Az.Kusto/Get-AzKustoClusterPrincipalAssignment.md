---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185270"
---
# <span data-ttu-id="00bd9-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="00bd9-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="00bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="00bd9-103">Ottiene un principalAssignment cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="00bd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00bd9-104">SYNTAX</span></span>

### <span data-ttu-id="00bd9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00bd9-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00bd9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="00bd9-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00bd9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00bd9-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="00bd9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00bd9-108">DESCRIPTION</span></span>
<span data-ttu-id="00bd9-109">Ottiene un principalAssignment cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="00bd9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00bd9-110">EXAMPLES</span></span>

### <span data-ttu-id="00bd9-111">Esempio 1: Elencare tutte le principalAssignment di Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="00bd9-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="00bd9-112">Il comando precedente elenca tutte le principalAssignment nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="00bd9-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="00bd9-113">Esempio 2: ottiene un principalAssignment cluster di Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="00bd9-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="00bd9-114">Il comando precedente restituisce l'attributo Kusto cluster principalAssignment denominato "kustoprincipal1" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="00bd9-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="00bd9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00bd9-115">PARAMETERS</span></span>

### <span data-ttu-id="00bd9-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="00bd9-116">-ClusterName</span></span>
<span data-ttu-id="00bd9-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="00bd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bd9-118">-DefaultProfile</span></span>
<span data-ttu-id="00bd9-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00bd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00bd9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00bd9-120">-InputObject</span></span>
<span data-ttu-id="00bd9-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="00bd9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00bd9-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="00bd9-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="00bd9-123">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="00bd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="00bd9-125">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="00bd9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00bd9-126">-SubscriptionId</span></span>
<span data-ttu-id="00bd9-127">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="00bd9-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="00bd9-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="00bd9-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="00bd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bd9-129">CommonParameters</span></span>
<span data-ttu-id="00bd9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bd9-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00bd9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bd9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="00bd9-132">INPUTS</span></span>

### <span data-ttu-id="00bd9-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="00bd9-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="00bd9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00bd9-134">OUTPUTS</span></span>

### <span data-ttu-id="00bd9-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="00bd9-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="00bd9-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="00bd9-136">NOTES</span></span>

<span data-ttu-id="00bd9-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="00bd9-137">ALIASES</span></span>

<span data-ttu-id="00bd9-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="00bd9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00bd9-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="00bd9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00bd9-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00bd9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00bd9-141">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="00bd9-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00bd9-142">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="00bd9-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="00bd9-143">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="00bd9-144">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="00bd9-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="00bd9-145">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="00bd9-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="00bd9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00bd9-147">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="00bd9-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="00bd9-148">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="00bd9-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="00bd9-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="00bd9-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="00bd9-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="00bd9-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="00bd9-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="00bd9-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="00bd9-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00bd9-152">RELATED LINKS</span></span>

