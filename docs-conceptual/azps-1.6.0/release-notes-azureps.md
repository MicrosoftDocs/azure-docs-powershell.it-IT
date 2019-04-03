---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475391"
---
## <a name="160---march-2019"></a><span data-ttu-id="ec4dd-101">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ec4dd-102">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-102">Highlights since the last major release</span></span>
* <span data-ttu-id="ec4dd-103">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ec4dd-103">General availability of `Az` module</span></span>
* <span data-ttu-id="ec4dd-104">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ec4dd-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ec4dd-105">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ec4dd-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ec4dd-106">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ec4dd-107">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ec4dd-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ec4dd-108">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ec4dd-109">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ec4dd-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ec4dd-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-110">Az.Automation</span></span>
* <span data-ttu-id="ec4dd-111">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec4dd-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ec4dd-112">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="ec4dd-112">Dynamic grouping</span></span>
    * <span data-ttu-id="ec4dd-113">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="ec4dd-113">Pre-Post script</span></span>
    * <span data-ttu-id="ec4dd-114">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="ec4dd-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-115">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-116">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ec4dd-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ec4dd-117">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ec4dd-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec4dd-118">Az.KeyVault</span></span>
* <span data-ttu-id="ec4dd-119">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec4dd-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-120">Az.Network</span></span>
* <span data-ttu-id="ec4dd-121">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ec4dd-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ec4dd-122">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="ec4dd-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="ec4dd-124">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="ec4dd-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ec4dd-125">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="ec4dd-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-126">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-127">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec4dd-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ec4dd-128">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="ec4dd-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-129">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-130">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ec4dd-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-131">Az.Storage</span></span>
* <span data-ttu-id="ec4dd-132">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ec4dd-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ec4dd-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ec4dd-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ec4dd-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ec4dd-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ec4dd-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ec4dd-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ec4dd-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ec4dd-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ec4dd-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-139">Az.Websites</span></span>
* <span data-ttu-id="ec4dd-140">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="ec4dd-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ec4dd-141">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ec4dd-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-142">Az.Accounts</span></span>
* <span data-ttu-id="ec4dd-143">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="ec4dd-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ec4dd-144">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ec4dd-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ec4dd-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-145">Az.Automation</span></span>
* <span data-ttu-id="ec4dd-146">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ec4dd-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ec4dd-147">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ec4dd-148">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ec4dd-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ec4dd-149">Az.Cdn</span></span>
* <span data-ttu-id="ec4dd-150">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="ec4dd-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-151">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-152">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="ec4dd-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ec4dd-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ec4dd-153">Az.DataFactory</span></span>
* <span data-ttu-id="ec4dd-154">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ec4dd-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ec4dd-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ec4dd-155">Az.LogicApp</span></span>
* <span data-ttu-id="ec4dd-156">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="ec4dd-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-157">Az.Network</span></span>
* <span data-ttu-id="ec4dd-158">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="ec4dd-160">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="ec4dd-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ec4dd-161">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="ec4dd-161">SDK Update</span></span>
* <span data-ttu-id="ec4dd-162">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ec4dd-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ec4dd-163">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ec4dd-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-164">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-165">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ec4dd-166">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ec4dd-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ec4dd-167">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ec4dd-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ec4dd-168">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ec4dd-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ec4dd-169">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ec4dd-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ec4dd-170">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ec4dd-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-171">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-172">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ec4dd-173">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ec4dd-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-174">Az.Storage</span></span>
* <span data-ttu-id="ec4dd-175">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec4dd-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ec4dd-176">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ec4dd-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="ec4dd-178">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="ec4dd-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ec4dd-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-179">Az.Automation</span></span>
* <span data-ttu-id="ec4dd-180">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ec4dd-181">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ec4dd-182">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ec4dd-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="ec4dd-184">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-185">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-186">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="ec4dd-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ec4dd-187">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="ec4dd-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ec4dd-188">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ec4dd-189">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="ec4dd-191">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="ec4dd-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ec4dd-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ec4dd-192">Az.EventHub</span></span>
* <span data-ttu-id="ec4dd-193">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="ec4dd-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ec4dd-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec4dd-194">Az.KeyVault</span></span>
* <span data-ttu-id="ec4dd-195">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ec4dd-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ec4dd-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ec4dd-196">Az.LogicApp</span></span>
* <span data-ttu-id="ec4dd-197">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ec4dd-198">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="ec4dd-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ec4dd-199">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ec4dd-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ec4dd-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ec4dd-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ec4dd-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ec4dd-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ec4dd-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ec4dd-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ec4dd-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ec4dd-204">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ec4dd-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ec4dd-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ec4dd-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ec4dd-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ec4dd-209">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ec4dd-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ec4dd-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ec4dd-210">Az.Monitor</span></span>
* <span data-ttu-id="ec4dd-211">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ec4dd-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-212">Az.Network</span></span>
* <span data-ttu-id="ec4dd-213">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec4dd-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ec4dd-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ec4dd-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="ec4dd-215">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ec4dd-216">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ec4dd-217">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ec4dd-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-218">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-219">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ec4dd-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ec4dd-220">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ec4dd-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ec4dd-221">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ec4dd-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ec4dd-222">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ec4dd-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-223">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-224">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="ec4dd-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ec4dd-225">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="ec4dd-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ec4dd-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-226">Az.Websites</span></span>
* <span data-ttu-id="ec4dd-227">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ec4dd-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ec4dd-228">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ec4dd-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-229">Az.Accounts</span></span>
* <span data-ttu-id="ec4dd-230">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ec4dd-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ec4dd-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-231">Az.AnalysisServices</span></span>
<span data-ttu-id="ec4dd-232">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-233">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-234">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="ec4dd-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ec4dd-235">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ec4dd-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ec4dd-236">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-237">Az.RecoveryServices</span></span>
<span data-ttu-id="ec4dd-238">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-239">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-240">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ec4dd-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ec4dd-241">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ec4dd-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ec4dd-242">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ec4dd-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ec4dd-243">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ec4dd-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-244">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-245">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ec4dd-246">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="ec4dd-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ec4dd-247">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ec4dd-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ec4dd-248">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ec4dd-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-249">Az.Accounts</span></span>
* <span data-ttu-id="ec4dd-250">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ec4dd-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="ec4dd-252">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="ec4dd-254">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ec4dd-255">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ec4dd-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-256">Az.Accounts</span></span>
* <span data-ttu-id="ec4dd-257">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ec4dd-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ec4dd-258">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ec4dd-259">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ec4dd-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ec4dd-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ec4dd-260">Az.Aks</span></span>
* <span data-ttu-id="ec4dd-261">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ec4dd-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-262">Az.Automation</span></span>
* <span data-ttu-id="ec4dd-263">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="ec4dd-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ec4dd-264">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ec4dd-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ec4dd-265">Az.Cdn</span></span>
* <span data-ttu-id="ec4dd-266">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-267">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-268">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ec4dd-269">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ec4dd-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ec4dd-270">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec4dd-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ec4dd-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ec4dd-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ec4dd-272">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ec4dd-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ec4dd-273">Az.DataFactory</span></span>
* <span data-ttu-id="ec4dd-274">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ec4dd-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="ec4dd-276">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ec4dd-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ec4dd-277">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ec4dd-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ec4dd-278">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ec4dd-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ec4dd-279">Az.IotHub</span></span>
* <span data-ttu-id="ec4dd-280">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ec4dd-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec4dd-281">Az.KeyVault</span></span>
* <span data-ttu-id="ec4dd-282">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-283">Az.Network</span></span>
* <span data-ttu-id="ec4dd-284">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-285">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-286">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="ec4dd-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ec4dd-287">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ec4dd-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ec4dd-288">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ec4dd-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ec4dd-289">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ec4dd-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ec4dd-290">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ec4dd-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ec4dd-291">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="ec4dd-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ec4dd-292">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ec4dd-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ec4dd-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ec4dd-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="ec4dd-294">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ec4dd-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ec4dd-295">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-295">Fix some error messages.</span></span>
* <span data-ttu-id="ec4dd-296">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ec4dd-297">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ec4dd-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ec4dd-298">Az.SignalR</span></span>
* <span data-ttu-id="ec4dd-299">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-300">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-301">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ec4dd-302">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="ec4dd-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ec4dd-303">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="ec4dd-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ec4dd-304">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ec4dd-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ec4dd-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-305">Az.Storage</span></span>
* <span data-ttu-id="ec4dd-306">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ec4dd-307">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ec4dd-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ec4dd-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ec4dd-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ec4dd-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ec4dd-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ec4dd-310">Az.TrafficManager</span></span>
* <span data-ttu-id="ec4dd-311">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ec4dd-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-312">Az.Websites</span></span>
* <span data-ttu-id="ec4dd-313">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ec4dd-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ec4dd-314">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ec4dd-315">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="ec4dd-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ec4dd-316">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ec4dd-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ec4dd-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-317">Az.Accounts</span></span>
* <span data-ttu-id="ec4dd-318">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ec4dd-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-319">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-320">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ec4dd-321">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ec4dd-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ec4dd-322">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="ec4dd-324">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ec4dd-325">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="ec4dd-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ec4dd-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ec4dd-326">Az.EventGrid</span></span>
* <span data-ttu-id="ec4dd-327">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ec4dd-328">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ec4dd-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ec4dd-329">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ec4dd-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ec4dd-330">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ec4dd-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ec4dd-331">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ec4dd-332">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ec4dd-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ec4dd-333">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ec4dd-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ec4dd-334">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ec4dd-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ec4dd-335">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ec4dd-336">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ec4dd-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="ec4dd-337">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ec4dd-338">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ec4dd-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ec4dd-339">Az.IotHub</span></span>
* <span data-ttu-id="ec4dd-340">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="ec4dd-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ec4dd-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ec4dd-341">Az.LogicApp</span></span>
* <span data-ttu-id="ec4dd-342">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="ec4dd-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-343">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-344">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ec4dd-345">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ec4dd-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ec4dd-346">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ec4dd-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ec4dd-347">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ec4dd-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ec4dd-348">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ec4dd-349">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ec4dd-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ec4dd-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ec4dd-350">Az.SignalR</span></span>
* <span data-ttu-id="ec4dd-351">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-352">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-353">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ec4dd-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-354">Az.Storage</span></span>
* <span data-ttu-id="ec4dd-355">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="ec4dd-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ec4dd-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec4dd-356">New-AzStorageContext</span></span>
* <span data-ttu-id="ec4dd-357">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="ec4dd-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ec4dd-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ec4dd-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ec4dd-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-359">Az.Websites</span></span>
* <span data-ttu-id="ec4dd-360">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ec4dd-361">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ec4dd-362">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ec4dd-363">Generale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-363">General</span></span>

