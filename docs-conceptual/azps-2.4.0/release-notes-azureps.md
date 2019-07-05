---
ms.openlocfilehash: ac8513b3eee4adfcaf0be8bf7b4e8d09190811df
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516641"
---
## <a name="240---july-2019"></a><span data-ttu-id="2b733-101">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-102">Az.Accounts</span></span>
* <span data-ttu-id="2b733-103">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="2b733-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2b733-104">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="2b733-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2b733-105">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b733-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2b733-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2b733-106">Az.Advisor</span></span>
* <span data-ttu-id="2b733-107">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2b733-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2b733-108">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="2b733-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2b733-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-109">Az.ApiManagement</span></span>
* <span data-ttu-id="2b733-110">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2b733-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2b733-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2b733-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2b733-112">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="2b733-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2b733-113">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="2b733-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2b733-114">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2b733-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2b733-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2b733-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2b733-116">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="2b733-116">Added support for specifiying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-117">Az.Automation</span></span>
* <span data-ttu-id="2b733-118">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="2b733-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-119">Az.Compute</span></span>
* <span data-ttu-id="2b733-120">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2b733-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b733-121">Az.DataFactory</span></span>
* <span data-ttu-id="2b733-122">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2b733-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2b733-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2b733-123">Az.EventGrid</span></span>
* <span data-ttu-id="2b733-124">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="2b733-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2b733-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2b733-125">Az.IotHub</span></span>
* <span data-ttu-id="2b733-126">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2b733-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-127">Az.Network</span></span>
* <span data-ttu-id="2b733-128">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="2b733-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2b733-129">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="2b733-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2b733-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="2b733-131">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2b733-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2b733-132">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2b733-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2b733-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="2b733-134">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2b733-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-136">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="2b733-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-137">Az.Resources</span></span>
    - <span data-ttu-id="2b733-138">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="2b733-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2b733-139">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2b733-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2b733-140">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="2b733-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2b733-141">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="2b733-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2b733-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b733-142">Az.ServiceBus</span></span>
* <span data-ttu-id="2b733-143">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2b733-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-144">Az.Sql</span></span>
* <span data-ttu-id="2b733-145">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="2b733-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2b733-146">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2b733-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2b733-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2b733-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2b733-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2b733-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2b733-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2b733-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2b733-153">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="2b733-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-154">Az.Storage</span></span>
* <span data-ttu-id="2b733-155">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2b733-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2b733-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2b733-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2b733-157">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="2b733-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2b733-158">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="2b733-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2b733-159">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2b733-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2b733-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2b733-162">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="2b733-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2b733-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2b733-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2b733-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2b733-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2b733-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2b733-165">Az.StorageSync</span></span>
* <span data-ttu-id="2b733-166">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="2b733-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2b733-167">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-168">Az.Accounts</span></span>
* <span data-ttu-id="2b733-169">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="2b733-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2b733-170">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2b733-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2b733-171">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="2b733-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2b733-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2b733-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2b733-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2b733-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-174">Az.Compute</span></span>
* <span data-ttu-id="2b733-175">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="2b733-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2b733-176">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="2b733-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2b733-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2b733-177">Az.Dns</span></span>
* <span data-ttu-id="2b733-178">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="2b733-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2b733-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2b733-179">Az.EventGrid</span></span>
* <span data-ttu-id="2b733-180">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2b733-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2b733-181">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2b733-181">New cmdlets:</span></span>
    - <span data-ttu-id="2b733-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2b733-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2b733-183">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2b733-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2b733-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2b733-185">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2b733-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2b733-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2b733-187">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2b733-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2b733-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2b733-189">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2b733-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2b733-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2b733-191">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="2b733-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2b733-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2b733-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2b733-193">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2b733-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2b733-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2b733-195">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="2b733-196">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2b733-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2b733-197">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="2b733-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2b733-198">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2b733-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="2b733-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2b733-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2b733-200">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2b733-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2b733-201">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2b733-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2b733-202">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="2b733-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2b733-203">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2b733-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2b733-204">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="2b733-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2b733-205">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="2b733-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2b733-206">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b733-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2b733-207">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="2b733-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="2b733-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2b733-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2b733-209">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="2b733-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2b733-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2b733-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2b733-211">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2b733-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2b733-212">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2b733-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2b733-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2b733-213">Az.FrontDoor</span></span>
