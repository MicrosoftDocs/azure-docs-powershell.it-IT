---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882473"
---
## <a name="150---march-2019"></a><span data-ttu-id="f4bb4-101">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4bb4-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-102">Az.Accounts</span></span>
* <span data-ttu-id="f4bb4-103">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="f4bb4-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f4bb4-104">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f4bb4-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4bb4-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4bb4-105">Az.Automation</span></span>
* <span data-ttu-id="f4bb4-106">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f4bb4-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f4bb4-107">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f4bb4-108">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f4bb4-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4bb4-109">Az.Cdn</span></span>
* <span data-ttu-id="f4bb4-110">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="f4bb4-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-111">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-112">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="f4bb4-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4bb4-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4bb4-113">Az.DataFactory</span></span>
* <span data-ttu-id="f4bb4-114">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f4bb4-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4bb4-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4bb4-115">Az.LogicApp</span></span>
* <span data-ttu-id="f4bb4-116">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="f4bb4-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-117">Az.Network</span></span>
* <span data-ttu-id="f4bb4-118">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4bb4-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4bb4-120">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="f4bb4-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f4bb4-121">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="f4bb4-121">SDK Update</span></span>
* <span data-ttu-id="f4bb4-122">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4bb4-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f4bb4-123">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4bb4-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-124">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-125">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f4bb4-126">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f4bb4-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f4bb4-127">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f4bb4-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f4bb4-128">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f4bb4-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f4bb4-129">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f4bb4-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f4bb4-130">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f4bb4-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-131">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-132">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f4bb4-133">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4bb4-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-134">Az.Storage</span></span>
* <span data-ttu-id="f4bb4-135">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4bb4-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f4bb4-136">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f4bb4-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="f4bb4-138">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="f4bb4-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4bb4-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4bb4-139">Az.Automation</span></span>
* <span data-ttu-id="f4bb4-140">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f4bb4-141">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f4bb4-142">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4bb4-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4bb4-144">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-145">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-146">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="f4bb4-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f4bb4-147">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="f4bb4-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f4bb4-148">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f4bb4-149">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4bb4-151">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="f4bb4-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f4bb4-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f4bb4-152">Az.EventHub</span></span>
* <span data-ttu-id="f4bb4-153">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="f4bb4-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f4bb4-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4bb4-154">Az.KeyVault</span></span>
* <span data-ttu-id="f4bb4-155">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4bb4-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4bb4-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4bb4-156">Az.LogicApp</span></span>
* <span data-ttu-id="f4bb4-157">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f4bb4-158">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="f4bb4-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f4bb4-159">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f4bb4-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4bb4-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4bb4-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4bb4-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4bb4-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4bb4-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4bb4-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4bb4-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f4bb4-164">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f4bb4-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4bb4-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4bb4-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4bb4-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f4bb4-169">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f4bb4-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f4bb4-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4bb4-170">Az.Monitor</span></span>
* <span data-ttu-id="f4bb4-171">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="f4bb4-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-172">Az.Network</span></span>
* <span data-ttu-id="f4bb4-173">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4bb4-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f4bb4-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4bb4-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="f4bb4-175">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f4bb4-176">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f4bb4-177">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f4bb4-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-178">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-179">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f4bb4-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f4bb4-180">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f4bb4-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f4bb4-181">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f4bb4-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f4bb4-182">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="f4bb4-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-183">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-184">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="f4bb4-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f4bb4-185">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="f4bb4-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4bb4-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-186">Az.Websites</span></span>
* <span data-ttu-id="f4bb4-187">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f4bb4-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f4bb4-188">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4bb4-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-189">Az.Accounts</span></span>
* <span data-ttu-id="f4bb4-190">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4bb4-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f4bb4-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-191">Az.AnalysisServices</span></span>
<span data-ttu-id="f4bb4-192">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-193">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-194">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="f4bb4-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f4bb4-195">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f4bb4-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f4bb4-196">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4bb4-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-197">Az.RecoveryServices</span></span>
<span data-ttu-id="f4bb4-198">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-199">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-200">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="f4bb4-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f4bb4-201">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f4bb4-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f4bb4-202">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f4bb4-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f4bb4-203">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f4bb4-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-204">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-205">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4bb4-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f4bb4-206">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="f4bb4-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f4bb4-207">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f4bb4-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f4bb4-208">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4bb4-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-209">Az.Accounts</span></span>
* <span data-ttu-id="f4bb4-210">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f4bb4-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="f4bb4-212">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4bb4-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4bb4-214">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f4bb4-215">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4bb4-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-216">Az.Accounts</span></span>
* <span data-ttu-id="f4bb4-217">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f4bb4-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f4bb4-218">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4bb4-219">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f4bb4-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f4bb4-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f4bb4-220">Az.Aks</span></span>
* <span data-ttu-id="f4bb4-221">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4bb4-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4bb4-222">Az.Automation</span></span>
* <span data-ttu-id="f4bb4-223">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="f4bb4-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f4bb4-224">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f4bb4-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4bb4-225">Az.Cdn</span></span>
* <span data-ttu-id="f4bb4-226">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-227">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-228">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f4bb4-229">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4bb4-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f4bb4-230">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f4bb4-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f4bb4-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4bb4-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f4bb4-232">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4bb4-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4bb4-233">Az.DataFactory</span></span>
* <span data-ttu-id="f4bb4-234">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f4bb4-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4bb4-236">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="f4bb4-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f4bb4-237">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f4bb4-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f4bb4-238">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4bb4-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4bb4-239">Az.IotHub</span></span>
* <span data-ttu-id="f4bb4-240">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f4bb4-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4bb4-241">Az.KeyVault</span></span>
* <span data-ttu-id="f4bb4-242">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-243">Az.Network</span></span>
* <span data-ttu-id="f4bb4-244">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-245">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-246">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="f4bb4-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f4bb4-247">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f4bb4-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f4bb4-248">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f4bb4-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f4bb4-249">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f4bb4-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f4bb4-250">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f4bb4-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f4bb4-251">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="f4bb4-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f4bb4-252">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f4bb4-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4bb4-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4bb4-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4bb4-254">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f4bb4-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f4bb4-255">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-255">Fix some error messages.</span></span>
* <span data-ttu-id="f4bb4-256">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f4bb4-257">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f4bb4-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f4bb4-258">Az.SignalR</span></span>
* <span data-ttu-id="f4bb4-259">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-260">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-261">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4bb4-262">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="f4bb4-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f4bb4-263">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="f4bb4-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f4bb4-264">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="f4bb4-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4bb4-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-265">Az.Storage</span></span>
* <span data-ttu-id="f4bb4-266">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4bb4-267">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f4bb4-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f4bb4-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f4bb4-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f4bb4-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f4bb4-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f4bb4-270">Az.TrafficManager</span></span>
* <span data-ttu-id="f4bb4-271">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4bb4-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-272">Az.Websites</span></span>
* <span data-ttu-id="f4bb4-273">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f4bb4-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4bb4-274">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f4bb4-275">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="f4bb4-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f4bb4-276">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f4bb4-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4bb4-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-277">Az.Accounts</span></span>
* <span data-ttu-id="f4bb4-278">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f4bb4-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-279">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-280">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f4bb4-281">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="f4bb4-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f4bb4-282">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4bb4-284">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f4bb4-285">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="f4bb4-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f4bb4-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f4bb4-286">Az.EventGrid</span></span>
* <span data-ttu-id="f4bb4-287">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f4bb4-288">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f4bb4-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f4bb4-289">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="f4bb4-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f4bb4-290">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="f4bb4-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f4bb4-291">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f4bb4-292">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="f4bb4-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f4bb4-293">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="f4bb4-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f4bb4-294">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="f4bb4-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f4bb4-295">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f4bb4-296">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="f4bb4-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="f4bb4-297">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f4bb4-298">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4bb4-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4bb4-299">Az.IotHub</span></span>
* <span data-ttu-id="f4bb4-300">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="f4bb4-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4bb4-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4bb4-301">Az.LogicApp</span></span>
* <span data-ttu-id="f4bb4-302">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="f4bb4-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-303">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-304">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f4bb4-305">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f4bb4-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f4bb4-306">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bb4-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f4bb4-307">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f4bb4-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f4bb4-308">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f4bb4-309">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f4bb4-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f4bb4-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f4bb4-310">Az.SignalR</span></span>
* <span data-ttu-id="f4bb4-311">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-312">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-313">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4bb4-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-314">Az.Storage</span></span>
* <span data-ttu-id="f4bb4-315">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="f4bb4-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f4bb4-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f4bb4-316">New-AzStorageContext</span></span>
* <span data-ttu-id="f4bb4-317">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="f4bb4-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f4bb4-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f4bb4-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4bb4-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-319">Az.Websites</span></span>
* <span data-ttu-id="f4bb4-320">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f4bb4-321">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f4bb4-322">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f4bb4-323">Generale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-323">General</span></span>

