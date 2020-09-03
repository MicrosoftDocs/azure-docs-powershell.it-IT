---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1cc7d6519ded41003daed558a8e78ee65ded072a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240965"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="666b8-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="666b8-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="666b8-104">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="666b8-105">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="666b8-105">Highlights since the last major release</span></span>
* <span data-ttu-id="666b8-106">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="666b8-106">General availability of `Az` module</span></span>
* <span data-ttu-id="666b8-107">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="666b8-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="666b8-108">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="666b8-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="666b8-109">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="666b8-110">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="666b8-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="666b8-111">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="666b8-112">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="666b8-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="666b8-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-113">Az.Accounts</span></span>
* <span data-ttu-id="666b8-114">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="666b8-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="666b8-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="666b8-115">Az.Batch</span></span>
* <span data-ttu-id="666b8-116">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="666b8-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="666b8-117">Az.Cdn</span></span>
* <span data-ttu-id="666b8-118">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="666b8-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="666b8-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="666b8-120">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-121">Az.Compute</span></span>
* <span data-ttu-id="666b8-122">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="666b8-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="666b8-123">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-124">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="666b8-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="666b8-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="666b8-125">Az.DataFactory</span></span>
* <span data-ttu-id="666b8-126">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="666b8-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-128">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="666b8-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="666b8-129">Az.EventGrid</span></span>
* <span data-ttu-id="666b8-130">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="666b8-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="666b8-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="666b8-131">Az.EventHub</span></span>
* <span data-ttu-id="666b8-132">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="666b8-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="666b8-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="666b8-133">Az.HDInsight</span></span>
* <span data-ttu-id="666b8-134">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="666b8-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="666b8-135">Az.IotHub</span></span>
* <span data-ttu-id="666b8-136">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="666b8-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-137">Az.KeyVault</span></span>
* <span data-ttu-id="666b8-138">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-139">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="666b8-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="666b8-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="666b8-140">Az.MachineLearning</span></span>
* <span data-ttu-id="666b8-141">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="666b8-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="666b8-142">Az.Media</span></span>
* <span data-ttu-id="666b8-143">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="666b8-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="666b8-144">Az.Monitor</span></span>
  * <span data-ttu-id="666b8-145">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="666b8-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="666b8-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="666b8-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="666b8-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="666b8-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="666b8-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="666b8-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="666b8-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="666b8-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="666b8-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="666b8-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="666b8-151">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="666b8-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-152">Az.Network</span></span>