* <span data-ttu-id="2b733-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2b733-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2b733-215">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="2b733-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2b733-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2b733-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2b733-217">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="2b733-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-218">Az.Network</span></span>
* <span data-ttu-id="2b733-219">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2b733-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2b733-220">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-220">New cmdlets</span></span>
        - <span data-ttu-id="2b733-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2b733-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2b733-222">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2b733-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2b733-223">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-223">New cmdlets</span></span> 
        - <span data-ttu-id="2b733-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2b733-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2b733-225">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2b733-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2b733-226">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-226">New cmdlets</span></span> 
        - <span data-ttu-id="2b733-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2b733-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="2b733-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2b733-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2b733-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2b733-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2b733-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2b733-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2b733-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2b733-232">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b733-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2b733-233">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-233">New cmdlets</span></span>
        - <span data-ttu-id="2b733-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b733-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2b733-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b733-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2b733-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b733-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2b733-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2b733-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2b733-238">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2b733-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2b733-239">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="2b733-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2b733-240">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="2b733-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2b733-241">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b733-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2b733-242">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b733-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2b733-243">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b733-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2b733-244">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2b733-245">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="2b733-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2b733-246">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2b733-247">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="2b733-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2b733-248">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2b733-249">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2b733-250">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2b733-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2b733-251">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2b733-252">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2b733-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2b733-253">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="2b733-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2b733-254">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2b733-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2b733-255">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="2b733-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2b733-256">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2b733-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="2b733-257">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2b733-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="2b733-258">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2b733-259">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2b733-260">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2b733-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="2b733-262">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="2b733-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-263">Az.Resources</span></span>
* <span data-ttu-id="2b733-264">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="2b733-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2b733-265">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2b733-266">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2b733-267">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="2b733-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2b733-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="2b733-269">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="2b733-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-270">Az.Sql</span></span>
* <span data-ttu-id="2b733-271">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2b733-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2b733-272">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2b733-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2b733-273">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="2b733-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2b733-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2b733-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2b733-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2b733-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2b733-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2b733-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2b733-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2b733-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2b733-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2b733-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-279">Az.Storage</span></span>
* <span data-ttu-id="2b733-280">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2b733-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2b733-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="2b733-282">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="2b733-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2b733-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-284">Az.Websites</span></span>
* <span data-ttu-id="2b733-285">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="2b733-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2b733-286">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2b733-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2b733-287">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2b733-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2b733-288">Az.Cdn</span></span>
* <span data-ttu-id="2b733-289">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="2b733-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-290">Az.Compute</span></span>
* <span data-ttu-id="2b733-291">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2b733-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2b733-292">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b733-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2b733-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b733-293">Az.EventHub</span></span>
* <span data-ttu-id="2b733-294">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="2b733-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2b733-295">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b733-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-296">Az.Network</span></span>
* <span data-ttu-id="2b733-297">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="2b733-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2b733-298">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="2b733-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2b733-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="2b733-300">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2b733-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-302">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="2b733-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2b733-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b733-303">Az.ServiceBus</span></span>
* <span data-ttu-id="2b733-304">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b733-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2b733-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="2b733-306">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="2b733-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2b733-307">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2b733-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-308">Az.Sql</span></span>
* <span data-ttu-id="2b733-309">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="2b733-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2b733-310">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2b733-311">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2b733-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2b733-312">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="2b733-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-313">Az.Websites</span></span>
* <span data-ttu-id="2b733-314">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="2b733-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2b733-315">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2b733-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-316">Az.ApiManagement</span></span>
* <span data-ttu-id="2b733-317">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="2b733-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2b733-318">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2b733-319">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2b733-320">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="2b733-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2b733-321">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2b733-322">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="2b733-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2b733-323">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2b733-324">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2b733-325">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2b733-326">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="2b733-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2b733-327">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2b733-328">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="2b733-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2b733-329">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="2b733-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2b733-330">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2b733-331">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="2b733-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2b733-332">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2b733-333">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2b733-334">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="2b733-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2b733-335">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="2b733-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="2b733-336">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="2b733-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2b733-337">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="2b733-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2b733-338">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2b733-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2b733-339">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="2b733-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2b733-340">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="2b733-341">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="2b733-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2b733-342">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="2b733-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2b733-343">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="2b733-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2b733-344">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2b733-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2b733-345">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2b733-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2b733-346">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="2b733-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2b733-347">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="2b733-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="2b733-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2b733-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2b733-349">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2b733-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2b733-350">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2b733-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2b733-351">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2b733-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2b733-352">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="2b733-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2b733-353">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="2b733-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2b733-354">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="2b733-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2b733-355">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="2b733-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2b733-356">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2b733-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="2b733-357">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2b733-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2b733-358">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2b733-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2b733-359">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2b733-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2b733-360">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="2b733-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2b733-361">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2b733-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2b733-362">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2b733-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2b733-363">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2b733-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="2b733-364">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="2b733-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2b733-365">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="2b733-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2b733-366">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2b733-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2b733-367">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="2b733-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2b733-368">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="2b733-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2b733-369">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="2b733-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2b733-370">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="2b733-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2b733-371">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="2b733-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2b733-372">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="2b733-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2b733-373">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2b733-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2b733-374">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2b733-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2b733-375">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2b733-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2b733-376">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2b733-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2b733-377">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2b733-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2b733-378">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2b733-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2b733-379">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2b733-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2b733-380">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2b733-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2b733-381">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="2b733-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2b733-382">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="2b733-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2b733-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2b733-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2b733-384">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="2b733-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2b733-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2b733-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2b733-386">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2b733-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2b733-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2b733-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2b733-388">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2b733-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2b733-389">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="2b733-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2b733-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2b733-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2b733-391">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="2b733-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="2b733-392">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2b733-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2b733-393">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="2b733-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-394">Az.Automation</span></span>
* <span data-ttu-id="2b733-395">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="2b733-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2b733-396">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2b733-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2b733-397">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2b733-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2b733-398">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="2b733-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2b733-399">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2b733-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2b733-400">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="2b733-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2b733-401">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2b733-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-402">Az.Compute</span></span>
* <span data-ttu-id="2b733-403">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2b733-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2b733-404">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="2b733-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-406">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2b733-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2b733-407">Az.Monitor</span></span>
* <span data-ttu-id="2b733-408">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="2b733-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-409">Az.Network</span></span>
* <span data-ttu-id="2b733-410">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="2b733-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2b733-411">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2b733-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="2b733-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b733-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2b733-413">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2b733-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-414">Az.Resources</span></span>
* <span data-ttu-id="2b733-415">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="2b733-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-416">Az.Sql</span></span>
* <span data-ttu-id="2b733-417">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="2b733-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2b733-418">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-419">Az.Accounts</span></span>
* <span data-ttu-id="2b733-420">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="2b733-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2b733-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2b733-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="2b733-422">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="2b733-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2b733-423">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="2b733-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-424">Az.Compute</span></span>
* <span data-ttu-id="2b733-425">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="2b733-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2b733-426">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2b733-427">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2b733-428">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2b733-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2b733-429">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2b733-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2b733-430">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2b733-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="2b733-431">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="2b733-431">Breaking changes</span></span>
    - <span data-ttu-id="2b733-432">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2b733-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2b733-433">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2b733-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2b733-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2b733-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="2b733-435">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="2b733-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2b733-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2b733-436">Az.Dns</span></span>
