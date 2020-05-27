---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386970"
---
## <a name="180---april-2019"></a><span data-ttu-id="63925-103">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="63925-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="63925-104">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="63925-104">Highlights since the last major release</span></span>
* <span data-ttu-id="63925-105">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="63925-105">General availability of `Az` module</span></span>
* <span data-ttu-id="63925-106">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="63925-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="63925-107">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="63925-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="63925-108">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="63925-109">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="63925-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="63925-110">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="63925-111">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="63925-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="63925-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-112">Az.Accounts</span></span>
* <span data-ttu-id="63925-113">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="63925-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="63925-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="63925-114">Az.Batch</span></span>
* <span data-ttu-id="63925-115">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="63925-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="63925-116">Az.Cdn</span></span>
* <span data-ttu-id="63925-117">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="63925-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="63925-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="63925-119">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-120">Az.Compute</span></span>
* <span data-ttu-id="63925-121">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="63925-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="63925-122">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-123">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="63925-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="63925-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="63925-124">Az.DataFactory</span></span>
* <span data-ttu-id="63925-125">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="63925-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-127">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="63925-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="63925-128">Az.EventGrid</span></span>
* <span data-ttu-id="63925-129">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="63925-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="63925-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="63925-130">Az.EventHub</span></span>
* <span data-ttu-id="63925-131">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="63925-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="63925-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="63925-132">Az.HDInsight</span></span>
* <span data-ttu-id="63925-133">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="63925-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="63925-134">Az.IotHub</span></span>
* <span data-ttu-id="63925-135">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="63925-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-136">Az.KeyVault</span></span>
* <span data-ttu-id="63925-137">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-138">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="63925-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="63925-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="63925-139">Az.MachineLearning</span></span>
* <span data-ttu-id="63925-140">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="63925-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="63925-141">Az.Media</span></span>
* <span data-ttu-id="63925-142">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="63925-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="63925-143">Az.Monitor</span></span>
  * <span data-ttu-id="63925-144">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="63925-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="63925-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="63925-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="63925-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="63925-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="63925-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="63925-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="63925-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="63925-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="63925-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="63925-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="63925-150">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="63925-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-151">Az.Network</span></span>
* <span data-ttu-id="63925-152">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-153">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="63925-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="63925-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="63925-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="63925-155">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="63925-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="63925-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="63925-157">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="63925-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="63925-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="63925-159">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="63925-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="63925-161">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-162">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="63925-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="63925-163">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="63925-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="63925-164">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="63925-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="63925-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="63925-165">Az.RedisCache</span></span>
* <span data-ttu-id="63925-166">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-167">Az.Resources</span></span>
* <span data-ttu-id="63925-168">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="63925-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-169">Az.Sql</span></span>
* <span data-ttu-id="63925-170">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="63925-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="63925-171">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-172">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="63925-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="63925-173">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="63925-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="63925-174">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="63925-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="63925-175">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="63925-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="63925-176">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="63925-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-177">Az.Websites</span></span>
* <span data-ttu-id="63925-178">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="63925-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="63925-179">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="63925-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="63925-180">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="63925-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="63925-181">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="63925-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="63925-182">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="63925-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="63925-183">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="63925-183">Highlights since the last major release</span></span>
* <span data-ttu-id="63925-184">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="63925-184">General availability of `Az` module</span></span>
* <span data-ttu-id="63925-185">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="63925-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="63925-186">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="63925-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="63925-187">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="63925-188">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="63925-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="63925-189">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="63925-190">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="63925-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="63925-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-191">Az.Accounts</span></span>
* <span data-ttu-id="63925-192">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="63925-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="63925-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="63925-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="63925-194">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="63925-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="63925-195">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="63925-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="63925-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-196">Az.Automation</span></span>
* <span data-ttu-id="63925-197">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="63925-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="63925-198">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="63925-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="63925-199">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="63925-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-200">Az.Compute</span></span>
* <span data-ttu-id="63925-201">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="63925-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="63925-202">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="63925-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="63925-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="63925-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="63925-204">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="63925-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="63925-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="63925-205">Az.DataFactory</span></span>
* <span data-ttu-id="63925-206">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="63925-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="63925-207">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="63925-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-208">Az.Resources</span></span>
* <span data-ttu-id="63925-209">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="63925-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="63925-210">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="63925-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="63925-211">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="63925-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="63925-212">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="63925-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="63925-213">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="63925-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="63925-214">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="63925-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-215">Az.Sql</span></span>
* <span data-ttu-id="63925-216">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="63925-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="63925-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-217">Az.Storage</span></span>
* <span data-ttu-id="63925-218">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="63925-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="63925-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="63925-219">New-AzStorageContext</span></span>
* <span data-ttu-id="63925-220">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="63925-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="63925-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="63925-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="63925-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="63925-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="63925-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="63925-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="63925-225">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="63925-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="63925-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63925-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="63925-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63925-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="63925-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="63925-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="63925-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="63925-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="63925-230">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="63925-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="63925-231">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="63925-231">Highlights since the last major release</span></span>
* <span data-ttu-id="63925-232">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="63925-232">General availability of `Az` module</span></span>
* <span data-ttu-id="63925-233">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="63925-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="63925-234">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="63925-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="63925-235">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="63925-236">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="63925-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="63925-237">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="63925-238">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="63925-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="63925-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-239">Az.Automation</span></span>
* <span data-ttu-id="63925-240">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="63925-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="63925-241">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="63925-241">Dynamic grouping</span></span>
    * <span data-ttu-id="63925-242">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="63925-242">Pre-Post script</span></span>
    * <span data-ttu-id="63925-243">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="63925-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-244">Az.Compute</span></span>
