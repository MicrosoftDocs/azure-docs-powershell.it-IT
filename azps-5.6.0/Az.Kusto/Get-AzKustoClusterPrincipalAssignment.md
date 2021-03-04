---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b89327f80ec5f8e0f5faf9f66e943ee07601799e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964478"
---
# <span data-ttu-id="67aef-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="67aef-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="67aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67aef-102">SYNOPSIS</span></span>
<span data-ttu-id="67aef-103">Ottiene un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="67aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67aef-104">SYNTAX</span></span>

### <span data-ttu-id="67aef-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67aef-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67aef-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="67aef-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67aef-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67aef-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="67aef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67aef-108">DESCRIPTION</span></span>
<span data-ttu-id="67aef-109">Ottiene un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="67aef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67aef-110">EXAMPLES</span></span>

### <span data-ttu-id="67aef-111">Esempio 1: Elencare tutte le principalAssignment di Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="67aef-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="67aef-112">Il comando precedente elenca tutte le principalAssignment nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="67aef-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="67aef-113">Esempio 2: ottiene un principalAssignment cluster di Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="67aef-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="67aef-114">Il comando precedente restituisce l'attributo Kusto cluster principalAssignment denominato "kustoprincipal1" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="67aef-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="67aef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67aef-115">PARAMETERS</span></span>

### <span data-ttu-id="67aef-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67aef-116">-ClusterName</span></span>
<span data-ttu-id="67aef-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="67aef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67aef-118">-DefaultProfile</span></span>
<span data-ttu-id="67aef-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67aef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67aef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67aef-120">-InputObject</span></span>
<span data-ttu-id="67aef-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="67aef-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67aef-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="67aef-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="67aef-123">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="67aef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67aef-124">-ResourceGroupName</span></span>
<span data-ttu-id="67aef-125">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="67aef-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67aef-126">-SubscriptionId</span></span>
<span data-ttu-id="67aef-127">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67aef-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67aef-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="67aef-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67aef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67aef-129">CommonParameters</span></span>
<span data-ttu-id="67aef-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67aef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67aef-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67aef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67aef-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="67aef-132">INPUTS</span></span>

### <span data-ttu-id="67aef-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="67aef-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="67aef-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67aef-134">OUTPUTS</span></span>

### <span data-ttu-id="67aef-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="67aef-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="67aef-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="67aef-136">NOTES</span></span>

<span data-ttu-id="67aef-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67aef-137">ALIASES</span></span>

<span data-ttu-id="67aef-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="67aef-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67aef-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="67aef-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67aef-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67aef-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67aef-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="67aef-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67aef-142">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="67aef-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="67aef-143">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="67aef-144">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="67aef-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="67aef-145">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="67aef-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="67aef-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67aef-147">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67aef-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="67aef-148">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="67aef-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="67aef-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67aef-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="67aef-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67aef-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="67aef-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="67aef-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="67aef-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67aef-152">RELATED LINKS</span></span>