* <span data-ttu-id="2b733-437">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="2b733-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2b733-438">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2b733-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2b733-439">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="2b733-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2b733-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2b733-440">Az.FrontDoor</span></span>
* <span data-ttu-id="2b733-441">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2b733-442">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="2b733-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2b733-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2b733-443">Az.HDInsight</span></span>
* <span data-ttu-id="2b733-444">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2b733-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2b733-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2b733-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2b733-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2b733-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2b733-447">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2b733-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2b733-448">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="2b733-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2b733-449">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2b733-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2b733-450">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="2b733-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2b733-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2b733-451">Az.Monitor</span></span>
* <span data-ttu-id="2b733-452">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="2b733-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="2b733-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2b733-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2b733-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2b733-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2b733-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2b733-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2b733-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2b733-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2b733-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2b733-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2b733-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2b733-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2b733-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2b733-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2b733-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2b733-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2b733-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2b733-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2b733-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2b733-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2b733-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2b733-464">[Altre](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="2b733-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2b733-465">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="2b733-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-466">Az.Network</span></span>
* <span data-ttu-id="2b733-467">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="2b733-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2b733-468">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-468">New cmdlets</span></span>
        - <span data-ttu-id="2b733-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="2b733-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2b733-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2b733-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2b733-473">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2b733-473">Updated cmdlets</span></span>
        - <span data-ttu-id="2b733-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2b733-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2b733-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2b733-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2b733-476">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2b733-477">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2b733-478">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2b733-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2b733-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="2b733-480">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b733-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2b733-481">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2b733-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2b733-482">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="2b733-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-484">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="2b733-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2b733-485">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2b733-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2b733-486">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2b733-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2b733-487">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2b733-488">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="2b733-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2b733-489">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="2b733-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2b733-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2b733-490">Az.Relay</span></span>
* <span data-ttu-id="2b733-491">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="2b733-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2b733-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b733-492">Az.ServiceBus</span></span>
* <span data-ttu-id="2b733-493">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b733-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-494">Az.Storage</span></span>
* <span data-ttu-id="2b733-495">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="2b733-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2b733-496">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2b733-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2b733-497">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="2b733-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2b733-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="2b733-499">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="2b733-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2b733-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2b733-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2b733-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-503">Az.Websites</span></span>
* <span data-ttu-id="2b733-504">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b733-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2b733-505">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="2b733-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2b733-506">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2b733-507">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2b733-507">Highlights since the last major release</span></span>
* <span data-ttu-id="2b733-508">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2b733-508">General availability of `Az` module</span></span>
* <span data-ttu-id="2b733-509">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2b733-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2b733-510">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2b733-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2b733-511">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2b733-512">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2b733-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2b733-513">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2b733-514">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2b733-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2b733-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-515">Az.Accounts</span></span>
* <span data-ttu-id="2b733-516">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="2b733-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2b733-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2b733-517">Az.Batch</span></span>
* <span data-ttu-id="2b733-518">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2b733-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2b733-519">Az.Cdn</span></span>
* <span data-ttu-id="2b733-520">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2b733-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2b733-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="2b733-522">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-523">Az.Compute</span></span>
* <span data-ttu-id="2b733-524">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="2b733-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2b733-525">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-526">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2b733-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2b733-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b733-527">Az.DataFactory</span></span>
* <span data-ttu-id="2b733-528">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="2b733-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-530">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2b733-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2b733-531">Az.EventGrid</span></span>
* <span data-ttu-id="2b733-532">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2b733-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2b733-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b733-533">Az.EventHub</span></span>
* <span data-ttu-id="2b733-534">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b733-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2b733-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2b733-535">Az.HDInsight</span></span>
* <span data-ttu-id="2b733-536">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2b733-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2b733-537">Az.IotHub</span></span>
* <span data-ttu-id="2b733-538">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2b733-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-539">Az.KeyVault</span></span>
* <span data-ttu-id="2b733-540">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-541">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2b733-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2b733-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2b733-542">Az.MachineLearning</span></span>
* <span data-ttu-id="2b733-543">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2b733-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2b733-544">Az.Media</span></span>
* <span data-ttu-id="2b733-545">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2b733-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2b733-546">Az.Monitor</span></span>
  * <span data-ttu-id="2b733-547">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="2b733-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2b733-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2b733-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2b733-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2b733-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2b733-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2b733-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2b733-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2b733-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2b733-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2b733-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2b733-553">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="2b733-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-554">Az.Network</span></span>