* <span data-ttu-id="63925-245">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="63925-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="63925-246">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="63925-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="63925-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-247">Az.KeyVault</span></span>
* <span data-ttu-id="63925-248">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-249">Az.Network</span></span>
* <span data-ttu-id="63925-250">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="63925-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="63925-251">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="63925-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="63925-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="63925-253">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="63925-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="63925-254">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="63925-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-255">Az.Resources</span></span>
* <span data-ttu-id="63925-256">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="63925-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="63925-257">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="63925-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-258">Az.Sql</span></span>
* <span data-ttu-id="63925-259">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="63925-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="63925-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-260">Az.Storage</span></span>
* <span data-ttu-id="63925-261">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="63925-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="63925-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="63925-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="63925-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="63925-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="63925-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="63925-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="63925-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="63925-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="63925-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-268">Az.Websites</span></span>
* <span data-ttu-id="63925-269">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="63925-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="63925-270">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="63925-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="63925-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-271">Az.Accounts</span></span>
* <span data-ttu-id="63925-272">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="63925-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="63925-273">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="63925-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="63925-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-274">Az.Automation</span></span>
* <span data-ttu-id="63925-275">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="63925-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="63925-276">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="63925-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="63925-277">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="63925-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="63925-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="63925-278">Az.Cdn</span></span>
* <span data-ttu-id="63925-279">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="63925-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-280">Az.Compute</span></span>
* <span data-ttu-id="63925-281">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="63925-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="63925-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="63925-282">Az.DataFactory</span></span>
* <span data-ttu-id="63925-283">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="63925-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="63925-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="63925-284">Az.LogicApp</span></span>
* <span data-ttu-id="63925-285">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="63925-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-286">Az.Network</span></span>
* <span data-ttu-id="63925-287">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="63925-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="63925-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="63925-289">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="63925-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="63925-290">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="63925-290">SDK Update</span></span>
* <span data-ttu-id="63925-291">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="63925-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="63925-292">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="63925-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-293">Az.Resources</span></span>
* <span data-ttu-id="63925-294">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="63925-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="63925-295">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="63925-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="63925-296">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="63925-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="63925-297">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="63925-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="63925-298">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="63925-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="63925-299">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="63925-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-300">Az.Sql</span></span>
* <span data-ttu-id="63925-301">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="63925-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="63925-302">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="63925-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="63925-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-303">Az.Storage</span></span>
* <span data-ttu-id="63925-304">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63925-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="63925-305">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="63925-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="63925-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="63925-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="63925-307">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="63925-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="63925-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-308">Az.Automation</span></span>
* <span data-ttu-id="63925-309">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="63925-310">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="63925-311">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="63925-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="63925-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="63925-313">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="63925-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-314">Az.Compute</span></span>
* <span data-ttu-id="63925-315">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="63925-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="63925-316">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="63925-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="63925-317">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="63925-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="63925-318">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="63925-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-320">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="63925-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="63925-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="63925-321">Az.EventHub</span></span>
* <span data-ttu-id="63925-322">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="63925-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="63925-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-323">Az.KeyVault</span></span>
* <span data-ttu-id="63925-324">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="63925-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="63925-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="63925-325">Az.LogicApp</span></span>
* <span data-ttu-id="63925-326">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="63925-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="63925-327">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="63925-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="63925-328">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="63925-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="63925-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="63925-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="63925-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="63925-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="63925-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="63925-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="63925-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="63925-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="63925-333">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="63925-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="63925-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="63925-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="63925-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="63925-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="63925-338">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="63925-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="63925-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="63925-339">Az.Monitor</span></span>
* <span data-ttu-id="63925-340">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="63925-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-341">Az.Network</span></span>
* <span data-ttu-id="63925-342">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63925-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="63925-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="63925-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="63925-344">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="63925-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="63925-345">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="63925-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="63925-346">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="63925-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="63925-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-347">Az.Resources</span></span>
* <span data-ttu-id="63925-348">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="63925-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="63925-349">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="63925-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="63925-350">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="63925-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="63925-351">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="63925-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-352">Az.Sql</span></span>
* <span data-ttu-id="63925-353">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="63925-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="63925-354">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="63925-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-355">Az.Websites</span></span>
* <span data-ttu-id="63925-356">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="63925-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="63925-357">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="63925-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="63925-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-358">Az.Accounts</span></span>
* <span data-ttu-id="63925-359">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="63925-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="63925-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="63925-360">Az.AnalysisServices</span></span>
<span data-ttu-id="63925-361">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="63925-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-362">Az.Compute</span></span>
* <span data-ttu-id="63925-363">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="63925-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="63925-364">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="63925-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="63925-365">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="63925-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="63925-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-366">Az.RecoveryServices</span></span>
<span data-ttu-id="63925-367">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="63925-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-368">Az.Resources</span></span>
* <span data-ttu-id="63925-369">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="63925-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="63925-370">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="63925-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="63925-371">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="63925-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="63925-372">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="63925-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-373">Az.Sql</span></span>
* <span data-ttu-id="63925-374">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="63925-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="63925-375">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="63925-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="63925-376">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="63925-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="63925-377">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="63925-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="63925-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-378">Az.Accounts</span></span>
* <span data-ttu-id="63925-379">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="63925-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="63925-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="63925-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="63925-381">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="63925-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="63925-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="63925-383">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="63925-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="63925-384">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="63925-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="63925-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-385">Az.Accounts</span></span>
* <span data-ttu-id="63925-386">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="63925-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="63925-387">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="63925-388">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="63925-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="63925-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="63925-389">Az.Aks</span></span>
* <span data-ttu-id="63925-390">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="63925-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-391">Az.Automation</span></span>
* <span data-ttu-id="63925-392">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="63925-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="63925-393">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="63925-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="63925-394">Az.Cdn</span></span>
* <span data-ttu-id="63925-395">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-396">Az.Compute</span></span>
* <span data-ttu-id="63925-397">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="63925-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="63925-398">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="63925-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="63925-399">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="63925-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="63925-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="63925-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="63925-401">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="63925-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="63925-402">Az.DataFactory</span></span>
* <span data-ttu-id="63925-403">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="63925-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-405">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="63925-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="63925-406">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="63925-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="63925-407">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="63925-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="63925-408">Az.IotHub</span></span>
* <span data-ttu-id="63925-409">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63925-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="63925-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-410">Az.KeyVault</span></span>
* <span data-ttu-id="63925-411">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-412">Az.Network</span></span>
* <span data-ttu-id="63925-413">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-414">Az.Resources</span></span>
* <span data-ttu-id="63925-415">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="63925-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="63925-416">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="63925-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="63925-417">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="63925-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="63925-418">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="63925-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="63925-419">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="63925-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="63925-420">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="63925-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="63925-421">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="63925-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="63925-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="63925-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="63925-423">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="63925-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="63925-424">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="63925-424">Fix some error messages.</span></span>
* <span data-ttu-id="63925-425">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="63925-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="63925-426">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="63925-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="63925-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="63925-427">Az.SignalR</span></span>
* <span data-ttu-id="63925-428">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-429">Az.Sql</span></span>
* <span data-ttu-id="63925-430">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="63925-431">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="63925-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="63925-432">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="63925-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="63925-433">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="63925-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="63925-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-434">Az.Storage</span></span>
* <span data-ttu-id="63925-435">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="63925-436">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="63925-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="63925-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="63925-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="63925-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="63925-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="63925-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="63925-439">Az.TrafficManager</span></span>
* <span data-ttu-id="63925-440">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-441">Az.Websites</span></span>
* <span data-ttu-id="63925-442">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="63925-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="63925-443">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="63925-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="63925-444">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="63925-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="63925-445">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="63925-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="63925-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-446">Az.Accounts</span></span>
* <span data-ttu-id="63925-447">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="63925-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-448">Az.Compute</span></span>
* <span data-ttu-id="63925-449">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="63925-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="63925-450">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="63925-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="63925-451">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-453">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="63925-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="63925-454">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="63925-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="63925-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="63925-455">Az.EventGrid</span></span>
* <span data-ttu-id="63925-456">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="63925-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="63925-457">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="63925-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="63925-458">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="63925-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="63925-459">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="63925-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="63925-460">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="63925-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="63925-461">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="63925-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="63925-462">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="63925-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="63925-463">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="63925-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="63925-464">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="63925-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="63925-465">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="63925-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="63925-466">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="63925-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="63925-467">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="63925-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="63925-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="63925-468">Az.IotHub</span></span>
* <span data-ttu-id="63925-469">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="63925-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="63925-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="63925-470">Az.LogicApp</span></span>
* <span data-ttu-id="63925-471">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="63925-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-472">Az.Resources</span></span>
* <span data-ttu-id="63925-473">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="63925-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="63925-474">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="63925-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="63925-475">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63925-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="63925-476">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="63925-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="63925-477">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="63925-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="63925-478">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="63925-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="63925-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="63925-479">Az.SignalR</span></span>
* <span data-ttu-id="63925-480">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-481">Az.Sql</span></span>
* <span data-ttu-id="63925-482">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="63925-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="63925-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-483">Az.Storage</span></span>
* <span data-ttu-id="63925-484">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="63925-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="63925-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="63925-485">New-AzStorageContext</span></span>
* <span data-ttu-id="63925-486">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="63925-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="63925-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="63925-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-488">Az.Websites</span></span>
* <span data-ttu-id="63925-489">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="63925-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="63925-490">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="63925-491">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="63925-492">Generale</span><span class="sxs-lookup"><span data-stu-id="63925-492">General</span></span>

