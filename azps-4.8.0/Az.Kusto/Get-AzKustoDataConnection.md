---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033429"
---
# <span data-ttu-id="687c3-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="687c3-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="687c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="687c3-102">SYNOPSIS</span></span>
<span data-ttu-id="687c3-103">Restituisce una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="687c3-103">Returns a data connection.</span></span>

## <span data-ttu-id="687c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="687c3-104">SYNTAX</span></span>

### <span data-ttu-id="687c3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="687c3-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="687c3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="687c3-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="687c3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="687c3-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="687c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="687c3-108">DESCRIPTION</span></span>
<span data-ttu-id="687c3-109">Restituisce una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="687c3-109">Returns a data connection.</span></span>

## <span data-ttu-id="687c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="687c3-110">EXAMPLES</span></span>

### <span data-ttu-id="687c3-111">Esempio 1: elencare tutte le connessioni dati in un database specifico</span><span class="sxs-lookup"><span data-stu-id="687c3-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="687c3-112">Il comando precedente restituisce tutti i database di Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="687c3-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="687c3-113">Esempio 2: ottenere una connessione dati specifica per nome</span><span class="sxs-lookup"><span data-stu-id="687c3-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="687c3-114">Il comando precedente restituisce la connessione dati denominata "mykustodataconnection" nel database "mykustodatabase" del cluster esistente "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="687c3-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="687c3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="687c3-115">PARAMETERS</span></span>

### <span data-ttu-id="687c3-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="687c3-116">-ClusterName</span></span>
<span data-ttu-id="687c3-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="687c3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="687c3-118">-DatabaseName</span></span>
<span data-ttu-id="687c3-119">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="687c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687c3-120">-DefaultProfile</span></span>
<span data-ttu-id="687c3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="687c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687c3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="687c3-122">-InputObject</span></span>
<span data-ttu-id="687c3-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="687c3-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="687c3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="687c3-124">-Name</span></span>
<span data-ttu-id="687c3-125">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="687c3-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="687c3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687c3-126">-ResourceGroupName</span></span>
<span data-ttu-id="687c3-127">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="687c3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="687c3-128">-SubscriptionId</span></span>
<span data-ttu-id="687c3-129">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="687c3-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="687c3-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="687c3-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="687c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687c3-131">CommonParameters</span></span>
<span data-ttu-id="687c3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="687c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687c3-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="687c3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687c3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="687c3-134">INPUTS</span></span>

### <span data-ttu-id="687c3-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="687c3-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="687c3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="687c3-136">OUTPUTS</span></span>

### <span data-ttu-id="687c3-137">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="687c3-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="687c3-138">Note</span><span class="sxs-lookup"><span data-stu-id="687c3-138">NOTES</span></span>

<span data-ttu-id="687c3-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="687c3-139">ALIASES</span></span>

<span data-ttu-id="687c3-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="687c3-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="687c3-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="687c3-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="687c3-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="687c3-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="687c3-143">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="687c3-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="687c3-144">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="687c3-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="687c3-145">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="687c3-146">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="687c3-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="687c3-147">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="687c3-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="687c3-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="687c3-149">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="687c3-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="687c3-150">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="687c3-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="687c3-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="687c3-152">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="687c3-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="687c3-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="687c3-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="687c3-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="687c3-154">RELATED LINKS</span></span>

