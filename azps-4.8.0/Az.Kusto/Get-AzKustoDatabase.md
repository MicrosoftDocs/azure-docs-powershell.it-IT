---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189813"
---
# <span data-ttu-id="933c4-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="933c4-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="933c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="933c4-102">SYNOPSIS</span></span>
<span data-ttu-id="933c4-103">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="933c4-103">Returns a database.</span></span>

## <span data-ttu-id="933c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="933c4-104">SYNTAX</span></span>

### <span data-ttu-id="933c4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="933c4-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="933c4-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="933c4-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="933c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="933c4-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="933c4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="933c4-108">DESCRIPTION</span></span>
<span data-ttu-id="933c4-109">Restituisce un database.</span><span class="sxs-lookup"><span data-stu-id="933c4-109">Returns a database.</span></span>

## <span data-ttu-id="933c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="933c4-110">EXAMPLES</span></span>

### <span data-ttu-id="933c4-111">Esempio 1: elencare tutti i database di Kusto in un cluster per nome</span><span class="sxs-lookup"><span data-stu-id="933c4-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="933c4-112">Il comando precedente restituisce tutti i database di Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="933c4-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="933c4-113">Esempio 2: ottenere un database di Kusto specifico per nome</span><span class="sxs-lookup"><span data-stu-id="933c4-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="933c4-114">Il comando precedente restituisce il database di Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="933c4-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="933c4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="933c4-115">PARAMETERS</span></span>

### <span data-ttu-id="933c4-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="933c4-116">-ClusterName</span></span>
<span data-ttu-id="933c4-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="933c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933c4-118">-DefaultProfile</span></span>
<span data-ttu-id="933c4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="933c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="933c4-120">-InputObject</span></span>
<span data-ttu-id="933c4-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="933c4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="933c4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="933c4-122">-Name</span></span>
<span data-ttu-id="933c4-123">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="933c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="933c4-125">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="933c4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="933c4-126">-SubscriptionId</span></span>
<span data-ttu-id="933c4-127">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="933c4-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="933c4-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="933c4-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="933c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933c4-129">CommonParameters</span></span>
<span data-ttu-id="933c4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933c4-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="933c4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933c4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="933c4-132">INPUTS</span></span>

### <span data-ttu-id="933c4-133">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="933c4-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="933c4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="933c4-134">OUTPUTS</span></span>

### <span data-ttu-id="933c4-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="933c4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="933c4-136">Note</span><span class="sxs-lookup"><span data-stu-id="933c4-136">NOTES</span></span>

<span data-ttu-id="933c4-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="933c4-137">ALIASES</span></span>

<span data-ttu-id="933c4-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="933c4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="933c4-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="933c4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="933c4-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="933c4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="933c4-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="933c4-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="933c4-142">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="933c4-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="933c4-143">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="933c4-144">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="933c4-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="933c4-145">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="933c4-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="933c4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="933c4-147">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="933c4-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="933c4-148">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="933c4-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="933c4-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="933c4-150">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="933c4-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="933c4-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="933c4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="933c4-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="933c4-152">RELATED LINKS</span></span>