- <span data-ttu-id="63925-493">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="63925-493">General Availability of Az Module</span></span>
- <span data-ttu-id="63925-494">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="63925-494">Online help for each module</span></span>
- <span data-ttu-id="63925-495">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="63925-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="63925-496">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="63925-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="63925-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-497">Az.Accounts</span></span>
- <span data-ttu-id="63925-498">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="63925-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="63925-499">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="63925-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="63925-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="63925-500">Az.ApiManagement</span></span>
- <span data-ttu-id="63925-501">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="63925-501">Fixes for #7002</span></span>
- <span data-ttu-id="63925-502">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="63925-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="63925-503">Az.Batch</span></span>
- <span data-ttu-id="63925-504">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="63925-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="63925-505">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="63925-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="63925-506">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="63925-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="63925-507">Az.Billing</span></span>
- <span data-ttu-id="63925-508">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="63925-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="63925-509">Az.CognitivServices</span></span>
- <span data-ttu-id="63925-510">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="63925-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="63925-511">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="63925-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="63925-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="63925-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="63925-513">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="63925-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="63925-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="63925-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="63925-515">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="63925-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="63925-517">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="63925-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="63925-518">Az.Monitor</span></span>
- <span data-ttu-id="63925-519">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="63925-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="63925-520">Az.KeyVault</span></span>
- <span data-ttu-id="63925-521">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="63925-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="63925-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="63925-522">Az.MachineLearning</span></span>
- <span data-ttu-id="63925-523">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="63925-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="63925-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="63925-524">Az.Media</span></span>
- <span data-ttu-id="63925-525">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="63925-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="63925-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-526">Az.Network</span></span>
<span data-ttu-id="63925-527">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="63925-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="63925-528">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="63925-528">New cmdlets added:</span></span>
        - <span data-ttu-id="63925-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="63925-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="63925-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="63925-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="63925-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="63925-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="63925-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="63925-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="63925-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="63925-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="63925-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="63925-537">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63925-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="63925-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63925-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="63925-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="63925-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="63925-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="63925-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="63925-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63925-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="63925-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63925-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="63925-543">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="63925-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="63925-544">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="63925-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="63925-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="63925-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="63925-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="63925-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="63925-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="63925-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="63925-548">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="63925-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="63925-549">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="63925-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="63925-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="63925-551">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="63925-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="63925-552">Az.Profile</span></span>
