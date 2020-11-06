---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490585"
---
# <span data-ttu-id="6c3bf-101">Modulo AzureRM. Insights</span><span class="sxs-lookup"><span data-stu-id="6c3bf-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="6c3bf-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c3bf-102">Description</span></span>
<span data-ttu-id="6c3bf-103">In questo argomento vengono visualizzati gli argomenti della Guida relativi ai cmdlet Azure Insights.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="6c3bf-104">Cmdlet AzureRM. Insights</span><span class="sxs-lookup"><span data-stu-id="6c3bf-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="6c3bf-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c3bf-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="6c3bf-106">Crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="6c3bf-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="6c3bf-108">Aggiunge o sostituisce una regola di avviso del log.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="6c3bf-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c3bf-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="6c3bf-110">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-110">Creates a new activity log profile.</span></span> <span data-ttu-id="6c3bf-111">Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="6c3bf-112">Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="6c3bf-113">Potrebbe essere di tipo ARM o Classic.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="6c3bf-114">Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="6c3bf-115">Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="6c3bf-116">**Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="6c3bf-117">Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="6c3bf-118">Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale".</span><span class="sxs-lookup"><span data-stu-id="6c3bf-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="6c3bf-119">Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="6c3bf-120">Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="6c3bf-121">Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="6c3bf-122">**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.**</span><span class="sxs-lookup"><span data-stu-id="6c3bf-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="6c3bf-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="6c3bf-124">Aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="6c3bf-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="6c3bf-126">Aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="6c3bf-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c3bf-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="6c3bf-128">Disabilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="6c3bf-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c3bf-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="6c3bf-130">Abilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="6c3bf-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c3bf-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="6c3bf-132">Ottiene i gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-132">Gets action group(s).</span></span>

### [<span data-ttu-id="6c3bf-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c3bf-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="6c3bf-134">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="6c3bf-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6c3bf-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="6c3bf-136">Ottiene la cronologia degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="6c3bf-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="6c3bf-138">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-138">Gets alert rules.</span></span>

### [<span data-ttu-id="6c3bf-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="6c3bf-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="6c3bf-140">Ottiene la cronologia di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="6c3bf-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c3bf-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="6c3bf-142">Ottiene le impostazioni di scalabilità orizzontale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="6c3bf-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6c3bf-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="6c3bf-144">Ottiene le categorie registrate e i grani temporali.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="6c3bf-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="6c3bf-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="6c3bf-146">Ottiene un log di eventi.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-146">Gets a log of events.</span></span>

### [<span data-ttu-id="6c3bf-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c3bf-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="6c3bf-148">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-148">Gets a log profile.</span></span>

### [<span data-ttu-id="6c3bf-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="6c3bf-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="6c3bf-150">Ottiene i valori metrici di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="6c3bf-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6c3bf-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="6c3bf-152">Ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="6c3bf-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="6c3bf-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="6c3bf-154">Ottiene le metriche di utilizzo per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="6c3bf-155">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c3bf-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="6c3bf-156">Crea un oggetto di riferimento ActionGroup in memoria.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="6c3bf-157">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="6c3bf-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="6c3bf-158">Crea un nuovo destinatario del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="6c3bf-159">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6c3bf-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="6c3bf-160">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="6c3bf-161">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6c3bf-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="6c3bf-162">Crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="6c3bf-163">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6c3bf-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="6c3bf-164">Crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="6c3bf-165">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="6c3bf-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="6c3bf-166">Crea una notifica tramite posta elettronica di scala.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="6c3bf-167">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="6c3bf-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="6c3bf-168">Crea un profilo di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="6c3bf-169">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="6c3bf-170">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="6c3bf-171">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="6c3bf-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="6c3bf-172">Crea un webhook di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="6c3bf-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c3bf-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="6c3bf-174">Rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-174">Removes an action group.</span></span>

### [<span data-ttu-id="6c3bf-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c3bf-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="6c3bf-176">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="6c3bf-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c3bf-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="6c3bf-178">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="6c3bf-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c3bf-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="6c3bf-180">Rimuove un'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="6c3bf-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c3bf-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="6c3bf-182">Rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-182">Removes a log profile.</span></span>

### [<span data-ttu-id="6c3bf-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c3bf-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="6c3bf-184">Crea un nuovo o aggiorna un gruppo di azioni esistente.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="6c3bf-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c3bf-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="6c3bf-186">Crea un nuovo o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="6c3bf-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6c3bf-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="6c3bf-188">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6c3bf-188">Sets the logs and metrics settings for the resource.</span></span>

