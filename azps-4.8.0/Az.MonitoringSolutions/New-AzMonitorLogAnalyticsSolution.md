---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189742"
---
# <span data-ttu-id="32cd2-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="32cd2-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="32cd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="32cd2-103">Crea una soluzione di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="32cd2-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="32cd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32cd2-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32cd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="32cd2-106">Crea una soluzione di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="32cd2-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="32cd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="32cd2-108">Esempio 1: creare una soluzione di analisi del log di monitoraggio per l'area di lavoro analisi log</span><span class="sxs-lookup"><span data-stu-id="32cd2-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="32cd2-109">Questo comando crea una soluzione di analisi del log di monitoraggio per l'area di lavoro analisi log.</span><span class="sxs-lookup"><span data-stu-id="32cd2-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="32cd2-110">I tipi comunemente usati sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32cd2-110">Commonly used types are:</span></span>

| <span data-ttu-id="32cd2-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="32cd2-111">Type</span></span> | <span data-ttu-id="32cd2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32cd2-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="32cd2-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="32cd2-113">SecurityCenterFree</span></span> |  <span data-ttu-id="32cd2-114">Azure Security Center-versione gratuita</span><span class="sxs-lookup"><span data-stu-id="32cd2-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="32cd2-115">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="32cd2-115">Security</span></span> | <span data-ttu-id="32cd2-116">Centro sicurezza di Azure</span><span class="sxs-lookup"><span data-stu-id="32cd2-116">Azure Security Center</span></span> |
| <span data-ttu-id="32cd2-117">Aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="32cd2-117">Updates</span></span> | <span data-ttu-id="32cd2-118">Gestione degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="32cd2-118">Update Management</span></span> |
| <span data-ttu-id="32cd2-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="32cd2-119">ContainerInsights</span></span> | <span data-ttu-id="32cd2-120">Monitor di Azure per i contenitori</span><span class="sxs-lookup"><span data-stu-id="32cd2-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="32cd2-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="32cd2-121">ServiceMap</span></span> | <span data-ttu-id="32cd2-122">Mappa del servizio</span><span class="sxs-lookup"><span data-stu-id="32cd2-122">Service Map</span></span> |
| <span data-ttu-id="32cd2-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="32cd2-123">AzureActivity</span></span> | <span data-ttu-id="32cd2-124">Analisi del log attività</span><span class="sxs-lookup"><span data-stu-id="32cd2-124">Activity log analytics</span></span> |
| <span data-ttu-id="32cd2-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="32cd2-125">ChangeTracking</span></span> | <span data-ttu-id="32cd2-126">Modifica del rilevamento e dell'inventario</span><span class="sxs-lookup"><span data-stu-id="32cd2-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="32cd2-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="32cd2-127">VMInsights</span></span> | <span data-ttu-id="32cd2-128">Monitor di Azure per VM</span><span class="sxs-lookup"><span data-stu-id="32cd2-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="32cd2-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="32cd2-129">SecurityInsights</span></span> | <span data-ttu-id="32cd2-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="32cd2-130">Azure Sentinel</span></span> |
| <span data-ttu-id="32cd2-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="32cd2-131">NetworkMonitoring</span></span> | <span data-ttu-id="32cd2-132">Monitoraggio delle prestazioni di rete</span><span class="sxs-lookup"><span data-stu-id="32cd2-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="32cd2-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="32cd2-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="32cd2-134">Valutazione della vulnerabilità SQL</span><span class="sxs-lookup"><span data-stu-id="32cd2-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="32cd2-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="32cd2-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="32cd2-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="32cd2-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="32cd2-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="32cd2-137">AntiMalware</span></span> | <span data-ttu-id="32cd2-138">Valutazione antimalware</span><span class="sxs-lookup"><span data-stu-id="32cd2-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="32cd2-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="32cd2-139">AzureAutomation</span></span> | <span data-ttu-id="32cd2-140">Lavoratore ibrido di automazione</span><span class="sxs-lookup"><span data-stu-id="32cd2-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="32cd2-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="32cd2-141">LogicAppsManagement</span></span> | <span data-ttu-id="32cd2-142">Gestione delle app logiche</span><span class="sxs-lookup"><span data-stu-id="32cd2-142">Logic Apps Management</span></span> |
| <span data-ttu-id="32cd2-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="32cd2-143">SQLDataClassification</span></span> | <span data-ttu-id="32cd2-144">Classificazione & individuazione dati SQL</span><span class="sxs-lookup"><span data-stu-id="32cd2-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="32cd2-145">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32cd2-145">PARAMETERS</span></span>

### <span data-ttu-id="32cd2-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cd2-146">-DefaultProfile</span></span>
<span data-ttu-id="32cd2-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32cd2-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32cd2-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="32cd2-148">-Location</span></span>
<span data-ttu-id="32cd2-149">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="32cd2-149">Resource location.</span></span>
<span data-ttu-id="32cd2-150">Deve essere uguale all'area di lavoro analitica del log.</span><span class="sxs-lookup"><span data-stu-id="32cd2-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="32cd2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cd2-151">-ResourceGroupName</span></span>
<span data-ttu-id="32cd2-152">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="32cd2-152">The name of the resource group to get.</span></span>
<span data-ttu-id="32cd2-153">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="32cd2-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="32cd2-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32cd2-154">-SubscriptionId</span></span>
<span data-ttu-id="32cd2-155">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32cd2-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="32cd2-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="32cd2-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32cd2-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="32cd2-157">-Tag</span></span>
<span data-ttu-id="32cd2-158">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="32cd2-158">Resource tags</span></span>

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

### <span data-ttu-id="32cd2-159">-Digitare</span><span class="sxs-lookup"><span data-stu-id="32cd2-159">-Type</span></span>
<span data-ttu-id="32cd2-160">Tipo di soluzione da creare.</span><span class="sxs-lookup"><span data-stu-id="32cd2-160">Type of the solution to be created.</span></span>
<span data-ttu-id="32cd2-161">Ad esempio "container".</span><span class="sxs-lookup"><span data-stu-id="32cd2-161">For example "Container".</span></span>

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

### <span data-ttu-id="32cd2-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="32cd2-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="32cd2-163">ID delle risorse di Azure per l'area di lavoro in cui verrà distribuita/abilitata la soluzione.</span><span class="sxs-lookup"><span data-stu-id="32cd2-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="32cd2-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32cd2-164">-Confirm</span></span>
<span data-ttu-id="32cd2-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32cd2-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32cd2-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32cd2-166">-WhatIf</span></span>
<span data-ttu-id="32cd2-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32cd2-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32cd2-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32cd2-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32cd2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cd2-169">CommonParameters</span></span>
<span data-ttu-id="32cd2-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cd2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cd2-171">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32cd2-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cd2-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32cd2-172">INPUTS</span></span>

## <span data-ttu-id="32cd2-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32cd2-173">OUTPUTS</span></span>

### <span data-ttu-id="32cd2-174">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="32cd2-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="32cd2-175">Note</span><span class="sxs-lookup"><span data-stu-id="32cd2-175">NOTES</span></span>

<span data-ttu-id="32cd2-176">ALIAS</span><span class="sxs-lookup"><span data-stu-id="32cd2-176">ALIASES</span></span>

## <span data-ttu-id="32cd2-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32cd2-177">RELATED LINKS</span></span>



[<span data-ttu-id="32cd2-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="32cd2-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