- <span data-ttu-id="63925-553">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="63925-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="63925-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="63925-555">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="63925-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-556">Az.Resources</span></span>
- <span data-ttu-id="63925-557">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="63925-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="63925-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="63925-559">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="63925-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="63925-560">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="63925-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="63925-561">Az.SIgnalR</span></span>
- <span data-ttu-id="63925-562">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="63925-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="63925-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-563">Az.Sql</span></span>
- <span data-ttu-id="63925-564">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="63925-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="63925-565">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="63925-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="63925-566">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="63925-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-567">Az.Storage</span></span>
- <span data-ttu-id="63925-568">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="63925-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-569">Az.Websites</span></span>
- <span data-ttu-id="63925-570">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="63925-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="63925-571">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="63925-572">Generale</span><span class="sxs-lookup"><span data-stu-id="63925-572">General</span></span>

* <span data-ttu-id="63925-573">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="63925-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="63925-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-574">Az.Compute</span></span>

* <span data-ttu-id="63925-575">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="63925-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="63925-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="63925-577">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="63925-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="63925-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="63925-578">Az.FrontDoor</span></span>

* <span data-ttu-id="63925-579">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="63925-579">Fixed some broken links</span></span>
    - <span data-ttu-id="63925-580">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="63925-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="63925-581">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="63925-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="63925-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="63925-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="63925-583">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="63925-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="63925-584">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="63925-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="63925-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-585">Az.Resources</span></span>