* <span data-ttu-id="2b733-555">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-556">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2b733-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2b733-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2b733-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="2b733-558">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2b733-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="2b733-560">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2b733-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2b733-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2b733-562">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-564">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-565">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2b733-566">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2b733-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2b733-567">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="2b733-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2b733-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2b733-568">Az.RedisCache</span></span>
* <span data-ttu-id="2b733-569">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-570">Az.Resources</span></span>
* <span data-ttu-id="2b733-571">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2b733-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-572">Az.Sql</span></span>
* <span data-ttu-id="2b733-573">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="2b733-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2b733-574">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-575">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="2b733-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2b733-576">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2b733-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2b733-577">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="2b733-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2b733-578">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="2b733-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2b733-579">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2b733-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-580">Az.Websites</span></span>
* <span data-ttu-id="2b733-581">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="2b733-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2b733-582">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2b733-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2b733-583">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="2b733-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2b733-584">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2b733-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2b733-585">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2b733-586">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2b733-586">Highlights since the last major release</span></span>
* <span data-ttu-id="2b733-587">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2b733-587">General availability of `Az` module</span></span>
* <span data-ttu-id="2b733-588">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2b733-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2b733-589">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2b733-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2b733-590">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2b733-591">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2b733-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2b733-592">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2b733-593">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2b733-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2b733-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-594">Az.Accounts</span></span>
* <span data-ttu-id="2b733-595">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2b733-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2b733-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b733-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="2b733-597">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="2b733-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2b733-598">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="2b733-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-599">Az.Automation</span></span>
* <span data-ttu-id="2b733-600">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="2b733-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2b733-601">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="2b733-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2b733-602">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-603">Az.Compute</span></span>
* <span data-ttu-id="2b733-604">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2b733-605">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="2b733-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="2b733-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="2b733-607">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="2b733-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2b733-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b733-608">Az.DataFactory</span></span>
* <span data-ttu-id="2b733-609">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="2b733-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2b733-610">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b733-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-611">Az.Resources</span></span>
* <span data-ttu-id="2b733-612">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="2b733-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2b733-613">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2b733-613">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2b733-614">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="2b733-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2b733-615">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2b733-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2b733-616">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="2b733-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2b733-617">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2b733-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-618">Az.Sql</span></span>
* <span data-ttu-id="2b733-619">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="2b733-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-620">Az.Storage</span></span>
* <span data-ttu-id="2b733-621">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="2b733-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2b733-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b733-622">New-AzStorageContext</span></span>
* <span data-ttu-id="2b733-623">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="2b733-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2b733-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2b733-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2b733-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2b733-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2b733-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2b733-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2b733-628">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="2b733-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2b733-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2b733-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2b733-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2b733-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2b733-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2b733-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2b733-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2b733-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2b733-633">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2b733-634">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2b733-634">Highlights since the last major release</span></span>
* <span data-ttu-id="2b733-635">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2b733-635">General availability of `Az` module</span></span>
* <span data-ttu-id="2b733-636">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2b733-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2b733-637">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2b733-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2b733-638">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2b733-639">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2b733-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2b733-640">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2b733-641">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2b733-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-642">Az.Automation</span></span>
* <span data-ttu-id="2b733-643">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b733-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2b733-644">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="2b733-644">Dynamic grouping</span></span>
    * <span data-ttu-id="2b733-645">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="2b733-645">Pre-Post script</span></span>
    * <span data-ttu-id="2b733-646">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="2b733-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-647">Az.Compute</span></span>
