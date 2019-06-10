---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 6171bab74aec6785938cad54d584f425ddbb850e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2019
ms.locfileid: "65971904"
---
## <a name="180---april-2019"></a><span data-ttu-id="7d8a1-101">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d8a1-102">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-102">Highlights since the last major release</span></span>
* <span data-ttu-id="7d8a1-103">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-103">General availability of `Az` module</span></span>
* <span data-ttu-id="7d8a1-104">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d8a1-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d8a1-105">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d8a1-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d8a1-106">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d8a1-107">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d8a1-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d8a1-108">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d8a1-109">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="7d8a1-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-110">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-111">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="7d8a1-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7d8a1-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d8a1-112">Az.Batch</span></span>
* <span data-ttu-id="7d8a1-113">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d8a1-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d8a1-114">Az.Cdn</span></span>
* <span data-ttu-id="7d8a1-115">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d8a1-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d8a1-117">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-118">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-119">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="7d8a1-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7d8a1-120">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-121">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d8a1-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d8a1-122">Az.DataFactory</span></span>
* <span data-ttu-id="7d8a1-123">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-125">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d8a1-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d8a1-126">Az.EventGrid</span></span>
* <span data-ttu-id="7d8a1-127">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d8a1-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-128">Az.EventHub</span></span>
* <span data-ttu-id="7d8a1-129">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7d8a1-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7d8a1-130">Az.HDInsight</span></span>
* <span data-ttu-id="7d8a1-131">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d8a1-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-132">Az.IotHub</span></span>
* <span data-ttu-id="7d8a1-133">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d8a1-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-134">Az.KeyVault</span></span>
* <span data-ttu-id="7d8a1-135">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-136">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7d8a1-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7d8a1-137">Az.MachineLearning</span></span>
* <span data-ttu-id="7d8a1-138">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7d8a1-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7d8a1-139">Az.Media</span></span>
* <span data-ttu-id="7d8a1-140">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d8a1-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d8a1-141">Az.Monitor</span></span>
  * <span data-ttu-id="7d8a1-142">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7d8a1-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7d8a1-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7d8a1-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7d8a1-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7d8a1-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7d8a1-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7d8a1-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7d8a1-148">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="7d8a1-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-149">Az.Network</span></span>
* <span data-ttu-id="7d8a1-150">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-151">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7d8a1-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7d8a1-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="7d8a1-153">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d8a1-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d8a1-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d8a1-155">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7d8a1-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7d8a1-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7d8a1-157">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d8a1-159">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-160">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7d8a1-161">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="7d8a1-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7d8a1-162">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="7d8a1-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d8a1-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d8a1-163">Az.RedisCache</span></span>
* <span data-ttu-id="7d8a1-164">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-165">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-166">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-167">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-168">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="7d8a1-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7d8a1-169">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-170">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7d8a1-171">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7d8a1-172">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7d8a1-173">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7d8a1-174">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-175">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-176">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7d8a1-177">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d8a1-178">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7d8a1-179">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7d8a1-180">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d8a1-181">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-181">Highlights since the last major release</span></span>
* <span data-ttu-id="7d8a1-182">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-182">General availability of `Az` module</span></span>
* <span data-ttu-id="7d8a1-183">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d8a1-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d8a1-184">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d8a1-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d8a1-185">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d8a1-186">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d8a1-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d8a1-187">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d8a1-188">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="7d8a1-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-189">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-190">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8a1-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d8a1-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d8a1-192">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7d8a1-193">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d8a1-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-194">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-195">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7d8a1-196">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7d8a1-197">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-198">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-199">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7d8a1-200">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7d8a1-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="7d8a1-202">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="7d8a1-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d8a1-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d8a1-203">Az.DataFactory</span></span>
* <span data-ttu-id="7d8a1-204">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7d8a1-205">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-206">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-207">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7d8a1-208">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-208">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7d8a1-209">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="7d8a1-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7d8a1-210">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7d8a1-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7d8a1-211">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7d8a1-212">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7d8a1-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-213">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-214">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d8a1-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-215">Az.Storage</span></span>
* <span data-ttu-id="7d8a1-216">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="7d8a1-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7d8a1-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d8a1-217">New-AzStorageContext</span></span>
* <span data-ttu-id="7d8a1-218">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7d8a1-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7d8a1-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7d8a1-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7d8a1-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7d8a1-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7d8a1-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7d8a1-223">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="7d8a1-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7d8a1-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d8a1-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7d8a1-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d8a1-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7d8a1-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d8a1-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7d8a1-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d8a1-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7d8a1-228">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d8a1-229">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-229">Highlights since the last major release</span></span>
* <span data-ttu-id="7d8a1-230">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-230">General availability of `Az` module</span></span>
* <span data-ttu-id="7d8a1-231">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d8a1-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d8a1-232">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d8a1-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d8a1-233">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d8a1-234">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d8a1-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d8a1-235">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d8a1-236">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="7d8a1-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d8a1-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-237">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-238">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d8a1-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7d8a1-239">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="7d8a1-239">Dynamic grouping</span></span>
    * <span data-ttu-id="7d8a1-240">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="7d8a1-240">Pre-Post script</span></span>
    * <span data-ttu-id="7d8a1-241">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="7d8a1-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-242">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-243">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7d8a1-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7d8a1-244">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d8a1-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-245">Az.KeyVault</span></span>