* <span data-ttu-id="63925-586">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="63925-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="63925-587">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="63925-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="63925-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-588">Az.Sql</span></span>

* <span data-ttu-id="63925-589">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="63925-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="63925-590">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="63925-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="63925-591">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="63925-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="63925-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-592">Az.Storage</span></span>

* <span data-ttu-id="63925-593">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63925-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="63925-594">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="63925-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="63925-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="63925-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="63925-596">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="63925-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="63925-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="63925-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="63925-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="63925-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="63925-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-599">Az.Websites</span></span>

* <span data-ttu-id="63925-600">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63925-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="63925-601">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="63925-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="63925-602">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="63925-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="63925-603">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="63925-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="63925-604">Az.ApiManagement</span></span>
* <span data-ttu-id="63925-605">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="63925-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="63925-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="63925-606">Az.Automation</span></span>
* <span data-ttu-id="63925-607">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="63925-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="63925-608">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="63925-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="63925-609">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="63925-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="63925-610">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="63925-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="63925-611">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="63925-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="63925-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-612">Az.Compute</span></span>
* <span data-ttu-id="63925-613">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="63925-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="63925-614">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="63925-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="63925-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="63925-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="63925-616">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="63925-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="63925-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="63925-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="63925-618">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="63925-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="63925-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-619">Az.Network</span></span>
* <span data-ttu-id="63925-620">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="63925-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="63925-621">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="63925-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="63925-622">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="63925-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="63925-623">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="63925-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="63925-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="63925-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="63925-625">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="63925-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="63925-626">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="63925-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="63925-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="63925-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="63925-628">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="63925-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="63925-629">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="63925-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="63925-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="63925-630">Az.Relay</span></span>
* <span data-ttu-id="63925-631">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="63925-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="63925-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-632">Az.Resources</span></span>
* <span data-ttu-id="63925-633">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="63925-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="63925-634">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="63925-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="63925-635">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="63925-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="63925-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="63925-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="63925-637">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="63925-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="63925-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-638">Az.Sql</span></span>
* <span data-ttu-id="63925-639">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="63925-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="63925-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="63925-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="63925-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="63925-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="63925-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="63925-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="63925-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="63925-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="63925-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="63925-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="63925-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="63925-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="63925-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="63925-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="63925-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="63925-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="63925-648">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="63925-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="63925-649">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="63925-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="63925-650">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="63925-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="63925-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="63925-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="63925-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="63925-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="63925-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="63925-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="63925-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="63925-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="63925-655">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="63925-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="63925-656">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="63925-657">Generale</span><span class="sxs-lookup"><span data-stu-id="63925-657">General</span></span>
* <span data-ttu-id="63925-658">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="63925-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="63925-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="63925-659">Az.Profile</span></span>
* <span data-ttu-id="63925-660">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="63925-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="63925-661">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="63925-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="63925-662">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="63925-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="63925-663">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="63925-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="63925-664">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="63925-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="63925-665">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="63925-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="63925-666">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="63925-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="63925-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="63925-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="63925-668">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="63925-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-669">Az.Compute</span></span>
* <span data-ttu-id="63925-670">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="63925-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="63925-671">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="63925-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="63925-672">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="63925-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-674">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="63925-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="63925-675">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="63925-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="63925-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="63925-676">Az.Insights</span></span>
* <span data-ttu-id="63925-677">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="63925-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="63925-678">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="63925-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="63925-679">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="63925-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="63925-680">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="63925-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-681">Az.Network</span></span>
* <span data-ttu-id="63925-682">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="63925-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="63925-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="63925-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="63925-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="63925-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="63925-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="63925-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="63925-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="63925-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="63925-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="63925-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="63925-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="63925-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="63925-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="63925-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="63925-690">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="63925-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-691">Az.Resources</span></span>
* <span data-ttu-id="63925-692">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="63925-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="63925-693">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="63925-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="63925-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="63925-694">Az.ServiceBus</span></span>
* <span data-ttu-id="63925-695">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="63925-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="63925-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="63925-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="63925-697">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="63925-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="63925-698">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="63925-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="63925-699">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="63925-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="63925-700">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="63925-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="63925-701">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="63925-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="63925-702">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="63925-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="63925-703">Az.Profile</span></span>
* <span data-ttu-id="63925-704">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="63925-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="63925-705">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="63925-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-706">Az.Compute</span></span>
* <span data-ttu-id="63925-707">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="63925-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="63925-708">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63925-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="63925-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="63925-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="63925-710">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="63925-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="63925-711">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="63925-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="63925-712">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="63925-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="63925-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="63925-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="63925-714">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="63925-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-715">Az.Network</span></span>
* <span data-ttu-id="63925-716">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="63925-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="63925-717">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63925-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-718">Az.Resources</span></span>
* <span data-ttu-id="63925-719">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="63925-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="63925-720">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="63925-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="63925-721">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="63925-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="63925-722">Azure.Storage</span></span>
* <span data-ttu-id="63925-723">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="63925-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="63925-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="63925-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="63925-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="63925-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="63925-726">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="63925-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="63925-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="63925-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="63925-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="63925-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="63925-729">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="63925-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="63925-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="63925-730">Az.Compute</span></span>
* <span data-ttu-id="63925-731">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="63925-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="63925-732">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="63925-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="63925-733">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="63925-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="63925-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="63925-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="63925-735">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="63925-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="63925-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="63925-736">Az.Network</span></span>
* <span data-ttu-id="63925-737">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="63925-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="63925-738">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="63925-738">new cmdlets added</span></span>
    - <span data-ttu-id="63925-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="63925-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="63925-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="63925-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="63925-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="63925-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="63925-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="63925-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="63925-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="63925-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="63925-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="63925-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="63925-745">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="63925-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="63925-746">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="63925-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="63925-747">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="63925-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="63925-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="63925-748">Az.RedisCache</span></span>
* <span data-ttu-id="63925-749">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="63925-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="63925-750">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="63925-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="63925-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="63925-751">Az.Resources</span></span>
* <span data-ttu-id="63925-752">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63925-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="63925-753">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="63925-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="63925-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="63925-754">Az.Sql</span></span>
* <span data-ttu-id="63925-755">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="63925-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="63925-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="63925-756">Az.Websites</span></span>
* <span data-ttu-id="63925-757">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="63925-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="63925-758">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="63925-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="63925-759">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="63925-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="63925-760">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="63925-760">Initial Release</span></span>