- <span data-ttu-id="ec4dd-364">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="ec4dd-364">General Availability of Az Module</span></span>
- <span data-ttu-id="ec4dd-365">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="ec4dd-365">Online help for each module</span></span>
- <span data-ttu-id="ec4dd-366">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ec4dd-367">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="ec4dd-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ec4dd-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-368">Az.Accounts</span></span>
- <span data-ttu-id="ec4dd-369">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="ec4dd-370">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="ec4dd-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ec4dd-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec4dd-371">Az.ApiManagement</span></span>
- <span data-ttu-id="ec4dd-372">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="ec4dd-372">Fixes for #7002</span></span>
- <span data-ttu-id="ec4dd-373">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ec4dd-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ec4dd-374">Az.Batch</span></span>
- <span data-ttu-id="ec4dd-375">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ec4dd-376">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ec4dd-377">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ec4dd-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ec4dd-378">Az.Billing</span></span>
- <span data-ttu-id="ec4dd-379">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ec4dd-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-380">Az.CognitivServices</span></span>
- <span data-ttu-id="ec4dd-381">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ec4dd-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ec4dd-382">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ec4dd-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ec4dd-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="ec4dd-384">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ec4dd-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ec4dd-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ec4dd-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ec4dd-386">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="ec4dd-388">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ec4dd-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ec4dd-389">Az.Monitor</span></span>
- <span data-ttu-id="ec4dd-390">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ec4dd-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec4dd-391">Az.KeyVault</span></span>
- <span data-ttu-id="ec4dd-392">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="ec4dd-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ec4dd-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ec4dd-393">Az.MachineLearning</span></span>
- <span data-ttu-id="ec4dd-394">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ec4dd-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ec4dd-395">Az.Media</span></span>
- <span data-ttu-id="ec4dd-396">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ec4dd-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ec4dd-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-397">Az.Network</span></span>
<span data-ttu-id="ec4dd-398">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ec4dd-399">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ec4dd-399">New cmdlets added:</span></span>
        - <span data-ttu-id="ec4dd-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ec4dd-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ec4dd-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ec4dd-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4dd-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ec4dd-408">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ec4dd-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec4dd-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ec4dd-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec4dd-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ec4dd-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec4dd-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ec4dd-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec4dd-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ec4dd-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ec4dd-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ec4dd-414">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ec4dd-415">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ec4dd-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ec4dd-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec4dd-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ec4dd-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec4dd-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ec4dd-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec4dd-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ec4dd-419">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ec4dd-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ec4dd-420">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ec4dd-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ec4dd-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="ec4dd-422">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ec4dd-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-423">Az.Profile</span></span>