* <span data-ttu-id="7d8a1-246">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-247">Az.Network</span></span>
* <span data-ttu-id="7d8a1-248">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7d8a1-249">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="7d8a1-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d8a1-251">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="7d8a1-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7d8a1-252">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="7d8a1-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-253">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-254">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d8a1-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7d8a1-255">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="7d8a1-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-256">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-257">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d8a1-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-258">Az.Storage</span></span>
* <span data-ttu-id="7d8a1-259">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7d8a1-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d8a1-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d8a1-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d8a1-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7d8a1-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7d8a1-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7d8a1-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7d8a1-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7d8a1-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-266">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-267">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="7d8a1-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7d8a1-268">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-269">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-270">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="7d8a1-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7d8a1-271">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7d8a1-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d8a1-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-272">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-273">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7d8a1-274">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7d8a1-275">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d8a1-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d8a1-276">Az.Cdn</span></span>
* <span data-ttu-id="7d8a1-277">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="7d8a1-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-278">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-279">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="7d8a1-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d8a1-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d8a1-280">Az.DataFactory</span></span>
* <span data-ttu-id="7d8a1-281">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="7d8a1-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d8a1-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d8a1-282">Az.LogicApp</span></span>
* <span data-ttu-id="7d8a1-283">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="7d8a1-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-284">Az.Network</span></span>
* <span data-ttu-id="7d8a1-285">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d8a1-287">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7d8a1-288">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="7d8a1-288">SDK Update</span></span>
* <span data-ttu-id="7d8a1-289">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d8a1-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7d8a1-290">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d8a1-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-291">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-292">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7d8a1-293">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7d8a1-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7d8a1-294">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7d8a1-295">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7d8a1-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7d8a1-296">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7d8a1-297">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7d8a1-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-298">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-299">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7d8a1-300">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d8a1-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-301">Az.Storage</span></span>
* <span data-ttu-id="7d8a1-302">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d8a1-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7d8a1-303">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7d8a1-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d8a1-305">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="7d8a1-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d8a1-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-306">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-307">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7d8a1-308">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7d8a1-309">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d8a1-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d8a1-311">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-312">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-313">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="7d8a1-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7d8a1-314">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="7d8a1-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7d8a1-315">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7d8a1-316">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-318">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="7d8a1-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d8a1-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-319">Az.EventHub</span></span>
* <span data-ttu-id="7d8a1-320">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7d8a1-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-321">Az.KeyVault</span></span>
* <span data-ttu-id="7d8a1-322">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d8a1-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d8a1-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d8a1-323">Az.LogicApp</span></span>
* <span data-ttu-id="7d8a1-324">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7d8a1-325">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="7d8a1-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7d8a1-326">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7d8a1-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d8a1-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d8a1-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d8a1-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d8a1-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7d8a1-331">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7d8a1-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d8a1-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d8a1-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d8a1-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7d8a1-336">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7d8a1-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d8a1-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d8a1-337">Az.Monitor</span></span>
* <span data-ttu-id="7d8a1-338">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="7d8a1-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-339">Az.Network</span></span>
* <span data-ttu-id="7d8a1-340">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d8a1-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d8a1-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d8a1-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d8a1-342">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7d8a1-343">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7d8a1-344">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7d8a1-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-345">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-346">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7d8a1-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7d8a1-347">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7d8a1-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7d8a1-348">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7d8a1-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7d8a1-349">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="7d8a1-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-350">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-351">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="7d8a1-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7d8a1-352">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="7d8a1-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-353">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-354">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="7d8a1-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7d8a1-355">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-356">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-357">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d8a1-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d8a1-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-358">Az.AnalysisServices</span></span>
<span data-ttu-id="7d8a1-359">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-360">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-361">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="7d8a1-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7d8a1-362">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7d8a1-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7d8a1-363">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-364">Az.RecoveryServices</span></span>
<span data-ttu-id="7d8a1-365">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-366">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-367">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="7d8a1-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7d8a1-368">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7d8a1-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7d8a1-369">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="7d8a1-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7d8a1-370">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7d8a1-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-371">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-372">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7d8a1-373">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="7d8a1-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7d8a1-374">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="7d8a1-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7d8a1-375">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-376">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-377">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d8a1-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d8a1-379">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d8a1-381">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7d8a1-382">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-383">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-384">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d8a1-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d8a1-385">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d8a1-386">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="7d8a1-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7d8a1-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7d8a1-387">Az.Aks</span></span>
* <span data-ttu-id="7d8a1-388">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d8a1-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-389">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-390">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7d8a1-391">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d8a1-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d8a1-392">Az.Cdn</span></span>
* <span data-ttu-id="7d8a1-393">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-394">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-395">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7d8a1-396">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d8a1-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7d8a1-397">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d8a1-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7d8a1-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7d8a1-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7d8a1-399">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d8a1-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d8a1-400">Az.DataFactory</span></span>
* <span data-ttu-id="7d8a1-401">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="7d8a1-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-403">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="7d8a1-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7d8a1-404">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7d8a1-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7d8a1-405">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d8a1-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-406">Az.IotHub</span></span>
* <span data-ttu-id="7d8a1-407">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d8a1-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-408">Az.KeyVault</span></span>
* <span data-ttu-id="7d8a1-409">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-410">Az.Network</span></span>
* <span data-ttu-id="7d8a1-411">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-412">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-413">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="7d8a1-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7d8a1-414">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7d8a1-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7d8a1-415">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="7d8a1-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7d8a1-416">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7d8a1-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7d8a1-417">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7d8a1-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7d8a1-418">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="7d8a1-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7d8a1-419">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7d8a1-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d8a1-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d8a1-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d8a1-421">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7d8a1-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7d8a1-422">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-422">Fix some error messages.</span></span>
* <span data-ttu-id="7d8a1-423">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7d8a1-424">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7d8a1-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7d8a1-425">Az.SignalR</span></span>
* <span data-ttu-id="7d8a1-426">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-427">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-428">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d8a1-429">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="7d8a1-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7d8a1-430">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="7d8a1-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7d8a1-431">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="7d8a1-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d8a1-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-432">Az.Storage</span></span>
* <span data-ttu-id="7d8a1-433">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d8a1-434">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7d8a1-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7d8a1-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7d8a1-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7d8a1-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7d8a1-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7d8a1-437">Az.TrafficManager</span></span>
* <span data-ttu-id="7d8a1-438">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-439">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-440">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="7d8a1-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d8a1-441">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7d8a1-442">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="7d8a1-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7d8a1-443">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="7d8a1-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d8a1-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-444">Az.Accounts</span></span>
* <span data-ttu-id="7d8a1-445">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="7d8a1-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-446">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-447">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7d8a1-448">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="7d8a1-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7d8a1-449">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-451">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7d8a1-452">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="7d8a1-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d8a1-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d8a1-453">Az.EventGrid</span></span>
* <span data-ttu-id="7d8a1-454">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7d8a1-455">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7d8a1-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7d8a1-456">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="7d8a1-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7d8a1-457">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="7d8a1-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7d8a1-458">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7d8a1-459">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="7d8a1-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7d8a1-460">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="7d8a1-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7d8a1-461">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="7d8a1-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7d8a1-462">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7d8a1-463">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="7d8a1-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="7d8a1-464">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7d8a1-465">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d8a1-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-466">Az.IotHub</span></span>
* <span data-ttu-id="7d8a1-467">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="7d8a1-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d8a1-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d8a1-468">Az.LogicApp</span></span>
* <span data-ttu-id="7d8a1-469">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="7d8a1-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-470">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-471">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7d8a1-472">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7d8a1-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7d8a1-473">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d8a1-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7d8a1-474">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7d8a1-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7d8a1-475">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7d8a1-476">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7d8a1-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7d8a1-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7d8a1-477">Az.SignalR</span></span>
* <span data-ttu-id="7d8a1-478">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-479">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-480">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d8a1-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-481">Az.Storage</span></span>
* <span data-ttu-id="7d8a1-482">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="7d8a1-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7d8a1-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d8a1-483">New-AzStorageContext</span></span>
* <span data-ttu-id="7d8a1-484">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="7d8a1-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7d8a1-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7d8a1-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-486">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-487">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7d8a1-488">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7d8a1-489">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7d8a1-490">Generale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-490">General</span></span>