* <span data-ttu-id="2b733-648">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="2b733-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2b733-649">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2b733-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2b733-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-650">Az.KeyVault</span></span>
* <span data-ttu-id="2b733-651">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-652">Az.Network</span></span>
* <span data-ttu-id="2b733-653">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2b733-654">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="2b733-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-656">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="2b733-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2b733-657">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="2b733-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-658">Az.Resources</span></span>
* <span data-ttu-id="2b733-659">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2b733-660">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="2b733-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-661">Az.Sql</span></span>
* <span data-ttu-id="2b733-662">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="2b733-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-663">Az.Storage</span></span>
* <span data-ttu-id="2b733-664">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2b733-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2b733-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2b733-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2b733-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2b733-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2b733-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2b733-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2b733-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2b733-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2b733-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-671">Az.Websites</span></span>
* <span data-ttu-id="2b733-672">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="2b733-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="2b733-673">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-674">Az.Accounts</span></span>
* <span data-ttu-id="2b733-675">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="2b733-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2b733-676">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-677">Az.Automation</span></span>
* <span data-ttu-id="2b733-678">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2b733-679">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="2b733-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2b733-680">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="2b733-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2b733-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2b733-681">Az.Cdn</span></span>
* <span data-ttu-id="2b733-682">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="2b733-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-683">Az.Compute</span></span>
* <span data-ttu-id="2b733-684">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="2b733-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2b733-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b733-685">Az.DataFactory</span></span>
* <span data-ttu-id="2b733-686">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2b733-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2b733-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2b733-687">Az.LogicApp</span></span>
* <span data-ttu-id="2b733-688">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="2b733-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-689">Az.Network</span></span>
* <span data-ttu-id="2b733-690">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="2b733-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-692">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2b733-693">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="2b733-693">SDK Update</span></span>
* <span data-ttu-id="2b733-694">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2b733-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2b733-695">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2b733-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-696">Az.Resources</span></span>
* <span data-ttu-id="2b733-697">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="2b733-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2b733-698">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2b733-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2b733-699">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2b733-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2b733-700">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2b733-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2b733-701">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2b733-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2b733-702">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2b733-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-703">Az.Sql</span></span>
* <span data-ttu-id="2b733-704">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2b733-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2b733-705">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="2b733-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-706">Az.Storage</span></span>
* <span data-ttu-id="2b733-707">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2b733-708">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2b733-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b733-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="2b733-710">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="2b733-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-711">Az.Automation</span></span>
* <span data-ttu-id="2b733-712">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2b733-713">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2b733-714">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2b733-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2b733-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="2b733-716">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b733-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-717">Az.Compute</span></span>
* <span data-ttu-id="2b733-718">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="2b733-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2b733-719">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="2b733-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2b733-720">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2b733-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2b733-721">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2b733-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-723">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="2b733-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2b733-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b733-724">Az.EventHub</span></span>
* <span data-ttu-id="2b733-725">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="2b733-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2b733-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-726">Az.KeyVault</span></span>
* <span data-ttu-id="2b733-727">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2b733-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2b733-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2b733-728">Az.LogicApp</span></span>
* <span data-ttu-id="2b733-729">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2b733-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2b733-730">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="2b733-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2b733-731">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2b733-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2b733-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b733-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2b733-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b733-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2b733-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b733-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2b733-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b733-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2b733-736">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2b733-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2b733-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2b733-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2b733-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2b733-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2b733-741">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2b733-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2b733-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2b733-742">Az.Monitor</span></span>
* <span data-ttu-id="2b733-743">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="2b733-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-744">Az.Network</span></span>
* <span data-ttu-id="2b733-745">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2b733-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2b733-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="2b733-747">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2b733-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2b733-748">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2b733-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2b733-749">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="2b733-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2b733-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-750">Az.Resources</span></span>
* <span data-ttu-id="2b733-751">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2b733-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2b733-752">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2b733-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2b733-753">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2b733-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2b733-754">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2b733-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-755">Az.Sql</span></span>
* <span data-ttu-id="2b733-756">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="2b733-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2b733-757">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="2b733-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-758">Az.Websites</span></span>
* <span data-ttu-id="2b733-759">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2b733-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2b733-760">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-761">Az.Accounts</span></span>
* <span data-ttu-id="2b733-762">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2b733-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2b733-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b733-763">Az.AnalysisServices</span></span>
<span data-ttu-id="2b733-764">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2b733-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-765">Az.Compute</span></span>
* <span data-ttu-id="2b733-766">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="2b733-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2b733-767">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2b733-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2b733-768">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2b733-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-769">Az.RecoveryServices</span></span>
<span data-ttu-id="2b733-770">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2b733-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-771">Az.Resources</span></span>
* <span data-ttu-id="2b733-772">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="2b733-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2b733-773">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2b733-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2b733-774">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2b733-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2b733-775">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2b733-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-776">Az.Sql</span></span>
* <span data-ttu-id="2b733-777">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b733-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2b733-778">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="2b733-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2b733-779">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2b733-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2b733-780">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-781">Az.Accounts</span></span>
* <span data-ttu-id="2b733-782">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2b733-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2b733-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b733-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="2b733-784">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2b733-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="2b733-786">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2b733-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2b733-787">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-788">Az.Accounts</span></span>
* <span data-ttu-id="2b733-789">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2b733-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2b733-790">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2b733-791">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2b733-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2b733-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2b733-792">Az.Aks</span></span>
* <span data-ttu-id="2b733-793">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2b733-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-794">Az.Automation</span></span>
* <span data-ttu-id="2b733-795">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="2b733-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2b733-796">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2b733-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2b733-797">Az.Cdn</span></span>
* <span data-ttu-id="2b733-798">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-799">Az.Compute</span></span>
* <span data-ttu-id="2b733-800">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2b733-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2b733-801">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2b733-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2b733-802">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b733-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2b733-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b733-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2b733-804">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2b733-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b733-805">Az.DataFactory</span></span>
* <span data-ttu-id="2b733-806">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2b733-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-808">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="2b733-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2b733-809">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2b733-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2b733-810">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2b733-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2b733-811">Az.IotHub</span></span>
* <span data-ttu-id="2b733-812">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2b733-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2b733-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-813">Az.KeyVault</span></span>
* <span data-ttu-id="2b733-814">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-815">Az.Network</span></span>
* <span data-ttu-id="2b733-816">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-817">Az.Resources</span></span>
* <span data-ttu-id="2b733-818">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="2b733-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2b733-819">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2b733-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2b733-820">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="2b733-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2b733-821">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2b733-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2b733-822">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2b733-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2b733-823">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="2b733-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2b733-824">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2b733-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2b733-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="2b733-826">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2b733-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2b733-827">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="2b733-827">Fix some error messages.</span></span>
* <span data-ttu-id="2b733-828">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="2b733-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2b733-829">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="2b733-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2b733-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2b733-830">Az.SignalR</span></span>
* <span data-ttu-id="2b733-831">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-832">Az.Sql</span></span>
* <span data-ttu-id="2b733-833">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2b733-834">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="2b733-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2b733-835">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="2b733-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2b733-836">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="2b733-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-837">Az.Storage</span></span>
* <span data-ttu-id="2b733-838">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2b733-839">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="2b733-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2b733-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2b733-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2b733-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2b733-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2b733-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2b733-842">Az.TrafficManager</span></span>
* <span data-ttu-id="2b733-843">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-844">Az.Websites</span></span>
* <span data-ttu-id="2b733-845">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2b733-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2b733-846">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2b733-847">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="2b733-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2b733-848">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2b733-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2b733-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-849">Az.Accounts</span></span>
* <span data-ttu-id="2b733-850">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2b733-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-851">Az.Compute</span></span>
* <span data-ttu-id="2b733-852">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2b733-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2b733-853">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2b733-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2b733-854">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-856">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="2b733-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2b733-857">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="2b733-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2b733-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2b733-858">Az.EventGrid</span></span>
* <span data-ttu-id="2b733-859">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2b733-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2b733-860">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2b733-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2b733-861">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2b733-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2b733-862">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="2b733-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2b733-863">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="2b733-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2b733-864">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="2b733-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2b733-865">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2b733-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2b733-866">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="2b733-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2b733-867">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="2b733-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2b733-868">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="2b733-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="2b733-869">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2b733-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2b733-870">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2b733-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2b733-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2b733-871">Az.IotHub</span></span>
* <span data-ttu-id="2b733-872">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="2b733-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2b733-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2b733-873">Az.LogicApp</span></span>
* <span data-ttu-id="2b733-874">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="2b733-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-875">Az.Resources</span></span>
* <span data-ttu-id="2b733-876">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="2b733-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2b733-877">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2b733-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2b733-878">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b733-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2b733-879">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2b733-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2b733-880">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="2b733-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2b733-881">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2b733-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2b733-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2b733-882">Az.SignalR</span></span>
* <span data-ttu-id="2b733-883">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-884">Az.Sql</span></span>
* <span data-ttu-id="2b733-885">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="2b733-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2b733-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-886">Az.Storage</span></span>
* <span data-ttu-id="2b733-887">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="2b733-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2b733-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b733-888">New-AzStorageContext</span></span>
* <span data-ttu-id="2b733-889">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="2b733-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2b733-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2b733-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-891">Az.Websites</span></span>
* <span data-ttu-id="2b733-892">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="2b733-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2b733-893">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2b733-894">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2b733-895">Generale</span><span class="sxs-lookup"><span data-stu-id="2b733-895">General</span></span>