- <span data-ttu-id="ec4dd-424">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ec4dd-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="ec4dd-426">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ec4dd-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-427">Az.Resources</span></span>
- <span data-ttu-id="ec4dd-428">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ec4dd-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ec4dd-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="ec4dd-430">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ec4dd-431">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ec4dd-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ec4dd-432">Az.SIgnalR</span></span>
- <span data-ttu-id="ec4dd-433">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ec4dd-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ec4dd-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-434">Az.Sql</span></span>
- <span data-ttu-id="ec4dd-435">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="ec4dd-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ec4dd-436">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ec4dd-437">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ec4dd-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-438">Az.Storage</span></span>
- <span data-ttu-id="ec4dd-439">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ec4dd-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-440">Az.Websites</span></span>
- <span data-ttu-id="ec4dd-441">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ec4dd-442">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ec4dd-443">Generale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-443">General</span></span>

* <span data-ttu-id="ec4dd-444">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ec4dd-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ec4dd-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-445">Az.Compute</span></span>

* <span data-ttu-id="ec4dd-446">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="ec4dd-448">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="ec4dd-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ec4dd-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ec4dd-449">Az.FrontDoor</span></span>

* <span data-ttu-id="ec4dd-450">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ec4dd-450">Fixed some broken links</span></span>
    - <span data-ttu-id="ec4dd-451">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ec4dd-452">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ec4dd-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="ec4dd-454">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ec4dd-455">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ec4dd-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-456">Az.Resources</span></span>