- <span data-ttu-id="7d8a1-491">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="7d8a1-491">General Availability of Az Module</span></span>
- <span data-ttu-id="7d8a1-492">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="7d8a1-492">Online help for each module</span></span>
- <span data-ttu-id="7d8a1-493">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7d8a1-494">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="7d8a1-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7d8a1-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-495">Az.Accounts</span></span>
- <span data-ttu-id="7d8a1-496">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="7d8a1-497">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="7d8a1-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7d8a1-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d8a1-498">Az.ApiManagement</span></span>
- <span data-ttu-id="7d8a1-499">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="7d8a1-499">Fixes for #7002</span></span>
- <span data-ttu-id="7d8a1-500">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7d8a1-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d8a1-501">Az.Batch</span></span>
- <span data-ttu-id="7d8a1-502">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7d8a1-503">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7d8a1-504">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7d8a1-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7d8a1-505">Az.Billing</span></span>
- <span data-ttu-id="7d8a1-506">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7d8a1-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-507">Az.CognitivServices</span></span>
- <span data-ttu-id="7d8a1-508">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7d8a1-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7d8a1-509">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7d8a1-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7d8a1-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="7d8a1-511">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d8a1-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7d8a1-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7d8a1-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7d8a1-513">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="7d8a1-515">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7d8a1-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d8a1-516">Az.Monitor</span></span>
- <span data-ttu-id="7d8a1-517">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7d8a1-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d8a1-518">Az.KeyVault</span></span>
- <span data-ttu-id="7d8a1-519">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="7d8a1-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7d8a1-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7d8a1-520">Az.MachineLearning</span></span>
- <span data-ttu-id="7d8a1-521">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7d8a1-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7d8a1-522">Az.Media</span></span>
- <span data-ttu-id="7d8a1-523">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d8a1-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7d8a1-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-524">Az.Network</span></span>
<span data-ttu-id="7d8a1-525">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7d8a1-526">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="7d8a1-526">New cmdlets added:</span></span>
        - <span data-ttu-id="7d8a1-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7d8a1-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7d8a1-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7d8a1-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d8a1-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7d8a1-535">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7d8a1-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d8a1-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7d8a1-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7d8a1-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7d8a1-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7d8a1-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7d8a1-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7d8a1-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7d8a1-541">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7d8a1-542">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d8a1-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7d8a1-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d8a1-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7d8a1-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d8a1-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7d8a1-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d8a1-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7d8a1-546">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d8a1-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7d8a1-547">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7d8a1-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d8a1-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="7d8a1-549">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7d8a1-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-550">Az.Profile</span></span>
