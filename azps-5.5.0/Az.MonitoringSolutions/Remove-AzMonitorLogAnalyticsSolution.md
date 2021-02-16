---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187335"
---
# <span data-ttu-id="05e41-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="05e41-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="05e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e41-102">SYNOPSIS</span></span>
<span data-ttu-id="05e41-103">Elimina la soluzione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="05e41-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="05e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05e41-104">SYNTAX</span></span>

### <span data-ttu-id="05e41-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05e41-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05e41-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05e41-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05e41-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05e41-107">DESCRIPTION</span></span>
<span data-ttu-id="05e41-108">Elimina la soluzione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="05e41-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="05e41-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05e41-109">EXAMPLES</span></span>

### <span data-ttu-id="05e41-110">Esempio 1: Rimuovere una soluzione di analisi del log di monitoraggio in base al nome</span><span class="sxs-lookup"><span data-stu-id="05e41-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="05e41-111">Questo comando rimuove una soluzione di analisi del log di monitoraggio in base al nome.</span><span class="sxs-lookup"><span data-stu-id="05e41-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="05e41-112">Esempio 2: Rimuovere una soluzione di analisi del log di monitoraggio per oggetto</span><span class="sxs-lookup"><span data-stu-id="05e41-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="05e41-113">Questo comando rimuove una soluzione di analisi del log di monitoraggio per oggetto.</span><span class="sxs-lookup"><span data-stu-id="05e41-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="05e41-114">Esempio 3: Rimuovere una soluzione di analisi del log di monitoraggio tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="05e41-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="05e41-115">Questo comando rimuove una soluzione di analisi del log di monitoraggio tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="05e41-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="05e41-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05e41-116">PARAMETERS</span></span>

### <span data-ttu-id="05e41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e41-117">-DefaultProfile</span></span>
<span data-ttu-id="05e41-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05e41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05e41-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05e41-119">-InputObject</span></span>
<span data-ttu-id="05e41-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="05e41-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-121">-Name</span><span class="sxs-lookup"><span data-stu-id="05e41-121">-Name</span></span>
<span data-ttu-id="05e41-122">Nome della soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="05e41-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05e41-123">-PassThru</span></span>
<span data-ttu-id="05e41-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="05e41-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e41-125">-ResourceGroupName</span></span>
<span data-ttu-id="05e41-126">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="05e41-126">The name of the resource group to get.</span></span>
<span data-ttu-id="05e41-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="05e41-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05e41-128">-SubscriptionId</span></span>
<span data-ttu-id="05e41-129">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05e41-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="05e41-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="05e41-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05e41-131">-Confirm</span></span>
<span data-ttu-id="05e41-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e41-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e41-133">-WhatIf</span></span>
<span data-ttu-id="05e41-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05e41-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05e41-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05e41-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e41-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e41-136">CommonParameters</span></span>
<span data-ttu-id="05e41-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e41-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e41-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05e41-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e41-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="05e41-139">INPUTS</span></span>

### <span data-ttu-id="05e41-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="05e41-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="05e41-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05e41-141">OUTPUTS</span></span>

### <span data-ttu-id="05e41-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05e41-142">System.Boolean</span></span>

## <span data-ttu-id="05e41-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="05e41-143">NOTES</span></span>

<span data-ttu-id="05e41-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="05e41-144">ALIASES</span></span>

<span data-ttu-id="05e41-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="05e41-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05e41-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="05e41-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05e41-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05e41-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05e41-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="05e41-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05e41-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="05e41-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05e41-150">`[ManagementAssociationName <String>]`: nome utente ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="05e41-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="05e41-151">`[ManagementConfigurationName <String>]`: nome configurazione gestione utenti.</span><span class="sxs-lookup"><span data-stu-id="05e41-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="05e41-152">`[ProviderName <String>]`: nome del provider per la risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="05e41-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="05e41-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="05e41-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="05e41-154">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="05e41-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="05e41-155">`[ResourceName <String>]`: nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="05e41-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="05e41-156">`[ResourceType <String>]`: tipo di risorsa per la risorsa padre</span><span class="sxs-lookup"><span data-stu-id="05e41-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="05e41-157">`[SolutionName <String>]`: nome della soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="05e41-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="05e41-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="05e41-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="05e41-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="05e41-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="05e41-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05e41-160">RELATED LINKS</span></span>