- <span data-ttu-id="2b733-896">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="2b733-896">General Availability of Az Module</span></span>
- <span data-ttu-id="2b733-897">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="2b733-897">Online help for each module</span></span>
- <span data-ttu-id="2b733-898">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2b733-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2b733-899">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="2b733-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2b733-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-900">Az.Accounts</span></span>
- <span data-ttu-id="2b733-901">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2b733-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="2b733-902">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="2b733-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2b733-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-903">Az.ApiManagement</span></span>
- <span data-ttu-id="2b733-904">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="2b733-904">Fixes for #7002</span></span>
- <span data-ttu-id="2b733-905">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2b733-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2b733-906">Az.Batch</span></span>
- <span data-ttu-id="2b733-907">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2b733-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2b733-908">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="2b733-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2b733-909">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2b733-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2b733-910">Az.Billing</span></span>
- <span data-ttu-id="2b733-911">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2b733-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2b733-912">Az.CognitivServices</span></span>
- <span data-ttu-id="2b733-913">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2b733-914">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2b733-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2b733-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="2b733-916">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2b733-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2b733-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2b733-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2b733-918">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2b733-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="2b733-920">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2b733-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2b733-921">Az.Monitor</span></span>
- <span data-ttu-id="2b733-922">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2b733-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b733-923">Az.KeyVault</span></span>
- <span data-ttu-id="2b733-924">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="2b733-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2b733-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2b733-925">Az.MachineLearning</span></span>
- <span data-ttu-id="2b733-926">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2b733-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2b733-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2b733-927">Az.Media</span></span>
- <span data-ttu-id="2b733-928">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2b733-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2b733-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-929">Az.Network</span></span>
<span data-ttu-id="2b733-930">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2b733-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2b733-931">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2b733-931">New cmdlets added:</span></span>
        - <span data-ttu-id="2b733-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2b733-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2b733-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2b733-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2b733-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b733-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2b733-940">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b733-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2b733-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b733-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2b733-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2b733-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2b733-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2b733-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2b733-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2b733-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2b733-946">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="2b733-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2b733-947">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2b733-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2b733-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2b733-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2b733-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2b733-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2b733-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2b733-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2b733-951">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2b733-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2b733-952">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2b733-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="2b733-954">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2b733-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2b733-955">Az.Profile</span></span>