* <span data-ttu-id="666b8-153">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-154">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="666b8-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="666b8-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="666b8-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="666b8-156">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="666b8-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="666b8-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="666b8-158">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="666b8-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="666b8-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="666b8-160">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="666b8-162">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-163">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="666b8-164">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="666b8-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="666b8-165">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="666b8-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="666b8-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="666b8-166">Az.RedisCache</span></span>
* <span data-ttu-id="666b8-167">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-168">Az.Resources</span></span>
* <span data-ttu-id="666b8-169">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="666b8-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-170">Az.Sql</span></span>
* <span data-ttu-id="666b8-171">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="666b8-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="666b8-172">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-173">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="666b8-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="666b8-174">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="666b8-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="666b8-175">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="666b8-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="666b8-176">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="666b8-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="666b8-177">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="666b8-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-178">Az.Websites</span></span>
* <span data-ttu-id="666b8-179">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="666b8-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="666b8-180">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="666b8-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="666b8-181">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="666b8-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="666b8-182">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="666b8-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="666b8-183">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="666b8-184">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="666b8-184">Highlights since the last major release</span></span>
* <span data-ttu-id="666b8-185">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="666b8-185">General availability of `Az` module</span></span>
* <span data-ttu-id="666b8-186">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="666b8-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="666b8-187">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="666b8-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="666b8-188">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="666b8-189">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="666b8-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="666b8-190">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="666b8-191">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="666b8-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="666b8-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-192">Az.Accounts</span></span>
* <span data-ttu-id="666b8-193">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="666b8-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="666b8-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="666b8-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="666b8-195">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="666b8-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="666b8-196">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="666b8-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="666b8-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-197">Az.Automation</span></span>
* <span data-ttu-id="666b8-198">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="666b8-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="666b8-199">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="666b8-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="666b8-200">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-201">Az.Compute</span></span>
* <span data-ttu-id="666b8-202">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="666b8-203">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="666b8-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="666b8-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="666b8-205">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="666b8-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="666b8-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="666b8-206">Az.DataFactory</span></span>
* <span data-ttu-id="666b8-207">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="666b8-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="666b8-208">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="666b8-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-209">Az.Resources</span></span>
* <span data-ttu-id="666b8-210">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="666b8-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="666b8-211">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="666b8-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="666b8-212">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="666b8-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="666b8-213">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="666b8-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="666b8-214">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="666b8-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="666b8-215">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="666b8-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-216">Az.Sql</span></span>
* <span data-ttu-id="666b8-217">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="666b8-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="666b8-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-218">Az.Storage</span></span>
* <span data-ttu-id="666b8-219">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="666b8-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="666b8-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="666b8-220">New-AzStorageContext</span></span>
* <span data-ttu-id="666b8-221">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="666b8-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="666b8-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="666b8-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="666b8-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="666b8-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="666b8-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="666b8-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="666b8-226">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="666b8-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="666b8-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="666b8-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="666b8-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="666b8-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="666b8-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="666b8-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="666b8-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="666b8-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="666b8-231">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="666b8-232">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="666b8-232">Highlights since the last major release</span></span>
* <span data-ttu-id="666b8-233">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="666b8-233">General availability of `Az` module</span></span>
* <span data-ttu-id="666b8-234">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="666b8-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="666b8-235">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="666b8-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="666b8-236">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="666b8-237">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="666b8-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="666b8-238">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="666b8-239">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="666b8-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="666b8-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-240">Az.Automation</span></span>
* <span data-ttu-id="666b8-241">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="666b8-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="666b8-242">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="666b8-242">Dynamic grouping</span></span>
    * <span data-ttu-id="666b8-243">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="666b8-243">Pre-Post script</span></span>
    * <span data-ttu-id="666b8-244">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="666b8-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-245">Az.Compute</span></span>
