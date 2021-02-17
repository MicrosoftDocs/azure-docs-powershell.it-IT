---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185287"
---
# <span data-ttu-id="98438-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="98438-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="98438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98438-102">SYNOPSIS</span></span>
<span data-ttu-id="98438-103">Ottiene un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="98438-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98438-104">SYNTAX</span></span>

### <span data-ttu-id="98438-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98438-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98438-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="98438-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98438-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98438-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98438-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="98438-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="98438-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98438-109">DESCRIPTION</span></span>
<span data-ttu-id="98438-110">Ottiene un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="98438-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98438-111">EXAMPLES</span></span>

### <span data-ttu-id="98438-112">Esempio 1: Elencare tutti i cluster Kusto in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="98438-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="98438-113">Il comando precedente elenca tutti i cluster Kusto nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="98438-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="98438-114">Esempio 2: Ottenere un cluster Kusto specifico per nome</span><span class="sxs-lookup"><span data-stu-id="98438-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="98438-115">Il comando precedente restituisce il cluster Kusto denominato "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="98438-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="98438-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98438-116">PARAMETERS</span></span>

### <span data-ttu-id="98438-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98438-117">-DefaultProfile</span></span>
<span data-ttu-id="98438-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98438-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98438-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98438-119">-InputObject</span></span>
<span data-ttu-id="98438-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="98438-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="98438-121">-Name</span><span class="sxs-lookup"><span data-stu-id="98438-121">-Name</span></span>
<span data-ttu-id="98438-122">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="98438-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98438-123">-ResourceGroupName</span></span>
<span data-ttu-id="98438-124">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="98438-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98438-125">-SubscriptionId</span></span>
<span data-ttu-id="98438-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98438-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="98438-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="98438-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="98438-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98438-128">CommonParameters</span></span>
<span data-ttu-id="98438-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98438-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98438-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98438-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98438-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="98438-131">INPUTS</span></span>

### <span data-ttu-id="98438-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="98438-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="98438-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98438-133">OUTPUTS</span></span>

### <span data-ttu-id="98438-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="98438-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="98438-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="98438-135">NOTES</span></span>

<span data-ttu-id="98438-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="98438-136">ALIASES</span></span>

<span data-ttu-id="98438-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="98438-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98438-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="98438-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98438-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98438-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98438-140">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="98438-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98438-141">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="98438-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="98438-142">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="98438-143">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="98438-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="98438-144">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="98438-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="98438-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98438-146">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="98438-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="98438-147">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="98438-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="98438-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="98438-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="98438-149">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98438-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="98438-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="98438-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="98438-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98438-151">RELATED LINKS</span></span>