* <span data-ttu-id="ec4dd-457">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ec4dd-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ec4dd-458">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ec4dd-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-459">Az.Sql</span></span>

* <span data-ttu-id="ec4dd-460">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ec4dd-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ec4dd-461">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="ec4dd-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ec4dd-462">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ec4dd-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-463">Az.Storage</span></span>

* <span data-ttu-id="ec4dd-464">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec4dd-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ec4dd-465">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="ec4dd-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ec4dd-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ec4dd-467">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="ec4dd-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="ec4dd-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ec4dd-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ec4dd-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ec4dd-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ec4dd-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-470">Az.Websites</span></span>

* <span data-ttu-id="ec4dd-471">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec4dd-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ec4dd-472">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ec4dd-473">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ec4dd-474">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ec4dd-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec4dd-475">Az.ApiManagement</span></span>
* <span data-ttu-id="ec4dd-476">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ec4dd-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ec4dd-477">Az.Automation</span></span>
* <span data-ttu-id="ec4dd-478">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="ec4dd-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ec4dd-479">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ec4dd-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ec4dd-480">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="ec4dd-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ec4dd-481">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ec4dd-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ec4dd-482">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="ec4dd-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ec4dd-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-483">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-484">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ec4dd-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ec4dd-485">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ec4dd-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="ec4dd-487">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ec4dd-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ec4dd-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ec4dd-489">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="ec4dd-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ec4dd-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-490">Az.Network</span></span>
* <span data-ttu-id="ec4dd-491">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ec4dd-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ec4dd-492">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="ec4dd-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ec4dd-493">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ec4dd-494">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ec4dd-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ec4dd-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ec4dd-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ec4dd-496">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ec4dd-497">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ec4dd-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ec4dd-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ec4dd-499">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ec4dd-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ec4dd-500">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec4dd-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ec4dd-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ec4dd-501">Az.Relay</span></span>
* <span data-ttu-id="ec4dd-502">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ec4dd-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-503">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-504">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ec4dd-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ec4dd-505">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="ec4dd-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ec4dd-506">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ec4dd-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ec4dd-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ec4dd-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="ec4dd-508">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ec4dd-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-509">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-510">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="ec4dd-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ec4dd-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ec4dd-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ec4dd-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ec4dd-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ec4dd-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ec4dd-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4dd-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ec4dd-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4dd-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ec4dd-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4dd-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ec4dd-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4dd-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ec4dd-519">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ec4dd-520">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ec4dd-521">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ec4dd-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ec4dd-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ec4dd-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ec4dd-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ec4dd-526">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ec4dd-527">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ec4dd-528">Generale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-528">General</span></span>
* <span data-ttu-id="ec4dd-529">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="ec4dd-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ec4dd-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-530">Az.Profile</span></span>
* <span data-ttu-id="ec4dd-531">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ec4dd-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ec4dd-532">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="ec4dd-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ec4dd-533">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ec4dd-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ec4dd-534">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="ec4dd-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ec4dd-535">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="ec4dd-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ec4dd-536">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ec4dd-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ec4dd-537">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="ec4dd-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ec4dd-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="ec4dd-539">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-540">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-541">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ec4dd-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ec4dd-542">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ec4dd-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ec4dd-543">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="ec4dd-545">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ec4dd-546">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ec4dd-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ec4dd-547">Az.Insights</span></span>
* <span data-ttu-id="ec4dd-548">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="ec4dd-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ec4dd-549">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="ec4dd-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ec4dd-550">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ec4dd-551">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="ec4dd-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-552">Az.Network</span></span>
* <span data-ttu-id="ec4dd-553">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec4dd-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ec4dd-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec4dd-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ec4dd-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ec4dd-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ec4dd-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ec4dd-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ec4dd-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ec4dd-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ec4dd-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec4dd-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ec4dd-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ec4dd-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ec4dd-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ec4dd-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="ec4dd-561">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="ec4dd-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-562">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-563">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ec4dd-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ec4dd-564">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ec4dd-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ec4dd-565">Az.ServiceBus</span></span>
* <span data-ttu-id="ec4dd-566">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ec4dd-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ec4dd-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="ec4dd-568">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ec4dd-569">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ec4dd-570">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ec4dd-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ec4dd-571">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ec4dd-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ec4dd-572">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ec4dd-573">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ec4dd-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-574">Az.Profile</span></span>
* <span data-ttu-id="ec4dd-575">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="ec4dd-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ec4dd-576">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ec4dd-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-577">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-578">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="ec4dd-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ec4dd-579">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ec4dd-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ec4dd-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="ec4dd-581">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ec4dd-582">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ec4dd-583">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ec4dd-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ec4dd-585">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-586">Az.Network</span></span>
* <span data-ttu-id="ec4dd-587">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ec4dd-588">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-589">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-590">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ec4dd-591">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ec4dd-592">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ec4dd-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-593">Azure.Storage</span></span>
* <span data-ttu-id="ec4dd-594">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="ec4dd-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ec4dd-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ec4dd-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ec4dd-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ec4dd-597">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="ec4dd-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ec4dd-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ec4dd-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ec4dd-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ec4dd-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="ec4dd-600">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ec4dd-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ec4dd-601">Az.Compute</span></span>
* <span data-ttu-id="ec4dd-602">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="ec4dd-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ec4dd-603">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ec4dd-604">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="ec4dd-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ec4dd-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec4dd-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ec4dd-606">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ec4dd-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ec4dd-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ec4dd-607">Az.Network</span></span>
* <span data-ttu-id="ec4dd-608">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ec4dd-609">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-609">new cmdlets added</span></span>
    - <span data-ttu-id="ec4dd-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ec4dd-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ec4dd-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ec4dd-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec4dd-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ec4dd-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ec4dd-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ec4dd-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ec4dd-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ec4dd-616">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="ec4dd-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ec4dd-617">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ec4dd-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ec4dd-618">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ec4dd-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ec4dd-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ec4dd-619">Az.RedisCache</span></span>
* <span data-ttu-id="ec4dd-620">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="ec4dd-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ec4dd-621">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ec4dd-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ec4dd-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ec4dd-622">Az.Resources</span></span>
* <span data-ttu-id="ec4dd-623">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ec4dd-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ec4dd-624">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="ec4dd-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ec4dd-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ec4dd-625">Az.Sql</span></span>
* <span data-ttu-id="ec4dd-626">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="ec4dd-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ec4dd-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ec4dd-627">Az.Websites</span></span>
* <span data-ttu-id="ec4dd-628">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="ec4dd-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ec4dd-629">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="ec4dd-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ec4dd-630">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="ec4dd-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ec4dd-631">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="ec4dd-631">Initial Release</span></span>