* <span data-ttu-id="666b8-246">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="666b8-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="666b8-247">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="666b8-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="666b8-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-248">Az.KeyVault</span></span>
* <span data-ttu-id="666b8-249">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-250">Az.Network</span></span>
* <span data-ttu-id="666b8-251">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="666b8-252">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="666b8-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="666b8-254">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="666b8-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="666b8-255">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="666b8-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-256">Az.Resources</span></span>
* <span data-ttu-id="666b8-257">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="666b8-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="666b8-258">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="666b8-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-259">Az.Sql</span></span>
* <span data-ttu-id="666b8-260">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="666b8-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="666b8-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-261">Az.Storage</span></span>
* <span data-ttu-id="666b8-262">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="666b8-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="666b8-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="666b8-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="666b8-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="666b8-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="666b8-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="666b8-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="666b8-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="666b8-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="666b8-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-269">Az.Websites</span></span>
* <span data-ttu-id="666b8-270">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="666b8-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="666b8-271">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="666b8-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-272">Az.Accounts</span></span>
* <span data-ttu-id="666b8-273">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="666b8-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="666b8-274">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="666b8-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="666b8-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-275">Az.Automation</span></span>
* <span data-ttu-id="666b8-276">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="666b8-277">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="666b8-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="666b8-278">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="666b8-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="666b8-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="666b8-279">Az.Cdn</span></span>
* <span data-ttu-id="666b8-280">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="666b8-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-281">Az.Compute</span></span>
* <span data-ttu-id="666b8-282">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="666b8-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="666b8-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="666b8-283">Az.DataFactory</span></span>
* <span data-ttu-id="666b8-284">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="666b8-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="666b8-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="666b8-285">Az.LogicApp</span></span>
* <span data-ttu-id="666b8-286">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="666b8-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-287">Az.Network</span></span>
* <span data-ttu-id="666b8-288">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="666b8-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="666b8-290">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="666b8-291">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="666b8-291">SDK Update</span></span>
* <span data-ttu-id="666b8-292">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="666b8-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="666b8-293">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="666b8-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-294">Az.Resources</span></span>
* <span data-ttu-id="666b8-295">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="666b8-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="666b8-296">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="666b8-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="666b8-297">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="666b8-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="666b8-298">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="666b8-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="666b8-299">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="666b8-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="666b8-300">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="666b8-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-301">Az.Sql</span></span>
* <span data-ttu-id="666b8-302">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="666b8-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="666b8-303">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="666b8-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="666b8-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-304">Az.Storage</span></span>
* <span data-ttu-id="666b8-305">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="666b8-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="666b8-306">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="666b8-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="666b8-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="666b8-308">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="666b8-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="666b8-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-309">Az.Automation</span></span>
* <span data-ttu-id="666b8-310">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="666b8-311">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="666b8-312">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="666b8-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="666b8-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="666b8-314">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="666b8-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-315">Az.Compute</span></span>
* <span data-ttu-id="666b8-316">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="666b8-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="666b8-317">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="666b8-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="666b8-318">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="666b8-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="666b8-319">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="666b8-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-321">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="666b8-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="666b8-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="666b8-322">Az.EventHub</span></span>
* <span data-ttu-id="666b8-323">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="666b8-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="666b8-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-324">Az.KeyVault</span></span>
* <span data-ttu-id="666b8-325">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="666b8-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="666b8-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="666b8-326">Az.LogicApp</span></span>
* <span data-ttu-id="666b8-327">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="666b8-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="666b8-328">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="666b8-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="666b8-329">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="666b8-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="666b8-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="666b8-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="666b8-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="666b8-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="666b8-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="666b8-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="666b8-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="666b8-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="666b8-334">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="666b8-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="666b8-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="666b8-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="666b8-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="666b8-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="666b8-339">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="666b8-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="666b8-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="666b8-340">Az.Monitor</span></span>
* <span data-ttu-id="666b8-341">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="666b8-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-342">Az.Network</span></span>
* <span data-ttu-id="666b8-343">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="666b8-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="666b8-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="666b8-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="666b8-345">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="666b8-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="666b8-346">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="666b8-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="666b8-347">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="666b8-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-348">Az.Resources</span></span>
* <span data-ttu-id="666b8-349">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="666b8-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="666b8-350">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="666b8-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="666b8-351">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="666b8-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="666b8-352">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="666b8-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-353">Az.Sql</span></span>
* <span data-ttu-id="666b8-354">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="666b8-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="666b8-355">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="666b8-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-356">Az.Websites</span></span>
* <span data-ttu-id="666b8-357">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="666b8-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="666b8-358">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="666b8-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-359">Az.Accounts</span></span>
* <span data-ttu-id="666b8-360">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="666b8-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="666b8-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="666b8-361">Az.AnalysisServices</span></span>
<span data-ttu-id="666b8-362">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="666b8-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-363">Az.Compute</span></span>
* <span data-ttu-id="666b8-364">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="666b8-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="666b8-365">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="666b8-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="666b8-366">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="666b8-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-367">Az.RecoveryServices</span></span>
<span data-ttu-id="666b8-368">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="666b8-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-369">Az.Resources</span></span>
* <span data-ttu-id="666b8-370">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="666b8-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="666b8-371">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="666b8-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="666b8-372">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="666b8-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="666b8-373">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="666b8-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-374">Az.Sql</span></span>
* <span data-ttu-id="666b8-375">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="666b8-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="666b8-376">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="666b8-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="666b8-377">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="666b8-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="666b8-378">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="666b8-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-379">Az.Accounts</span></span>
* <span data-ttu-id="666b8-380">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="666b8-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="666b8-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="666b8-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="666b8-382">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="666b8-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="666b8-384">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="666b8-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="666b8-385">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="666b8-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-386">Az.Accounts</span></span>
* <span data-ttu-id="666b8-387">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="666b8-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="666b8-388">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="666b8-389">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="666b8-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="666b8-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="666b8-390">Az.Aks</span></span>
* <span data-ttu-id="666b8-391">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="666b8-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-392">Az.Automation</span></span>
* <span data-ttu-id="666b8-393">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="666b8-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="666b8-394">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="666b8-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="666b8-395">Az.Cdn</span></span>
* <span data-ttu-id="666b8-396">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-397">Az.Compute</span></span>
* <span data-ttu-id="666b8-398">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="666b8-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="666b8-399">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="666b8-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="666b8-400">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="666b8-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="666b8-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="666b8-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="666b8-402">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="666b8-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="666b8-403">Az.DataFactory</span></span>
* <span data-ttu-id="666b8-404">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="666b8-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-406">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="666b8-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="666b8-407">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="666b8-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="666b8-408">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="666b8-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="666b8-409">Az.IotHub</span></span>
* <span data-ttu-id="666b8-410">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="666b8-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="666b8-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-411">Az.KeyVault</span></span>
* <span data-ttu-id="666b8-412">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-413">Az.Network</span></span>
* <span data-ttu-id="666b8-414">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-415">Az.Resources</span></span>
* <span data-ttu-id="666b8-416">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="666b8-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="666b8-417">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="666b8-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="666b8-418">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="666b8-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="666b8-419">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="666b8-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="666b8-420">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="666b8-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="666b8-421">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="666b8-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="666b8-422">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="666b8-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="666b8-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="666b8-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="666b8-424">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="666b8-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="666b8-425">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="666b8-425">Fix some error messages.</span></span>
* <span data-ttu-id="666b8-426">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="666b8-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="666b8-427">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="666b8-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="666b8-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="666b8-428">Az.SignalR</span></span>
* <span data-ttu-id="666b8-429">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-430">Az.Sql</span></span>
* <span data-ttu-id="666b8-431">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="666b8-432">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="666b8-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="666b8-433">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="666b8-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="666b8-434">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="666b8-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="666b8-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-435">Az.Storage</span></span>
* <span data-ttu-id="666b8-436">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="666b8-437">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="666b8-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="666b8-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="666b8-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="666b8-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="666b8-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="666b8-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="666b8-440">Az.TrafficManager</span></span>
* <span data-ttu-id="666b8-441">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-442">Az.Websites</span></span>
* <span data-ttu-id="666b8-443">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="666b8-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="666b8-444">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="666b8-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="666b8-445">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="666b8-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="666b8-446">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="666b8-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="666b8-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-447">Az.Accounts</span></span>
* <span data-ttu-id="666b8-448">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="666b8-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-449">Az.Compute</span></span>
* <span data-ttu-id="666b8-450">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="666b8-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="666b8-451">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="666b8-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="666b8-452">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-454">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="666b8-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="666b8-455">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="666b8-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="666b8-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="666b8-456">Az.EventGrid</span></span>
* <span data-ttu-id="666b8-457">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="666b8-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="666b8-458">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="666b8-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="666b8-459">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="666b8-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="666b8-460">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="666b8-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="666b8-461">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="666b8-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="666b8-462">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="666b8-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="666b8-463">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="666b8-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="666b8-464">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="666b8-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="666b8-465">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="666b8-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="666b8-466">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="666b8-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="666b8-467">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="666b8-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="666b8-468">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="666b8-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="666b8-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="666b8-469">Az.IotHub</span></span>
* <span data-ttu-id="666b8-470">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="666b8-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="666b8-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="666b8-471">Az.LogicApp</span></span>
* <span data-ttu-id="666b8-472">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="666b8-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-473">Az.Resources</span></span>
* <span data-ttu-id="666b8-474">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="666b8-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="666b8-475">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="666b8-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="666b8-476">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666b8-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="666b8-477">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="666b8-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="666b8-478">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="666b8-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="666b8-479">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="666b8-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="666b8-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="666b8-480">Az.SignalR</span></span>
* <span data-ttu-id="666b8-481">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-482">Az.Sql</span></span>
* <span data-ttu-id="666b8-483">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="666b8-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="666b8-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-484">Az.Storage</span></span>
* <span data-ttu-id="666b8-485">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="666b8-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="666b8-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="666b8-486">New-AzStorageContext</span></span>
* <span data-ttu-id="666b8-487">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="666b8-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="666b8-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="666b8-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-489">Az.Websites</span></span>
* <span data-ttu-id="666b8-490">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="666b8-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="666b8-491">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="666b8-492">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="666b8-493">Generale</span><span class="sxs-lookup"><span data-stu-id="666b8-493">General</span></span>

