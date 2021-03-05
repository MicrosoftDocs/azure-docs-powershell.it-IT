---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 06c824c140f18c81ca3ce1547257e4765a2543b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964445"
---
# <span data-ttu-id="0b3f3-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="0b3f3-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="0b3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3f3-103">Restituisce una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-103">Returns a data connection.</span></span>

## <span data-ttu-id="0b3f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b3f3-104">SYNTAX</span></span>

### <span data-ttu-id="0b3f3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b3f3-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3f3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0b3f3-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b3f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0b3f3-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b3f3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b3f3-108">DESCRIPTION</span></span>
<span data-ttu-id="0b3f3-109">Restituisce una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-109">Returns a data connection.</span></span>

## <span data-ttu-id="0b3f3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b3f3-110">EXAMPLES</span></span>

### <span data-ttu-id="0b3f3-111">Esempio 1: Elencare tutte le connessioni dati in un database specifico</span><span class="sxs-lookup"><span data-stu-id="0b3f3-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="0b3f3-112">Il comando precedente restituisce tutti i database Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="0b3f3-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="0b3f3-113">Esempio 2: Ottenere una specifica connessione dati in base al nome</span><span class="sxs-lookup"><span data-stu-id="0b3f3-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="0b3f3-114">Il comando precedente restituisce la connessione dati denominata "mykustodataconnection" nel database "mykustodatabase" del cluster esistente "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="0b3f3-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="0b3f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b3f3-115">PARAMETERS</span></span>

### <span data-ttu-id="0b3f3-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b3f3-116">-ClusterName</span></span>
<span data-ttu-id="0b3f3-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0b3f3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b3f3-118">-DatabaseName</span></span>
<span data-ttu-id="0b3f3-119">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0b3f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3f3-120">-DefaultProfile</span></span>
<span data-ttu-id="0b3f3-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b3f3-122">-InputObject</span></span>
<span data-ttu-id="0b3f3-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b3f3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0b3f3-124">-Name</span></span>
<span data-ttu-id="0b3f3-125">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b3f3-127">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0b3f3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b3f3-128">-SubscriptionId</span></span>
<span data-ttu-id="0b3f3-129">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b3f3-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0b3f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3f3-131">CommonParameters</span></span>
<span data-ttu-id="0b3f3-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3f3-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3f3-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b3f3-134">INPUTS</span></span>

### <span data-ttu-id="0b3f3-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0b3f3-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0b3f3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b3f3-136">OUTPUTS</span></span>

### <span data-ttu-id="0b3f3-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="0b3f3-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="0b3f3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b3f3-138">NOTES</span></span>

<span data-ttu-id="0b3f3-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0b3f3-139">ALIASES</span></span>

<span data-ttu-id="0b3f3-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0b3f3-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b3f3-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b3f3-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b3f3-143">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0b3f3-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b3f3-144">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0b3f3-145">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0b3f3-146">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0b3f3-147">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0b3f3-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0b3f3-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b3f3-149">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0b3f3-150">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0b3f3-151">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0b3f3-152">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0b3f3-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0b3f3-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0b3f3-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b3f3-154">RELATED LINKS</span></span>