- <span data-ttu-id="f4bb4-324">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="f4bb4-324">General Availability of Az Module</span></span>
- <span data-ttu-id="f4bb4-325">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="f4bb4-325">Online help for each module</span></span>
- <span data-ttu-id="f4bb4-326">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f4bb4-327">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="f4bb4-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f4bb4-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-328">Az.Accounts</span></span>
- <span data-ttu-id="f4bb4-329">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="f4bb4-330">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="f4bb4-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f4bb4-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4bb4-331">Az.ApiManagement</span></span>
- <span data-ttu-id="f4bb4-332">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="f4bb4-332">Fixes for #7002</span></span>
- <span data-ttu-id="f4bb4-333">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f4bb4-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f4bb4-334">Az.Batch</span></span>
- <span data-ttu-id="f4bb4-335">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f4bb4-336">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f4bb4-337">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f4bb4-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4bb4-338">Az.Billing</span></span>
- <span data-ttu-id="f4bb4-339">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f4bb4-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-340">Az.CognitivServices</span></span>
- <span data-ttu-id="f4bb4-341">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4bb4-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f4bb4-342">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f4bb4-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f4bb4-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="f4bb4-344">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f4bb4-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f4bb4-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f4bb4-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f4bb4-346">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="f4bb4-348">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f4bb4-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4bb4-349">Az.Monitor</span></span>
- <span data-ttu-id="f4bb4-350">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f4bb4-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4bb4-351">Az.KeyVault</span></span>
- <span data-ttu-id="f4bb4-352">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="f4bb4-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f4bb4-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f4bb4-353">Az.MachineLearning</span></span>
- <span data-ttu-id="f4bb4-354">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f4bb4-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f4bb4-355">Az.Media</span></span>
- <span data-ttu-id="f4bb4-356">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4bb4-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f4bb4-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-357">Az.Network</span></span>
<span data-ttu-id="f4bb4-358">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f4bb4-359">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="f4bb4-359">New cmdlets added:</span></span>
        - <span data-ttu-id="f4bb4-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f4bb4-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f4bb4-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f4bb4-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4bb4-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f4bb4-368">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f4bb4-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4bb4-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f4bb4-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f4bb4-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f4bb4-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f4bb4-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f4bb4-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4bb4-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f4bb4-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4bb4-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f4bb4-374">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f4bb4-375">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4bb4-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f4bb4-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4bb4-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f4bb4-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4bb4-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f4bb4-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4bb4-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f4bb4-379">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f4bb4-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f4bb4-380">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f4bb4-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4bb4-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="f4bb4-382">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f4bb4-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-383">Az.Profile</span></span>