- <span data-ttu-id="666b8-494">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="666b8-494">General Availability of Az Module</span></span>
- <span data-ttu-id="666b8-495">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="666b8-495">Online help for each module</span></span>
- <span data-ttu-id="666b8-496">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="666b8-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="666b8-497">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="666b8-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="666b8-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-498">Az.Accounts</span></span>
- <span data-ttu-id="666b8-499">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="666b8-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="666b8-500">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="666b8-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="666b8-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="666b8-501">Az.ApiManagement</span></span>
- <span data-ttu-id="666b8-502">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="666b8-502">Fixes for #7002</span></span>
- <span data-ttu-id="666b8-503">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="666b8-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="666b8-504">Az.Batch</span></span>
- <span data-ttu-id="666b8-505">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="666b8-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="666b8-506">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="666b8-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="666b8-507">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="666b8-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="666b8-508">Az.Billing</span></span>
- <span data-ttu-id="666b8-509">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="666b8-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="666b8-510">Az.CognitivServices</span></span>
- <span data-ttu-id="666b8-511">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="666b8-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="666b8-512">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="666b8-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="666b8-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="666b8-514">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="666b8-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="666b8-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="666b8-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="666b8-516">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="666b8-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="666b8-518">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="666b8-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="666b8-519">Az.Monitor</span></span>
- <span data-ttu-id="666b8-520">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="666b8-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="666b8-521">Az.KeyVault</span></span>
- <span data-ttu-id="666b8-522">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="666b8-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="666b8-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="666b8-523">Az.MachineLearning</span></span>
- <span data-ttu-id="666b8-524">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="666b8-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="666b8-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="666b8-525">Az.Media</span></span>
- <span data-ttu-id="666b8-526">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="666b8-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="666b8-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-527">Az.Network</span></span>
<span data-ttu-id="666b8-528">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="666b8-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="666b8-529">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="666b8-529">New cmdlets added:</span></span>
        - <span data-ttu-id="666b8-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="666b8-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="666b8-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="666b8-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="666b8-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="666b8-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="666b8-538">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="666b8-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="666b8-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="666b8-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="666b8-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="666b8-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="666b8-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="666b8-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="666b8-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="666b8-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="666b8-544">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="666b8-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="666b8-545">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="666b8-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="666b8-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="666b8-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="666b8-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="666b8-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="666b8-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="666b8-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="666b8-549">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="666b8-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="666b8-550">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="666b8-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="666b8-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="666b8-552">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="666b8-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="666b8-553">Az.Profile</span></span>