- <span data-ttu-id="7d8a1-551">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d8a1-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="7d8a1-553">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7d8a1-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-554">Az.Resources</span></span>
- <span data-ttu-id="7d8a1-555">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7d8a1-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d8a1-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="7d8a1-557">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7d8a1-558">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7d8a1-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7d8a1-559">Az.SIgnalR</span></span>
- <span data-ttu-id="7d8a1-560">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7d8a1-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7d8a1-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-561">Az.Sql</span></span>
- <span data-ttu-id="7d8a1-562">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="7d8a1-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7d8a1-563">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7d8a1-564">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7d8a1-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-565">Az.Storage</span></span>
- <span data-ttu-id="7d8a1-566">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7d8a1-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-567">Az.Websites</span></span>
- <span data-ttu-id="7d8a1-568">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7d8a1-569">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7d8a1-570">Generale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-570">General</span></span>

* <span data-ttu-id="7d8a1-571">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="7d8a1-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7d8a1-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-572">Az.Compute</span></span>

* <span data-ttu-id="7d8a1-573">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="7d8a1-575">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="7d8a1-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7d8a1-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d8a1-576">Az.FrontDoor</span></span>

* <span data-ttu-id="7d8a1-577">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="7d8a1-577">Fixed some broken links</span></span>
    - <span data-ttu-id="7d8a1-578">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7d8a1-579">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7d8a1-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="7d8a1-581">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7d8a1-582">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7d8a1-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-583">Az.Resources</span></span>