- <span data-ttu-id="2b733-956">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2b733-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="2b733-958">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2b733-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-959">Az.Resources</span></span>
- <span data-ttu-id="2b733-960">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2b733-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="2b733-962">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="2b733-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2b733-963">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2b733-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2b733-964">Az.SIgnalR</span></span>
- <span data-ttu-id="2b733-965">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2b733-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2b733-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-966">Az.Sql</span></span>
- <span data-ttu-id="2b733-967">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="2b733-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2b733-968">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2b733-969">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2b733-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-970">Az.Storage</span></span>
- <span data-ttu-id="2b733-971">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2b733-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-972">Az.Websites</span></span>
- <span data-ttu-id="2b733-973">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2b733-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2b733-974">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2b733-975">Generale</span><span class="sxs-lookup"><span data-stu-id="2b733-975">General</span></span>

* <span data-ttu-id="2b733-976">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="2b733-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2b733-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-977">Az.Compute</span></span>

* <span data-ttu-id="2b733-978">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2b733-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2b733-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="2b733-980">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="2b733-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2b733-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2b733-981">Az.FrontDoor</span></span>

* <span data-ttu-id="2b733-982">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="2b733-982">Fixed some broken links</span></span>
    - <span data-ttu-id="2b733-983">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2b733-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2b733-984">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2b733-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2b733-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2b733-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="2b733-986">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2b733-987">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="2b733-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2b733-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-988">Az.Resources</span></span>

* <span data-ttu-id="2b733-989">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2b733-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2b733-990">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="2b733-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2b733-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-991">Az.Sql</span></span>

* <span data-ttu-id="2b733-992">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="2b733-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2b733-993">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="2b733-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2b733-994">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="2b733-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2b733-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-995">Az.Storage</span></span>

* <span data-ttu-id="2b733-996">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2b733-997">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="2b733-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2b733-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2b733-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2b733-999">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="2b733-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="2b733-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2b733-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2b733-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2b733-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2b733-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-1002">Az.Websites</span></span>