- <span data-ttu-id="666b8-554">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="666b8-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="666b8-556">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="666b8-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-557">Az.Resources</span></span>
- <span data-ttu-id="666b8-558">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="666b8-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="666b8-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="666b8-560">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="666b8-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="666b8-561">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="666b8-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="666b8-562">Az.SIgnalR</span></span>
- <span data-ttu-id="666b8-563">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="666b8-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="666b8-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-564">Az.Sql</span></span>
- <span data-ttu-id="666b8-565">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="666b8-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="666b8-566">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="666b8-567">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="666b8-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-568">Az.Storage</span></span>
- <span data-ttu-id="666b8-569">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="666b8-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-570">Az.Websites</span></span>
- <span data-ttu-id="666b8-571">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="666b8-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="666b8-572">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="666b8-573">Generale</span><span class="sxs-lookup"><span data-stu-id="666b8-573">General</span></span>

* <span data-ttu-id="666b8-574">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="666b8-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="666b8-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-575">Az.Compute</span></span>

* <span data-ttu-id="666b8-576">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="666b8-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="666b8-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="666b8-578">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="666b8-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="666b8-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="666b8-579">Az.FrontDoor</span></span>

* <span data-ttu-id="666b8-580">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="666b8-580">Fixed some broken links</span></span>
    - <span data-ttu-id="666b8-581">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="666b8-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="666b8-582">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="666b8-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="666b8-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="666b8-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="666b8-584">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="666b8-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="666b8-585">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="666b8-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="666b8-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-586">Az.Resources</span></span>

