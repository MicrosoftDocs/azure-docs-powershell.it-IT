---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 714f971b32f9863ab2e5dc088d07859f2f5181a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964430"
---
# <span data-ttu-id="48610-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="48610-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="48610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48610-102">SYNOPSIS</span></span>
<span data-ttu-id="48610-103">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="48610-103">Returns a database.</span></span>

## <span data-ttu-id="48610-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48610-104">SYNTAX</span></span>

### <span data-ttu-id="48610-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48610-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48610-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="48610-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48610-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48610-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="48610-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48610-108">DESCRIPTION</span></span>
<span data-ttu-id="48610-109">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="48610-109">Returns a database.</span></span>

## <span data-ttu-id="48610-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48610-110">EXAMPLES</span></span>

### <span data-ttu-id="48610-111">Esempio 1: Elencare tutti i database Kusto in un cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="48610-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="48610-112">Il comando precedente restituisce tutti i database Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="48610-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="48610-113">Esempio 2: Ottenere un database kusto specifico in base al nome</span><span class="sxs-lookup"><span data-stu-id="48610-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="48610-114">Il comando precedente restituisce il database Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="48610-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="48610-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48610-115">PARAMETERS</span></span>

### <span data-ttu-id="48610-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="48610-116">-ClusterName</span></span>
<span data-ttu-id="48610-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="48610-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48610-118">-DefaultProfile</span></span>
<span data-ttu-id="48610-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48610-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48610-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48610-120">-InputObject</span></span>
<span data-ttu-id="48610-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="48610-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48610-122">-Name</span><span class="sxs-lookup"><span data-stu-id="48610-122">-Name</span></span>
<span data-ttu-id="48610-123">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48610-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48610-124">-ResourceGroupName</span></span>
<span data-ttu-id="48610-125">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="48610-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48610-126">-SubscriptionId</span></span>
<span data-ttu-id="48610-127">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48610-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="48610-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="48610-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="48610-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48610-129">CommonParameters</span></span>
<span data-ttu-id="48610-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48610-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48610-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48610-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48610-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="48610-132">INPUTS</span></span>

### <span data-ttu-id="48610-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="48610-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="48610-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48610-134">OUTPUTS</span></span>

### <span data-ttu-id="48610-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="48610-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="48610-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="48610-136">NOTES</span></span>

<span data-ttu-id="48610-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="48610-137">ALIASES</span></span>

<span data-ttu-id="48610-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="48610-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48610-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="48610-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48610-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48610-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48610-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="48610-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48610-142">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="48610-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="48610-143">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="48610-144">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="48610-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="48610-145">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="48610-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="48610-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48610-147">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="48610-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="48610-148">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="48610-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="48610-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48610-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="48610-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48610-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="48610-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="48610-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48610-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48610-152">RELATED LINKS</span></span>

