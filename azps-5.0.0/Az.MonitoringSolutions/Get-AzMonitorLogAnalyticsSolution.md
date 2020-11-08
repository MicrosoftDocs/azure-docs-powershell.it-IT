---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203485"
---
# <span data-ttu-id="a10ef-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="a10ef-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="a10ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a10ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a10ef-103">Recupera la soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a10ef-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="a10ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a10ef-104">SYNTAX</span></span>

### <span data-ttu-id="a10ef-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a10ef-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a10ef-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a10ef-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a10ef-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a10ef-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a10ef-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="a10ef-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a10ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a10ef-109">DESCRIPTION</span></span>
<span data-ttu-id="a10ef-110">Recupera la soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a10ef-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="a10ef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a10ef-111">EXAMPLES</span></span>

### <span data-ttu-id="a10ef-112">Esempio 1: ottenere una soluzione di analisi del log di monitoraggio per nome</span><span class="sxs-lookup"><span data-stu-id="a10ef-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a10ef-113">Questo comando consente di ottenere una soluzione di analisi del log di monitoraggio per nome.</span><span class="sxs-lookup"><span data-stu-id="a10ef-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="a10ef-114">Esempio 2: ottenere una soluzione di analisi del log di monitoraggio tramite ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a10ef-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a10ef-115">Questo comando consente di ottenere una soluzione di analisi del log di monitoraggio tramite ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a10ef-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="a10ef-116">Esempio 3: ottenere una soluzione di analisi del log di monitoraggio per oggetto</span><span class="sxs-lookup"><span data-stu-id="a10ef-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a10ef-117">Questo comando ottiene una soluzione di analisi del log di monitoraggio per oggetto.</span><span class="sxs-lookup"><span data-stu-id="a10ef-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="a10ef-118">Esempio 4: ottenere tutte le soluzioni di analisi del log di monitoraggio in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a10ef-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a10ef-119">Questo comando consente di ottenere tutte le soluzioni di analisi del log di monitor in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a10ef-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="a10ef-120">Esempio 5: ottenere tutte le soluzioni di analisi del log del monitor in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a10ef-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a10ef-121">Questo comando consente di ottenere tutte le soluzioni di analisi del log del monitor in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a10ef-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="a10ef-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a10ef-122">PARAMETERS</span></span>

### <span data-ttu-id="a10ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10ef-123">-DefaultProfile</span></span>
<span data-ttu-id="a10ef-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a10ef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a10ef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a10ef-125">-InputObject</span></span>
<span data-ttu-id="a10ef-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a10ef-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a10ef-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a10ef-127">-Name</span></span>
<span data-ttu-id="a10ef-128">Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a10ef-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a10ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a10ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="a10ef-130">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a10ef-130">The name of the resource group to get.</span></span>
<span data-ttu-id="a10ef-131">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a10ef-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a10ef-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a10ef-132">-SubscriptionId</span></span>
<span data-ttu-id="a10ef-133">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a10ef-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a10ef-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a10ef-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a10ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10ef-135">CommonParameters</span></span>
<span data-ttu-id="a10ef-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a10ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10ef-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a10ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10ef-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a10ef-138">INPUTS</span></span>

### <span data-ttu-id="a10ef-139">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="a10ef-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="a10ef-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a10ef-140">OUTPUTS</span></span>

### <span data-ttu-id="a10ef-141">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="a10ef-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="a10ef-142">Note</span><span class="sxs-lookup"><span data-stu-id="a10ef-142">NOTES</span></span>

<span data-ttu-id="a10ef-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a10ef-143">ALIASES</span></span>

<span data-ttu-id="a10ef-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a10ef-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a10ef-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a10ef-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a10ef-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a10ef-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a10ef-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a10ef-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a10ef-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a10ef-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a10ef-149">`[ManagementAssociationName <String>]`: Nome ManagementAssociation utente.</span><span class="sxs-lookup"><span data-stu-id="a10ef-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="a10ef-150">`[ManagementConfigurationName <String>]`: Nome configurazione gestione utenti.</span><span class="sxs-lookup"><span data-stu-id="a10ef-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="a10ef-151">`[ProviderName <String>]`: Nome provider per la risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a10ef-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="a10ef-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a10ef-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="a10ef-153">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a10ef-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="a10ef-154">`[ResourceName <String>]`: Nome risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a10ef-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="a10ef-155">`[ResourceType <String>]`: Tipo di risorsa per la risorsa padre</span><span class="sxs-lookup"><span data-stu-id="a10ef-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="a10ef-156">`[SolutionName <String>]`: Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a10ef-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="a10ef-157">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a10ef-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a10ef-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a10ef-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a10ef-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a10ef-159">RELATED LINKS</span></span>