* <span data-ttu-id="666b8-587">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="666b8-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="666b8-588">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="666b8-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="666b8-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-589">Az.Sql</span></span>

* <span data-ttu-id="666b8-590">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="666b8-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="666b8-591">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="666b8-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="666b8-592">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="666b8-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="666b8-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-593">Az.Storage</span></span>

* <span data-ttu-id="666b8-594">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="666b8-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="666b8-595">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="666b8-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="666b8-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="666b8-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="666b8-597">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="666b8-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="666b8-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="666b8-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="666b8-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="666b8-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="666b8-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-600">Az.Websites</span></span>

* <span data-ttu-id="666b8-601">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="666b8-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="666b8-602">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="666b8-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="666b8-603">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="666b8-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="666b8-604">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="666b8-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="666b8-605">Az.ApiManagement</span></span>
* <span data-ttu-id="666b8-606">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="666b8-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="666b8-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="666b8-607">Az.Automation</span></span>
* <span data-ttu-id="666b8-608">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="666b8-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="666b8-609">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="666b8-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="666b8-610">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="666b8-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="666b8-611">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="666b8-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="666b8-612">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="666b8-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="666b8-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-613">Az.Compute</span></span>
* <span data-ttu-id="666b8-614">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="666b8-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="666b8-615">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="666b8-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="666b8-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="666b8-617">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="666b8-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="666b8-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="666b8-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="666b8-619">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="666b8-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="666b8-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-620">Az.Network</span></span>
* <span data-ttu-id="666b8-621">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="666b8-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="666b8-622">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="666b8-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="666b8-623">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="666b8-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="666b8-624">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="666b8-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="666b8-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="666b8-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="666b8-626">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="666b8-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="666b8-627">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="666b8-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="666b8-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="666b8-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="666b8-629">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="666b8-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="666b8-630">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="666b8-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="666b8-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="666b8-631">Az.Relay</span></span>
* <span data-ttu-id="666b8-632">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="666b8-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="666b8-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-633">Az.Resources</span></span>
* <span data-ttu-id="666b8-634">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="666b8-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="666b8-635">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="666b8-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="666b8-636">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="666b8-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="666b8-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="666b8-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="666b8-638">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="666b8-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="666b8-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-639">Az.Sql</span></span>
* <span data-ttu-id="666b8-640">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="666b8-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="666b8-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="666b8-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="666b8-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="666b8-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="666b8-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="666b8-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="666b8-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="666b8-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="666b8-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="666b8-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="666b8-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="666b8-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="666b8-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="666b8-649">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="666b8-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="666b8-650">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="666b8-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="666b8-651">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="666b8-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="666b8-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="666b8-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="666b8-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="666b8-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="666b8-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="666b8-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="666b8-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="666b8-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="666b8-656">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="666b8-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="666b8-657">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="666b8-658">Generale</span><span class="sxs-lookup"><span data-stu-id="666b8-658">General</span></span>
* <span data-ttu-id="666b8-659">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="666b8-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="666b8-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="666b8-660">Az.Profile</span></span>
* <span data-ttu-id="666b8-661">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="666b8-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="666b8-662">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="666b8-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="666b8-663">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="666b8-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="666b8-664">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="666b8-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="666b8-665">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="666b8-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="666b8-666">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="666b8-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="666b8-667">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="666b8-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="666b8-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="666b8-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="666b8-669">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="666b8-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-670">Az.Compute</span></span>
* <span data-ttu-id="666b8-671">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="666b8-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="666b8-672">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="666b8-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="666b8-673">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="666b8-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-675">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="666b8-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="666b8-676">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="666b8-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="666b8-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="666b8-677">Az.Insights</span></span>
* <span data-ttu-id="666b8-678">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="666b8-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="666b8-679">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="666b8-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="666b8-680">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="666b8-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="666b8-681">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="666b8-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-682">Az.Network</span></span>
* <span data-ttu-id="666b8-683">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="666b8-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="666b8-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="666b8-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="666b8-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="666b8-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="666b8-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="666b8-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="666b8-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="666b8-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="666b8-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="666b8-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="666b8-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="666b8-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="666b8-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="666b8-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="666b8-691">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="666b8-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-692">Az.Resources</span></span>
* <span data-ttu-id="666b8-693">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="666b8-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="666b8-694">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="666b8-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="666b8-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="666b8-695">Az.ServiceBus</span></span>
* <span data-ttu-id="666b8-696">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="666b8-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="666b8-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="666b8-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="666b8-698">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="666b8-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="666b8-699">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="666b8-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="666b8-700">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="666b8-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="666b8-701">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="666b8-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="666b8-702">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="666b8-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="666b8-703">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="666b8-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="666b8-704">Az.Profile</span></span>
* <span data-ttu-id="666b8-705">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="666b8-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="666b8-706">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="666b8-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-707">Az.Compute</span></span>
* <span data-ttu-id="666b8-708">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="666b8-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="666b8-709">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666b8-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="666b8-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="666b8-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="666b8-711">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="666b8-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="666b8-712">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="666b8-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="666b8-713">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="666b8-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="666b8-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="666b8-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="666b8-715">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="666b8-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-716">Az.Network</span></span>
* <span data-ttu-id="666b8-717">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="666b8-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="666b8-718">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666b8-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-719">Az.Resources</span></span>
* <span data-ttu-id="666b8-720">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="666b8-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="666b8-721">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="666b8-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="666b8-722">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="666b8-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="666b8-723">Azure.Storage</span></span>
* <span data-ttu-id="666b8-724">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="666b8-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="666b8-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="666b8-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="666b8-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="666b8-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="666b8-727">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="666b8-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="666b8-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="666b8-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="666b8-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="666b8-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="666b8-730">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="666b8-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="666b8-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="666b8-731">Az.Compute</span></span>
* <span data-ttu-id="666b8-732">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="666b8-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="666b8-733">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="666b8-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="666b8-734">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="666b8-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="666b8-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="666b8-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="666b8-736">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="666b8-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="666b8-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="666b8-737">Az.Network</span></span>
* <span data-ttu-id="666b8-738">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="666b8-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="666b8-739">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="666b8-739">new cmdlets added</span></span>
    - <span data-ttu-id="666b8-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="666b8-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="666b8-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="666b8-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="666b8-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="666b8-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="666b8-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="666b8-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="666b8-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="666b8-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="666b8-746">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="666b8-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="666b8-747">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="666b8-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="666b8-748">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="666b8-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="666b8-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="666b8-749">Az.RedisCache</span></span>
* <span data-ttu-id="666b8-750">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="666b8-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="666b8-751">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="666b8-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="666b8-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="666b8-752">Az.Resources</span></span>
* <span data-ttu-id="666b8-753">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="666b8-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="666b8-754">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="666b8-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="666b8-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="666b8-755">Az.Sql</span></span>
* <span data-ttu-id="666b8-756">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="666b8-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="666b8-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="666b8-757">Az.Websites</span></span>
* <span data-ttu-id="666b8-758">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="666b8-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="666b8-759">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="666b8-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="666b8-760">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="666b8-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="666b8-761">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="666b8-761">Initial Release</span></span>
