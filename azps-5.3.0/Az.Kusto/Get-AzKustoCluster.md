---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487184"
---
# <span data-ttu-id="b9fa9-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b9fa9-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="b9fa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fa9-103">Ottiene un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="b9fa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-104">SYNTAX</span></span>

### <span data-ttu-id="b9fa9-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9fa9-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9fa9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b9fa9-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9fa9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fa9-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9fa9-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="b9fa9-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9fa9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9fa9-109">DESCRIPTION</span></span>
<span data-ttu-id="b9fa9-110">Ottiene un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="b9fa9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-111">EXAMPLES</span></span>

### <span data-ttu-id="b9fa9-112">Esempio 1: elencare tutti i cluster di Kusto in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b9fa9-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="b9fa9-113">Il comando precedente elenca tutti i cluster kusto nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="b9fa9-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="b9fa9-114">Esempio 2: ottenere un cluster specifico di Kusto per nome</span><span class="sxs-lookup"><span data-stu-id="b9fa9-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="b9fa9-115">Il comando precedente restituisce il cluster kusto denominato "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="b9fa9-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="b9fa9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-116">PARAMETERS</span></span>

### <span data-ttu-id="b9fa9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fa9-117">-DefaultProfile</span></span>
<span data-ttu-id="b9fa9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fa9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9fa9-119">-InputObject</span></span>
<span data-ttu-id="b9fa9-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9fa9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9fa9-121">-Name</span></span>
<span data-ttu-id="b9fa9-122">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fa9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fa9-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9fa9-124">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b9fa9-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9fa9-125">-SubscriptionId</span></span>
<span data-ttu-id="b9fa9-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9fa9-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fa9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fa9-128">CommonParameters</span></span>
<span data-ttu-id="b9fa9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fa9-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9fa9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fa9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-131">INPUTS</span></span>

### <span data-ttu-id="b9fa9-132">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fa9-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b9fa9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9fa9-133">OUTPUTS</span></span>

### <span data-ttu-id="b9fa9-134">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="b9fa9-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="b9fa9-135">Note</span><span class="sxs-lookup"><span data-stu-id="b9fa9-135">NOTES</span></span>

<span data-ttu-id="b9fa9-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b9fa9-136">ALIASES</span></span>

<span data-ttu-id="b9fa9-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9fa9-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9fa9-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9fa9-140">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b9fa9-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9fa9-141">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b9fa9-142">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b9fa9-143">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b9fa9-144">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b9fa9-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b9fa9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9fa9-146">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b9fa9-147">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b9fa9-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b9fa9-149">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b9fa9-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b9fa9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9fa9-151">RELATED LINKS</span></span>