- <span data-ttu-id="f4bb4-384">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4bb4-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f4bb4-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="f4bb4-386">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f4bb4-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-387">Az.Resources</span></span>
- <span data-ttu-id="f4bb4-388">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f4bb4-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4bb4-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="f4bb4-390">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f4bb4-391">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f4bb4-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f4bb4-392">Az.SIgnalR</span></span>
- <span data-ttu-id="f4bb4-393">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f4bb4-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f4bb4-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-394">Az.Sql</span></span>
- <span data-ttu-id="f4bb4-395">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="f4bb4-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f4bb4-396">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f4bb4-397">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f4bb4-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-398">Az.Storage</span></span>
- <span data-ttu-id="f4bb4-399">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f4bb4-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-400">Az.Websites</span></span>
- <span data-ttu-id="f4bb4-401">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f4bb4-402">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f4bb4-403">Generale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-403">General</span></span>

* <span data-ttu-id="f4bb4-404">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f4bb4-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f4bb4-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-405">Az.Compute</span></span>

* <span data-ttu-id="f4bb4-406">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="f4bb4-408">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="f4bb4-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f4bb4-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f4bb4-409">Az.FrontDoor</span></span>

* <span data-ttu-id="f4bb4-410">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="f4bb4-410">Fixed some broken links</span></span>
    - <span data-ttu-id="f4bb4-411">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f4bb4-412">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f4bb4-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="f4bb4-414">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f4bb4-415">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f4bb4-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-416">Az.Resources</span></span>

