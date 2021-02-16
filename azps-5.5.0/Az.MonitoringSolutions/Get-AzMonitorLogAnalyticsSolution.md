---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187374"
---
# <span data-ttu-id="06336-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="06336-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="06336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06336-102">SYNOPSIS</span></span>
<span data-ttu-id="06336-103">Recupera la soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="06336-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="06336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06336-104">SYNTAX</span></span>

### <span data-ttu-id="06336-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06336-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="06336-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="06336-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06336-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06336-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="06336-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="06336-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="06336-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06336-109">DESCRIPTION</span></span>
<span data-ttu-id="06336-110">Recupera la soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="06336-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="06336-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06336-111">EXAMPLES</span></span>

### <span data-ttu-id="06336-112">Esempio 1: Ottenere una soluzione di analisi del log di monitoraggio in base al nome</span><span class="sxs-lookup"><span data-stu-id="06336-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="06336-113">Questo comando ottiene una soluzione di analisi del log di monitoraggio in base al nome.</span><span class="sxs-lookup"><span data-stu-id="06336-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="06336-114">Esempio 2: Ottenere una soluzione di analisi del log di monitoraggio in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="06336-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="06336-115">Questo comando ottiene una soluzione di analisi del log di monitoraggio in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="06336-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="06336-116">Esempio 3: Ottenere una soluzione di analisi del log di monitoraggio per oggetto</span><span class="sxs-lookup"><span data-stu-id="06336-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="06336-117">Questo comando ottiene una soluzione di analisi del log di monitoraggio per oggetto.</span><span class="sxs-lookup"><span data-stu-id="06336-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="06336-118">Esempio 4: Ottenere tutte le soluzioni di analisi del log di monitoraggio in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="06336-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="06336-119">Questo comando recupera tutte le soluzioni di analisi del log di monitoraggio in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06336-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="06336-120">Esempio 5: Ottenere tutte le soluzioni di analisi del log di monitoraggio in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="06336-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="06336-121">Questo comando recupera tutte le soluzioni di analisi del log di monitoraggio in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="06336-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="06336-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06336-122">PARAMETERS</span></span>

### <span data-ttu-id="06336-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06336-123">-DefaultProfile</span></span>
<span data-ttu-id="06336-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06336-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06336-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06336-125">-InputObject</span></span>
<span data-ttu-id="06336-126">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="06336-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06336-127">-Name</span><span class="sxs-lookup"><span data-stu-id="06336-127">-Name</span></span>
<span data-ttu-id="06336-128">Nome della soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="06336-128">User Solution Name.</span></span>

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

### <span data-ttu-id="06336-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06336-129">-ResourceGroupName</span></span>
<span data-ttu-id="06336-130">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="06336-130">The name of the resource group to get.</span></span>
<span data-ttu-id="06336-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="06336-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="06336-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06336-132">-SubscriptionId</span></span>
<span data-ttu-id="06336-133">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06336-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06336-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="06336-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06336-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06336-135">CommonParameters</span></span>
<span data-ttu-id="06336-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06336-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06336-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06336-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06336-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="06336-138">INPUTS</span></span>

### <span data-ttu-id="06336-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="06336-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="06336-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06336-140">OUTPUTS</span></span>

### <span data-ttu-id="06336-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="06336-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="06336-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="06336-142">NOTES</span></span>

<span data-ttu-id="06336-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="06336-143">ALIASES</span></span>

<span data-ttu-id="06336-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="06336-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06336-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="06336-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06336-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06336-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06336-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="06336-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06336-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="06336-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06336-149">`[ManagementAssociationName <String>]`: nome utente ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="06336-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="06336-150">`[ManagementConfigurationName <String>]`: nome configurazione gestione utenti.</span><span class="sxs-lookup"><span data-stu-id="06336-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="06336-151">`[ProviderName <String>]`: nome del provider per la risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="06336-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="06336-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="06336-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="06336-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="06336-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="06336-154">`[ResourceName <String>]`: nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="06336-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="06336-155">`[ResourceType <String>]`: tipo di risorsa per la risorsa padre</span><span class="sxs-lookup"><span data-stu-id="06336-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="06336-156">`[SolutionName <String>]`: nome della soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="06336-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="06336-157">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06336-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06336-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="06336-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06336-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06336-159">RELATED LINKS</span></span>

