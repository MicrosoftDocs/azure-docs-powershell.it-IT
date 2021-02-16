---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187343"
---
# <span data-ttu-id="a715f-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="a715f-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="a715f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a715f-102">SYNOPSIS</span></span>
<span data-ttu-id="a715f-103">Crea una soluzione di analisi dei log.</span><span class="sxs-lookup"><span data-stu-id="a715f-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="a715f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a715f-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a715f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a715f-105">DESCRIPTION</span></span>
<span data-ttu-id="a715f-106">Crea una soluzione di analisi dei log.</span><span class="sxs-lookup"><span data-stu-id="a715f-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="a715f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a715f-107">EXAMPLES</span></span>

### <span data-ttu-id="a715f-108">Esempio 1: Creare una soluzione di analisi del log di monitoraggio per l'area di lavoro analisi log</span><span class="sxs-lookup"><span data-stu-id="a715f-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a715f-109">Questo comando crea una soluzione di analisi del log di monitoraggio per l'area di lavoro di analisi dei log.</span><span class="sxs-lookup"><span data-stu-id="a715f-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="a715f-110">I tipi di uso più comune sono:</span><span class="sxs-lookup"><span data-stu-id="a715f-110">Commonly used types are:</span></span>

| <span data-ttu-id="a715f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a715f-111">Type</span></span> | <span data-ttu-id="a715f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a715f-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="a715f-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="a715f-113">SecurityCenterFree</span></span> |  <span data-ttu-id="a715f-114">Centro sicurezza di Azure - Edizione gratuita</span><span class="sxs-lookup"><span data-stu-id="a715f-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="a715f-115">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="a715f-115">Security</span></span> | <span data-ttu-id="a715f-116">Centro sicurezza di Azure</span><span class="sxs-lookup"><span data-stu-id="a715f-116">Azure Security Center</span></span> |
| <span data-ttu-id="a715f-117">Aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="a715f-117">Updates</span></span> | <span data-ttu-id="a715f-118">Gestione degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="a715f-118">Update Management</span></span> |
| <span data-ttu-id="a715f-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="a715f-119">ContainerInsights</span></span> | <span data-ttu-id="a715f-120">Azure Monitor for Containers</span><span class="sxs-lookup"><span data-stu-id="a715f-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="a715f-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="a715f-121">ServiceMap</span></span> | <span data-ttu-id="a715f-122">Service Map</span><span class="sxs-lookup"><span data-stu-id="a715f-122">Service Map</span></span> |
| <span data-ttu-id="a715f-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="a715f-123">AzureActivity</span></span> | <span data-ttu-id="a715f-124">Analisi del log attività</span><span class="sxs-lookup"><span data-stu-id="a715f-124">Activity log analytics</span></span> |
| <span data-ttu-id="a715f-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="a715f-125">ChangeTracking</span></span> | <span data-ttu-id="a715f-126">Rilevamento delle modifiche e inventario</span><span class="sxs-lookup"><span data-stu-id="a715f-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="a715f-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="a715f-127">VMInsights</span></span> | <span data-ttu-id="a715f-128">Monitoraggio di Azure per le macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="a715f-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="a715f-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="a715f-129">SecurityInsights</span></span> | <span data-ttu-id="a715f-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="a715f-130">Azure Sentinel</span></span> |
| <span data-ttu-id="a715f-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="a715f-131">NetworkMonitoring</span></span> | <span data-ttu-id="a715f-132">Network Performance Monitor</span><span class="sxs-lookup"><span data-stu-id="a715f-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="a715f-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="a715f-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="a715f-134">SQL valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="a715f-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="a715f-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a715f-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="a715f-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a715f-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="a715f-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="a715f-137">AntiMalware</span></span> | <span data-ttu-id="a715f-138">Valutazione antimalware</span><span class="sxs-lookup"><span data-stu-id="a715f-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="a715f-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="a715f-139">AzureAutomation</span></span> | <span data-ttu-id="a715f-140">Utente ibrido di automazione</span><span class="sxs-lookup"><span data-stu-id="a715f-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="a715f-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="a715f-141">LogicAppsManagement</span></span> | <span data-ttu-id="a715f-142">Gestione delle app per la logica</span><span class="sxs-lookup"><span data-stu-id="a715f-142">Logic Apps Management</span></span> |
| <span data-ttu-id="a715f-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="a715f-143">SQLDataClassification</span></span> | <span data-ttu-id="a715f-144">SQL classificazione & individuazione dati</span><span class="sxs-lookup"><span data-stu-id="a715f-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="a715f-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a715f-145">PARAMETERS</span></span>

### <span data-ttu-id="a715f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a715f-146">-DefaultProfile</span></span>
<span data-ttu-id="a715f-147">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a715f-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a715f-148">-Location</span><span class="sxs-lookup"><span data-stu-id="a715f-148">-Location</span></span>
<span data-ttu-id="a715f-149">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a715f-149">Resource location.</span></span>
<span data-ttu-id="a715f-150">Deve essere uguale all'area di lavoro di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="a715f-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a715f-151">-ResourceGroupName</span></span>
<span data-ttu-id="a715f-152">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a715f-152">The name of the resource group to get.</span></span>
<span data-ttu-id="a715f-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a715f-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a715f-154">-SubscriptionId</span></span>
<span data-ttu-id="a715f-155">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a715f-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a715f-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a715f-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="a715f-157">-Tag</span></span>
<span data-ttu-id="a715f-158">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="a715f-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-159">-Type</span><span class="sxs-lookup"><span data-stu-id="a715f-159">-Type</span></span>
<span data-ttu-id="a715f-160">Tipo di soluzione da creare.</span><span class="sxs-lookup"><span data-stu-id="a715f-160">Type of the solution to be created.</span></span>
<span data-ttu-id="a715f-161">Ad esempio, "Contenitore".</span><span class="sxs-lookup"><span data-stu-id="a715f-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a715f-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="a715f-163">ID delle risorse di Azure per l'area di lavoro in cui verrà distribuita/abilitata la soluzione.</span><span class="sxs-lookup"><span data-stu-id="a715f-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a715f-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a715f-164">-Confirm</span></span>
<span data-ttu-id="a715f-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a715f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a715f-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a715f-166">-WhatIf</span></span>
<span data-ttu-id="a715f-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a715f-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a715f-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a715f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a715f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a715f-169">CommonParameters</span></span>
<span data-ttu-id="a715f-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a715f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a715f-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a715f-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a715f-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="a715f-172">INPUTS</span></span>

## <span data-ttu-id="a715f-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a715f-173">OUTPUTS</span></span>

### <span data-ttu-id="a715f-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="a715f-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="a715f-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="a715f-175">NOTES</span></span>

<span data-ttu-id="a715f-176">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a715f-176">ALIASES</span></span>

## <span data-ttu-id="a715f-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a715f-177">RELATED LINKS</span></span>



[<span data-ttu-id="a715f-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a715f-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

