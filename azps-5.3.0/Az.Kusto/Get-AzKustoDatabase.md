---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474112"
---
# <span data-ttu-id="5ca13-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5ca13-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="5ca13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ca13-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca13-103">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="5ca13-103">Returns a database.</span></span>

## <span data-ttu-id="5ca13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ca13-104">SYNTAX</span></span>

### <span data-ttu-id="5ca13-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ca13-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ca13-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5ca13-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ca13-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ca13-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5ca13-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ca13-108">DESCRIPTION</span></span>
<span data-ttu-id="5ca13-109">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="5ca13-109">Returns a database.</span></span>

## <span data-ttu-id="5ca13-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ca13-110">EXAMPLES</span></span>

### <span data-ttu-id="5ca13-111">Esempio 1: elencare tutti i database di Kusto in un cluster per nome</span><span class="sxs-lookup"><span data-stu-id="5ca13-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5ca13-112">Il comando precedente restituisce tutti i database di Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="5ca13-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="5ca13-113">Esempio 2: ottenere un database di Kusto specifico per nome</span><span class="sxs-lookup"><span data-stu-id="5ca13-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5ca13-114">Il comando precedente restituisce il database di Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="5ca13-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="5ca13-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ca13-115">PARAMETERS</span></span>

### <span data-ttu-id="5ca13-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="5ca13-116">-ClusterName</span></span>
<span data-ttu-id="5ca13-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5ca13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca13-118">-DefaultProfile</span></span>
<span data-ttu-id="5ca13-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca13-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca13-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ca13-120">-InputObject</span></span>
<span data-ttu-id="5ca13-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5ca13-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ca13-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ca13-122">-Name</span></span>
<span data-ttu-id="5ca13-123">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5ca13-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca13-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ca13-125">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5ca13-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ca13-126">-SubscriptionId</span></span>
<span data-ttu-id="5ca13-127">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca13-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ca13-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5ca13-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ca13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca13-129">CommonParameters</span></span>
<span data-ttu-id="5ca13-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca13-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ca13-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca13-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ca13-132">INPUTS</span></span>

### <span data-ttu-id="5ca13-133">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5ca13-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5ca13-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ca13-134">OUTPUTS</span></span>

### <span data-ttu-id="5ca13-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. IDatabase</span><span class="sxs-lookup"><span data-stu-id="5ca13-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="5ca13-136">Note</span><span class="sxs-lookup"><span data-stu-id="5ca13-136">NOTES</span></span>

<span data-ttu-id="5ca13-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5ca13-137">ALIASES</span></span>

<span data-ttu-id="5ca13-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ca13-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ca13-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5ca13-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ca13-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ca13-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ca13-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5ca13-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ca13-142">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="5ca13-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5ca13-143">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5ca13-144">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="5ca13-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5ca13-145">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5ca13-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5ca13-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ca13-147">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca13-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5ca13-148">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5ca13-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="5ca13-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5ca13-150">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca13-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ca13-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5ca13-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5ca13-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ca13-152">RELATED LINKS</span></span>