* <span data-ttu-id="7d8a1-584">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7d8a1-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7d8a1-585">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7d8a1-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-586">Az.Sql</span></span>

* <span data-ttu-id="7d8a1-587">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="7d8a1-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7d8a1-588">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="7d8a1-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7d8a1-589">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7d8a1-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-590">Az.Storage</span></span>

* <span data-ttu-id="7d8a1-591">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d8a1-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7d8a1-592">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="7d8a1-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7d8a1-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7d8a1-594">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="7d8a1-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="7d8a1-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7d8a1-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7d8a1-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7d8a1-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7d8a1-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-597">Az.Websites</span></span>

* <span data-ttu-id="7d8a1-598">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7d8a1-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7d8a1-599">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7d8a1-600">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7d8a1-601">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7d8a1-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d8a1-602">Az.ApiManagement</span></span>
* <span data-ttu-id="7d8a1-603">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7d8a1-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d8a1-604">Az.Automation</span></span>
* <span data-ttu-id="7d8a1-605">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="7d8a1-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7d8a1-606">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="7d8a1-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7d8a1-607">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="7d8a1-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7d8a1-608">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7d8a1-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7d8a1-609">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="7d8a1-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7d8a1-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-610">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-611">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7d8a1-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7d8a1-612">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7d8a1-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="7d8a1-614">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7d8a1-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7d8a1-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7d8a1-616">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="7d8a1-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7d8a1-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-617">Az.Network</span></span>
* <span data-ttu-id="7d8a1-618">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7d8a1-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7d8a1-619">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="7d8a1-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7d8a1-620">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7d8a1-621">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d8a1-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7d8a1-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7d8a1-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7d8a1-623">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7d8a1-624">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7d8a1-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7d8a1-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7d8a1-626">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d8a1-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7d8a1-627">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="7d8a1-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7d8a1-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7d8a1-628">Az.Relay</span></span>
* <span data-ttu-id="7d8a1-629">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7d8a1-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-630">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-631">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="7d8a1-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7d8a1-632">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="7d8a1-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7d8a1-633">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7d8a1-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7d8a1-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d8a1-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d8a1-635">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7d8a1-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-636">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-637">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="7d8a1-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7d8a1-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d8a1-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d8a1-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d8a1-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d8a1-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d8a1-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d8a1-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d8a1-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d8a1-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d8a1-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d8a1-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d8a1-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d8a1-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7d8a1-646">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7d8a1-647">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7d8a1-648">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7d8a1-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7d8a1-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7d8a1-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7d8a1-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7d8a1-653">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7d8a1-654">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7d8a1-655">Generale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-655">General</span></span>
* <span data-ttu-id="7d8a1-656">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="7d8a1-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7d8a1-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-657">Az.Profile</span></span>
* <span data-ttu-id="7d8a1-658">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d8a1-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7d8a1-659">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="7d8a1-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7d8a1-660">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7d8a1-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7d8a1-661">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="7d8a1-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7d8a1-662">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="7d8a1-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7d8a1-663">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="7d8a1-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7d8a1-664">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="7d8a1-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d8a1-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d8a1-666">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-667">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-668">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d8a1-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7d8a1-669">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7d8a1-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7d8a1-670">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-672">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7d8a1-673">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7d8a1-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7d8a1-674">Az.Insights</span></span>
* <span data-ttu-id="7d8a1-675">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="7d8a1-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7d8a1-676">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="7d8a1-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7d8a1-677">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7d8a1-678">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="7d8a1-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-679">Az.Network</span></span>
* <span data-ttu-id="7d8a1-680">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d8a1-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7d8a1-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d8a1-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7d8a1-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7d8a1-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7d8a1-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d8a1-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7d8a1-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7d8a1-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7d8a1-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d8a1-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7d8a1-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d8a1-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7d8a1-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7d8a1-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="7d8a1-688">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="7d8a1-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-689">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-690">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7d8a1-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7d8a1-691">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d8a1-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d8a1-692">Az.ServiceBus</span></span>
* <span data-ttu-id="7d8a1-693">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d8a1-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d8a1-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d8a1-695">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7d8a1-696">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7d8a1-697">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7d8a1-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7d8a1-698">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7d8a1-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7d8a1-699">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7d8a1-700">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7d8a1-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-701">Az.Profile</span></span>
* <span data-ttu-id="7d8a1-702">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="7d8a1-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7d8a1-703">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d8a1-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-704">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-705">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="7d8a1-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7d8a1-706">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d8a1-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d8a1-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d8a1-708">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7d8a1-709">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7d8a1-710">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7d8a1-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7d8a1-712">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-713">Az.Network</span></span>
* <span data-ttu-id="7d8a1-714">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7d8a1-715">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-716">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-717">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7d8a1-718">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7d8a1-719">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7d8a1-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-720">Azure.Storage</span></span>
* <span data-ttu-id="7d8a1-721">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="7d8a1-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7d8a1-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7d8a1-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7d8a1-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7d8a1-724">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="7d8a1-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7d8a1-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7d8a1-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7d8a1-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d8a1-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d8a1-727">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d8a1-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d8a1-728">Az.Compute</span></span>
* <span data-ttu-id="7d8a1-729">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="7d8a1-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7d8a1-730">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7d8a1-731">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="7d8a1-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7d8a1-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7d8a1-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7d8a1-733">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="7d8a1-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d8a1-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d8a1-734">Az.Network</span></span>
* <span data-ttu-id="7d8a1-735">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7d8a1-736">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-736">new cmdlets added</span></span>
    - <span data-ttu-id="7d8a1-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d8a1-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d8a1-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d8a1-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a1-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d8a1-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7d8a1-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7d8a1-743">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="7d8a1-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7d8a1-744">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7d8a1-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7d8a1-745">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a1-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d8a1-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d8a1-746">Az.RedisCache</span></span>
* <span data-ttu-id="7d8a1-747">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="7d8a1-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7d8a1-748">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="7d8a1-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d8a1-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d8a1-749">Az.Resources</span></span>
* <span data-ttu-id="7d8a1-750">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d8a1-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7d8a1-751">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="7d8a1-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d8a1-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d8a1-752">Az.Sql</span></span>
* <span data-ttu-id="7d8a1-753">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="7d8a1-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d8a1-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d8a1-754">Az.Websites</span></span>
* <span data-ttu-id="7d8a1-755">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="7d8a1-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7d8a1-756">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="7d8a1-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7d8a1-757">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="7d8a1-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7d8a1-758">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="7d8a1-758">Initial Release</span></span>