* <span data-ttu-id="2b733-1003">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b733-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2b733-1004">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="2b733-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2b733-1005">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b733-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2b733-1006">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2b733-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b733-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="2b733-1008">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b733-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2b733-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2b733-1009">Az.Automation</span></span>
* <span data-ttu-id="2b733-1010">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="2b733-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2b733-1011">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="2b733-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2b733-1012">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="2b733-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2b733-1013">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="2b733-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2b733-1014">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="2b733-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2b733-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-1015">Az.Compute</span></span>
* <span data-ttu-id="2b733-1016">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2b733-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2b733-1017">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b733-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2b733-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="2b733-1019">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b733-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2b733-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2b733-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2b733-1021">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="2b733-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2b733-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-1022">Az.Network</span></span>
* <span data-ttu-id="2b733-1023">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2b733-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2b733-1024">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="2b733-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2b733-1025">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b733-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2b733-1026">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b733-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2b733-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2b733-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2b733-1028">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="2b733-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2b733-1029">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="2b733-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2b733-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2b733-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2b733-1031">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2b733-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2b733-1032">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b733-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2b733-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2b733-1033">Az.Relay</span></span>
* <span data-ttu-id="2b733-1034">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2b733-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2b733-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-1035">Az.Resources</span></span>
* <span data-ttu-id="2b733-1036">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2b733-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2b733-1037">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="2b733-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2b733-1038">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2b733-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2b733-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="2b733-1040">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="2b733-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2b733-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-1041">Az.Sql</span></span>
* <span data-ttu-id="2b733-1042">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="2b733-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2b733-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2b733-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2b733-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2b733-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2b733-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2b733-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2b733-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2b733-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2b733-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2b733-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2b733-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2b733-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2b733-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2b733-1051">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="2b733-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2b733-1052">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="2b733-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2b733-1053">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="2b733-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2b733-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2b733-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2b733-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2b733-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2b733-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2b733-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2b733-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2b733-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2b733-1058">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2b733-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2b733-1059">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2b733-1060">Generale</span><span class="sxs-lookup"><span data-stu-id="2b733-1060">General</span></span>
* <span data-ttu-id="2b733-1061">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="2b733-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2b733-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2b733-1062">Az.Profile</span></span>
* <span data-ttu-id="2b733-1063">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2b733-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2b733-1064">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="2b733-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2b733-1065">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2b733-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2b733-1066">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="2b733-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2b733-1067">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="2b733-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2b733-1068">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="2b733-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2b733-1069">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="2b733-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2b733-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2b733-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="2b733-1071">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2b733-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-1072">Az.Compute</span></span>
* <span data-ttu-id="2b733-1073">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2b733-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2b733-1074">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2b733-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2b733-1075">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="2b733-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-1077">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2b733-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2b733-1078">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="2b733-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2b733-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2b733-1079">Az.Insights</span></span>
* <span data-ttu-id="2b733-1080">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="2b733-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2b733-1081">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="2b733-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2b733-1082">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="2b733-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2b733-1083">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="2b733-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-1084">Az.Network</span></span>
* <span data-ttu-id="2b733-1085">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b733-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2b733-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b733-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2b733-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2b733-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2b733-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2b733-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2b733-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2b733-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2b733-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b733-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2b733-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2b733-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2b733-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2b733-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="2b733-1093">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="2b733-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-1094">Az.Resources</span></span>
* <span data-ttu-id="2b733-1095">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2b733-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2b733-1096">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="2b733-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2b733-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b733-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="2b733-1098">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="2b733-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2b733-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b733-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="2b733-1100">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="2b733-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2b733-1101">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="2b733-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2b733-1102">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2b733-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2b733-1103">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2b733-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2b733-1104">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2b733-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2b733-1105">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2b733-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2b733-1106">Az.Profile</span></span>
* <span data-ttu-id="2b733-1107">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="2b733-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2b733-1108">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2b733-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-1109">Az.Compute</span></span>
* <span data-ttu-id="2b733-1110">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="2b733-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2b733-1111">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b733-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2b733-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b733-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="2b733-1113">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2b733-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2b733-1114">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b733-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2b733-1115">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="2b733-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2b733-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="2b733-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2b733-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b733-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-1118">Az.Network</span></span>
* <span data-ttu-id="2b733-1119">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="2b733-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2b733-1120">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b733-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-1121">Az.Resources</span></span>
* <span data-ttu-id="2b733-1122">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="2b733-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2b733-1123">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="2b733-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2b733-1124">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2b733-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2b733-1125">Azure.Storage</span></span>
* <span data-ttu-id="2b733-1126">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="2b733-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2b733-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2b733-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2b733-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2b733-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2b733-1129">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="2b733-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2b733-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2b733-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2b733-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2b733-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="2b733-1132">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="2b733-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2b733-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2b733-1133">Az.Compute</span></span>
* <span data-ttu-id="2b733-1134">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="2b733-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2b733-1135">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2b733-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2b733-1136">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="2b733-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2b733-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2b733-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2b733-1138">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="2b733-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2b733-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2b733-1139">Az.Network</span></span>
* <span data-ttu-id="2b733-1140">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2b733-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2b733-1141">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b733-1141">new cmdlets added</span></span>
    - <span data-ttu-id="2b733-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2b733-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2b733-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2b733-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2b733-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2b733-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2b733-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2b733-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2b733-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2b733-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2b733-1148">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="2b733-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2b733-1149">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b733-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2b733-1150">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2b733-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2b733-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2b733-1151">Az.RedisCache</span></span>
* <span data-ttu-id="2b733-1152">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="2b733-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2b733-1153">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2b733-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2b733-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2b733-1154">Az.Resources</span></span>
* <span data-ttu-id="2b733-1155">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b733-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2b733-1156">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="2b733-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2b733-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2b733-1157">Az.Sql</span></span>
* <span data-ttu-id="2b733-1158">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="2b733-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2b733-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2b733-1159">Az.Websites</span></span>
* <span data-ttu-id="2b733-1160">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="2b733-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2b733-1161">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="2b733-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2b733-1162">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="2b733-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2b733-1163">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="2b733-1163">Initial Release</span></span>