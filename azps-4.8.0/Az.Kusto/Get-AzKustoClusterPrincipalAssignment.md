---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033430"
---
# <span data-ttu-id="f86ad-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f86ad-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f86ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f86ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f86ad-103">Ottiene un cluster di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f86ad-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f86ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f86ad-104">SYNTAX</span></span>

### <span data-ttu-id="f86ad-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f86ad-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f86ad-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f86ad-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f86ad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f86ad-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f86ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f86ad-108">DESCRIPTION</span></span>
<span data-ttu-id="f86ad-109">Ottiene un cluster di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f86ad-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f86ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f86ad-110">EXAMPLES</span></span>

### <span data-ttu-id="f86ad-111">Esempio 1: elenca tutti i principalAssignment di cluster kusto</span><span class="sxs-lookup"><span data-stu-id="f86ad-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f86ad-112">Il comando precedente elenca tutti i principalAssignment nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f86ad-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f86ad-113">Esempio 2: ottiene un cluster kusto principalAssignment per nome</span><span class="sxs-lookup"><span data-stu-id="f86ad-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f86ad-114">Il comando precedente restituisce il cluster kusto principalAssignment denominato "kustoprincipal1" nel cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="f86ad-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f86ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f86ad-115">PARAMETERS</span></span>

### <span data-ttu-id="f86ad-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f86ad-116">-ClusterName</span></span>
<span data-ttu-id="f86ad-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f86ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86ad-118">-DefaultProfile</span></span>
<span data-ttu-id="f86ad-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f86ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f86ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f86ad-120">-InputObject</span></span>
<span data-ttu-id="f86ad-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f86ad-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f86ad-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f86ad-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f86ad-123">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f86ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f86ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="f86ad-125">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f86ad-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f86ad-126">-SubscriptionId</span></span>
<span data-ttu-id="f86ad-127">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f86ad-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f86ad-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f86ad-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f86ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86ad-129">CommonParameters</span></span>
<span data-ttu-id="f86ad-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f86ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86ad-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f86ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86ad-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f86ad-132">INPUTS</span></span>

### <span data-ttu-id="f86ad-133">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f86ad-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f86ad-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f86ad-134">OUTPUTS</span></span>

### <span data-ttu-id="f86ad-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f86ad-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f86ad-136">Note</span><span class="sxs-lookup"><span data-stu-id="f86ad-136">NOTES</span></span>

<span data-ttu-id="f86ad-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f86ad-137">ALIASES</span></span>

<span data-ttu-id="f86ad-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f86ad-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f86ad-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f86ad-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f86ad-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f86ad-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f86ad-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f86ad-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f86ad-142">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="f86ad-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f86ad-143">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f86ad-144">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f86ad-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f86ad-145">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f86ad-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f86ad-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f86ad-147">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f86ad-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f86ad-148">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f86ad-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f86ad-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f86ad-150">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f86ad-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f86ad-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f86ad-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f86ad-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f86ad-152">RELATED LINKS</span></span>

