---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185238"
---
# <span data-ttu-id="d115c-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d115c-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="d115c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d115c-102">SYNOPSIS</span></span>
<span data-ttu-id="d115c-103">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="d115c-103">Returns a database.</span></span>

## <span data-ttu-id="d115c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d115c-104">SYNTAX</span></span>

### <span data-ttu-id="d115c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d115c-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d115c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d115c-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d115c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d115c-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d115c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d115c-108">DESCRIPTION</span></span>
<span data-ttu-id="d115c-109">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="d115c-109">Returns a database.</span></span>

## <span data-ttu-id="d115c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d115c-110">EXAMPLES</span></span>

### <span data-ttu-id="d115c-111">Esempio 1: Elencare tutti i database Kusto in un cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="d115c-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d115c-112">Il comando precedente restituisce tutti i database Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="d115c-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d115c-113">Esempio 2: ottenere un database di Kusto specifico in base al nome</span><span class="sxs-lookup"><span data-stu-id="d115c-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d115c-114">Il comando precedente restituisce il database Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="d115c-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="d115c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d115c-115">PARAMETERS</span></span>

### <span data-ttu-id="d115c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d115c-116">-ClusterName</span></span>
<span data-ttu-id="d115c-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d115c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d115c-118">-DefaultProfile</span></span>
<span data-ttu-id="d115c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d115c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d115c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d115c-120">-InputObject</span></span>
<span data-ttu-id="d115c-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d115c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d115c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d115c-122">-Name</span></span>
<span data-ttu-id="d115c-123">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d115c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d115c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d115c-125">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d115c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d115c-126">-SubscriptionId</span></span>
<span data-ttu-id="d115c-127">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d115c-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d115c-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d115c-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d115c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d115c-129">CommonParameters</span></span>
<span data-ttu-id="d115c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d115c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d115c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d115c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d115c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="d115c-132">INPUTS</span></span>

### <span data-ttu-id="d115c-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d115c-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d115c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d115c-134">OUTPUTS</span></span>

### <span data-ttu-id="d115c-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="d115c-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="d115c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="d115c-136">NOTES</span></span>

<span data-ttu-id="d115c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d115c-137">ALIASES</span></span>

<span data-ttu-id="d115c-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d115c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d115c-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d115c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d115c-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d115c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d115c-141">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d115c-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d115c-142">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="d115c-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d115c-143">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d115c-144">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="d115c-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d115c-145">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d115c-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d115c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d115c-147">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d115c-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d115c-148">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d115c-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d115c-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d115c-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d115c-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d115c-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d115c-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d115c-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d115c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d115c-152">RELATED LINKS</span></span>