* <span data-ttu-id="f4bb4-417">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f4bb4-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f4bb4-418">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f4bb4-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-419">Az.Sql</span></span>

* <span data-ttu-id="f4bb4-420">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f4bb4-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f4bb4-421">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="f4bb4-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f4bb4-422">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f4bb4-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-423">Az.Storage</span></span>

* <span data-ttu-id="f4bb4-424">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4bb4-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f4bb4-425">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="f4bb4-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f4bb4-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f4bb4-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f4bb4-427">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="f4bb4-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="f4bb4-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f4bb4-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f4bb4-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f4bb4-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f4bb4-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-430">Az.Websites</span></span>

* <span data-ttu-id="f4bb4-431">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f4bb4-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f4bb4-432">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f4bb4-433">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f4bb4-434">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f4bb4-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4bb4-435">Az.ApiManagement</span></span>
* <span data-ttu-id="f4bb4-436">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f4bb4-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4bb4-437">Az.Automation</span></span>
* <span data-ttu-id="f4bb4-438">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="f4bb4-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f4bb4-439">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="f4bb4-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f4bb4-440">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="f4bb4-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f4bb4-441">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="f4bb4-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f4bb4-442">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="f4bb4-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f4bb4-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-443">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-444">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f4bb4-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f4bb4-445">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f4bb4-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="f4bb4-447">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f4bb4-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f4bb4-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f4bb4-449">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="f4bb4-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f4bb4-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-450">Az.Network</span></span>
* <span data-ttu-id="f4bb4-451">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f4bb4-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f4bb4-452">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="f4bb4-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f4bb4-453">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f4bb4-454">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4bb4-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f4bb4-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f4bb4-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f4bb4-456">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f4bb4-457">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f4bb4-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f4bb4-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f4bb4-459">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4bb4-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f4bb4-460">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4bb4-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f4bb4-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f4bb4-461">Az.Relay</span></span>
* <span data-ttu-id="f4bb4-462">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f4bb4-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-463">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-464">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f4bb4-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f4bb4-465">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="f4bb4-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f4bb4-466">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f4bb4-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f4bb4-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4bb4-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4bb4-468">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f4bb4-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-469">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-470">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="f4bb4-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f4bb4-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4bb4-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4bb4-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4bb4-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4bb4-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4bb4-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4bb4-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4bb4-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4bb4-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4bb4-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4bb4-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4bb4-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4bb4-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f4bb4-479">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f4bb4-480">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f4bb4-481">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f4bb4-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f4bb4-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f4bb4-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f4bb4-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f4bb4-486">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f4bb4-487">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f4bb4-488">Generale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-488">General</span></span>
* <span data-ttu-id="f4bb4-489">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="f4bb4-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f4bb4-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-490">Az.Profile</span></span>
* <span data-ttu-id="f4bb4-491">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4bb4-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f4bb4-492">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="f4bb4-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f4bb4-493">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f4bb4-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f4bb4-494">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="f4bb4-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f4bb4-495">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="f4bb4-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f4bb4-496">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="f4bb4-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f4bb4-497">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="f4bb4-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4bb4-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4bb4-499">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-500">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-501">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f4bb4-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f4bb4-502">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f4bb4-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f4bb4-503">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4bb4-505">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f4bb4-506">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f4bb4-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f4bb4-507">Az.Insights</span></span>
* <span data-ttu-id="f4bb4-508">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="f4bb4-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f4bb4-509">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="f4bb4-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f4bb4-510">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f4bb4-511">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="f4bb4-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-512">Az.Network</span></span>
* <span data-ttu-id="f4bb4-513">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4bb4-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f4bb4-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4bb4-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f4bb4-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f4bb4-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f4bb4-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4bb4-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f4bb4-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f4bb4-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f4bb4-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4bb4-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f4bb4-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4bb4-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f4bb4-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f4bb4-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="f4bb4-521">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="f4bb4-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-522">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-523">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f4bb4-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f4bb4-524">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f4bb4-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f4bb4-525">Az.ServiceBus</span></span>
* <span data-ttu-id="f4bb4-526">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4bb4-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4bb4-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4bb4-528">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f4bb4-529">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f4bb4-530">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f4bb4-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f4bb4-531">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f4bb4-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f4bb4-532">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f4bb4-533">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f4bb4-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-534">Az.Profile</span></span>
* <span data-ttu-id="f4bb4-535">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="f4bb4-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f4bb4-536">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4bb4-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-537">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-538">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="f4bb4-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f4bb4-539">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4bb4-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4bb4-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4bb4-541">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f4bb4-542">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f4bb4-543">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f4bb4-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f4bb4-545">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-546">Az.Network</span></span>
* <span data-ttu-id="f4bb4-547">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f4bb4-548">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-549">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-550">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f4bb4-551">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f4bb4-552">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f4bb4-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-553">Azure.Storage</span></span>
* <span data-ttu-id="f4bb4-554">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="f4bb4-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f4bb4-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f4bb4-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f4bb4-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f4bb4-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f4bb4-557">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="f4bb4-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f4bb4-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f4bb4-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f4bb4-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4bb4-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4bb4-560">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4bb4-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4bb4-561">Az.Compute</span></span>
* <span data-ttu-id="f4bb4-562">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="f4bb4-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f4bb4-563">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f4bb4-564">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="f4bb4-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f4bb4-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f4bb4-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f4bb4-566">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="f4bb4-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4bb4-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4bb4-567">Az.Network</span></span>
* <span data-ttu-id="f4bb4-568">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f4bb4-569">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-569">new cmdlets added</span></span>
    - <span data-ttu-id="f4bb4-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4bb4-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4bb4-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4bb4-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4bb4-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4bb4-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f4bb4-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f4bb4-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4bb4-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f4bb4-576">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="f4bb4-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f4bb4-577">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f4bb4-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f4bb4-578">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f4bb4-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f4bb4-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f4bb4-579">Az.RedisCache</span></span>
* <span data-ttu-id="f4bb4-580">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="f4bb4-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f4bb4-581">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f4bb4-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4bb4-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4bb4-582">Az.Resources</span></span>
* <span data-ttu-id="f4bb4-583">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4bb4-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f4bb4-584">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="f4bb4-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4bb4-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4bb4-585">Az.Sql</span></span>
* <span data-ttu-id="f4bb4-586">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="f4bb4-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4bb4-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4bb4-587">Az.Websites</span></span>
* <span data-ttu-id="f4bb4-588">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="f4bb4-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f4bb4-589">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="f4bb4-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f4bb4-590">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="f4bb4-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f4bb4-591">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="f4bb4-591">Initial Release</span></span>