---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364135"
---
## <a name="170---april-2019"></a><span data-ttu-id="0aee2-101">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0aee2-102">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0aee2-102">Highlights since the last major release</span></span>
* <span data-ttu-id="0aee2-103">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0aee2-103">General availability of `Az` module</span></span>
* <span data-ttu-id="0aee2-104">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0aee2-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0aee2-105">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0aee2-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0aee2-106">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0aee2-107">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0aee2-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0aee2-108">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0aee2-109">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0aee2-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0aee2-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-110">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-111">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0aee2-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0aee2-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="0aee2-113">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="0aee2-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0aee2-114">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0aee2-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0aee2-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-115">Az.Automation</span></span>
* <span data-ttu-id="0aee2-116">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="0aee2-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0aee2-117">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="0aee2-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0aee2-118">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0aee2-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-119">Az.Compute</span></span>
* <span data-ttu-id="0aee2-120">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0aee2-121">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="0aee2-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0aee2-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="0aee2-123">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="0aee2-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0aee2-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0aee2-124">Az.DataFactory</span></span>
* <span data-ttu-id="0aee2-125">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="0aee2-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0aee2-126">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0aee2-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-127">Az.Resources</span></span>
* <span data-ttu-id="0aee2-128">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="0aee2-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0aee2-129">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0aee2-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0aee2-130">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="0aee2-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0aee2-131">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0aee2-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0aee2-132">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="0aee2-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0aee2-133">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0aee2-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-134">Az.Sql</span></span>
* <span data-ttu-id="0aee2-135">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="0aee2-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0aee2-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-136">Az.Storage</span></span>
* <span data-ttu-id="0aee2-137">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="0aee2-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0aee2-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0aee2-138">New-AzStorageContext</span></span>
* <span data-ttu-id="0aee2-139">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="0aee2-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0aee2-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0aee2-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0aee2-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0aee2-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0aee2-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0aee2-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0aee2-144">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="0aee2-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0aee2-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0aee2-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0aee2-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0aee2-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0aee2-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0aee2-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0aee2-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0aee2-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0aee2-149">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0aee2-150">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0aee2-150">Highlights since the last major release</span></span>
* <span data-ttu-id="0aee2-151">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0aee2-151">General availability of `Az` module</span></span>
* <span data-ttu-id="0aee2-152">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0aee2-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0aee2-153">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0aee2-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0aee2-154">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0aee2-155">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0aee2-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0aee2-156">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0aee2-157">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0aee2-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0aee2-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-158">Az.Automation</span></span>
* <span data-ttu-id="0aee2-159">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0aee2-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0aee2-160">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="0aee2-160">Dynamic grouping</span></span>
    * <span data-ttu-id="0aee2-161">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="0aee2-161">Pre-Post script</span></span>
    * <span data-ttu-id="0aee2-162">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="0aee2-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-163">Az.Compute</span></span>
* <span data-ttu-id="0aee2-164">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0aee2-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0aee2-165">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0aee2-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0aee2-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0aee2-166">Az.KeyVault</span></span>
* <span data-ttu-id="0aee2-167">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="0aee2-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-168">Az.Network</span></span>
* <span data-ttu-id="0aee2-169">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0aee2-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0aee2-170">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="0aee2-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="0aee2-172">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="0aee2-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0aee2-173">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="0aee2-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-174">Az.Resources</span></span>
* <span data-ttu-id="0aee2-175">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0aee2-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0aee2-176">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="0aee2-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-177">Az.Sql</span></span>
* <span data-ttu-id="0aee2-178">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="0aee2-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0aee2-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-179">Az.Storage</span></span>
* <span data-ttu-id="0aee2-180">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0aee2-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0aee2-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0aee2-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0aee2-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0aee2-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0aee2-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0aee2-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0aee2-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0aee2-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0aee2-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-187">Az.Websites</span></span>
* <span data-ttu-id="0aee2-188">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="0aee2-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0aee2-189">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0aee2-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-190">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-191">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="0aee2-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0aee2-192">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0aee2-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0aee2-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-193">Az.Automation</span></span>
* <span data-ttu-id="0aee2-194">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0aee2-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0aee2-195">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="0aee2-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0aee2-196">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="0aee2-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0aee2-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0aee2-197">Az.Cdn</span></span>
* <span data-ttu-id="0aee2-198">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="0aee2-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-199">Az.Compute</span></span>
* <span data-ttu-id="0aee2-200">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="0aee2-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0aee2-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0aee2-201">Az.DataFactory</span></span>
* <span data-ttu-id="0aee2-202">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="0aee2-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0aee2-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0aee2-203">Az.LogicApp</span></span>
* <span data-ttu-id="0aee2-204">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="0aee2-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-205">Az.Network</span></span>
* <span data-ttu-id="0aee2-206">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="0aee2-208">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="0aee2-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0aee2-209">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="0aee2-209">SDK Update</span></span>
* <span data-ttu-id="0aee2-210">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0aee2-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0aee2-211">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0aee2-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-212">Az.Resources</span></span>
* <span data-ttu-id="0aee2-213">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="0aee2-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0aee2-214">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0aee2-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0aee2-215">Correzione del problema con il piping del risultato di `Get-AzResource` in</span><span class="sxs-lookup"><span data-stu-id="0aee2-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="0aee2-216">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0aee2-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0aee2-217">Correzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di</span><span class="sxs-lookup"><span data-stu-id="0aee2-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="0aee2-218">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0aee2-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-219">Az.Sql</span></span>
* <span data-ttu-id="0aee2-220">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0aee2-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0aee2-221">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0aee2-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0aee2-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-222">Az.Storage</span></span>
* <span data-ttu-id="0aee2-223">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0aee2-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0aee2-224">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0aee2-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="0aee2-226">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="0aee2-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0aee2-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-227">Az.Automation</span></span>
* <span data-ttu-id="0aee2-228">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0aee2-229">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0aee2-230">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0aee2-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="0aee2-232">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0aee2-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-233">Az.Compute</span></span>
* <span data-ttu-id="0aee2-234">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="0aee2-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0aee2-235">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="0aee2-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0aee2-236">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0aee2-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0aee2-237">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0aee2-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="0aee2-239">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="0aee2-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0aee2-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0aee2-240">Az.EventHub</span></span>
* <span data-ttu-id="0aee2-241">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="0aee2-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0aee2-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0aee2-242">Az.KeyVault</span></span>
* <span data-ttu-id="0aee2-243">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0aee2-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0aee2-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0aee2-244">Az.LogicApp</span></span>
* <span data-ttu-id="0aee2-245">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0aee2-246">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="0aee2-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0aee2-247">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0aee2-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0aee2-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0aee2-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0aee2-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0aee2-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0aee2-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0aee2-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0aee2-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0aee2-252">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0aee2-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0aee2-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0aee2-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0aee2-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0aee2-257">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0aee2-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0aee2-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0aee2-258">Az.Monitor</span></span>
* <span data-ttu-id="0aee2-259">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0aee2-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-260">Az.Network</span></span>
* <span data-ttu-id="0aee2-261">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0aee2-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0aee2-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0aee2-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="0aee2-263">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="0aee2-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0aee2-264">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0aee2-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0aee2-265">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="0aee2-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0aee2-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-266">Az.Resources</span></span>
* <span data-ttu-id="0aee2-267">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0aee2-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0aee2-268">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0aee2-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0aee2-269">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0aee2-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0aee2-270">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0aee2-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-271">Az.Sql</span></span>
* <span data-ttu-id="0aee2-272">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="0aee2-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0aee2-273">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="0aee2-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0aee2-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-274">Az.Websites</span></span>
* <span data-ttu-id="0aee2-275">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0aee2-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0aee2-276">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0aee2-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-277">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-278">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0aee2-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0aee2-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-279">Az.AnalysisServices</span></span>
<span data-ttu-id="0aee2-280">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0aee2-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-281">Az.Compute</span></span>
* <span data-ttu-id="0aee2-282">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="0aee2-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0aee2-283">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0aee2-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0aee2-284">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0aee2-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-285">Az.RecoveryServices</span></span>
<span data-ttu-id="0aee2-286">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0aee2-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-287">Az.Resources</span></span>
* <span data-ttu-id="0aee2-288">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="0aee2-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0aee2-289">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0aee2-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0aee2-290">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="0aee2-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0aee2-291">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0aee2-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-292">Az.Sql</span></span>
* <span data-ttu-id="0aee2-293">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0aee2-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0aee2-294">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="0aee2-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0aee2-295">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="0aee2-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0aee2-296">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0aee2-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-297">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-298">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0aee2-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="0aee2-300">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="0aee2-302">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0aee2-303">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0aee2-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-304">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-305">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0aee2-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0aee2-306">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0aee2-307">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0aee2-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0aee2-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0aee2-308">Az.Aks</span></span>
* <span data-ttu-id="0aee2-309">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0aee2-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-310">Az.Automation</span></span>
* <span data-ttu-id="0aee2-311">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="0aee2-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0aee2-312">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0aee2-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0aee2-313">Az.Cdn</span></span>
* <span data-ttu-id="0aee2-314">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-315">Az.Compute</span></span>
* <span data-ttu-id="0aee2-316">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0aee2-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0aee2-317">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0aee2-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0aee2-318">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0aee2-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0aee2-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0aee2-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0aee2-320">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0aee2-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0aee2-321">Az.DataFactory</span></span>
* <span data-ttu-id="0aee2-322">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="0aee2-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="0aee2-324">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0aee2-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0aee2-325">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0aee2-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0aee2-326">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0aee2-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0aee2-327">Az.IotHub</span></span>
* <span data-ttu-id="0aee2-328">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0aee2-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0aee2-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0aee2-329">Az.KeyVault</span></span>
* <span data-ttu-id="0aee2-330">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-331">Az.Network</span></span>
* <span data-ttu-id="0aee2-332">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-333">Az.Resources</span></span>
* <span data-ttu-id="0aee2-334">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="0aee2-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0aee2-335">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0aee2-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0aee2-336">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="0aee2-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0aee2-337">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0aee2-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0aee2-338">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0aee2-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0aee2-339">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="0aee2-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0aee2-340">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0aee2-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0aee2-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0aee2-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="0aee2-342">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0aee2-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0aee2-343">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="0aee2-343">Fix some error messages.</span></span>
* <span data-ttu-id="0aee2-344">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="0aee2-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0aee2-345">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0aee2-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0aee2-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0aee2-346">Az.SignalR</span></span>
* <span data-ttu-id="0aee2-347">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-348">Az.Sql</span></span>
* <span data-ttu-id="0aee2-349">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0aee2-350">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="0aee2-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0aee2-351">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="0aee2-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0aee2-352">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="0aee2-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0aee2-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-353">Az.Storage</span></span>
* <span data-ttu-id="0aee2-354">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0aee2-355">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="0aee2-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0aee2-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0aee2-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0aee2-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0aee2-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0aee2-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0aee2-358">Az.TrafficManager</span></span>
* <span data-ttu-id="0aee2-359">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0aee2-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-360">Az.Websites</span></span>
* <span data-ttu-id="0aee2-361">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0aee2-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0aee2-362">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee2-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0aee2-363">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="0aee2-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0aee2-364">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0aee2-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0aee2-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-365">Az.Accounts</span></span>
* <span data-ttu-id="0aee2-366">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0aee2-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-367">Az.Compute</span></span>
* <span data-ttu-id="0aee2-368">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0aee2-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0aee2-369">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0aee2-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0aee2-370">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="0aee2-372">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="0aee2-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0aee2-373">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="0aee2-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0aee2-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0aee2-374">Az.EventGrid</span></span>
* <span data-ttu-id="0aee2-375">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0aee2-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0aee2-376">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0aee2-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0aee2-377">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0aee2-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0aee2-378">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0aee2-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0aee2-379">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0aee2-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0aee2-380">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0aee2-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0aee2-381">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0aee2-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0aee2-382">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0aee2-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0aee2-383">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0aee2-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0aee2-384">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0aee2-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="0aee2-385">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0aee2-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0aee2-386">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0aee2-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0aee2-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0aee2-387">Az.IotHub</span></span>
* <span data-ttu-id="0aee2-388">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="0aee2-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0aee2-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0aee2-389">Az.LogicApp</span></span>
* <span data-ttu-id="0aee2-390">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="0aee2-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-391">Az.Resources</span></span>
* <span data-ttu-id="0aee2-392">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0aee2-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0aee2-393">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0aee2-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0aee2-394">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0aee2-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0aee2-395">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0aee2-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0aee2-396">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="0aee2-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0aee2-397">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0aee2-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0aee2-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0aee2-398">Az.SignalR</span></span>
* <span data-ttu-id="0aee2-399">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-400">Az.Sql</span></span>
* <span data-ttu-id="0aee2-401">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="0aee2-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0aee2-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-402">Az.Storage</span></span>
* <span data-ttu-id="0aee2-403">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="0aee2-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0aee2-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0aee2-404">New-AzStorageContext</span></span>
* <span data-ttu-id="0aee2-405">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="0aee2-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0aee2-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0aee2-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0aee2-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-407">Az.Websites</span></span>
* <span data-ttu-id="0aee2-408">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="0aee2-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0aee2-409">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0aee2-410">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0aee2-411">Generale</span><span class="sxs-lookup"><span data-stu-id="0aee2-411">General</span></span>

- <span data-ttu-id="0aee2-412">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="0aee2-412">General Availability of Az Module</span></span>
- <span data-ttu-id="0aee2-413">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="0aee2-413">Online help for each module</span></span>
- <span data-ttu-id="0aee2-414">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0aee2-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0aee2-415">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="0aee2-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0aee2-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-416">Az.Accounts</span></span>
- <span data-ttu-id="0aee2-417">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0aee2-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="0aee2-418">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="0aee2-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0aee2-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0aee2-419">Az.ApiManagement</span></span>
- <span data-ttu-id="0aee2-420">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="0aee2-420">Fixes for #7002</span></span>
- <span data-ttu-id="0aee2-421">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0aee2-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0aee2-422">Az.Batch</span></span>
- <span data-ttu-id="0aee2-423">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0aee2-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0aee2-424">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="0aee2-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0aee2-425">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0aee2-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0aee2-426">Az.Billing</span></span>
- <span data-ttu-id="0aee2-427">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0aee2-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-428">Az.CognitivServices</span></span>
- <span data-ttu-id="0aee2-429">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0aee2-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0aee2-430">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="0aee2-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0aee2-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="0aee2-432">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0aee2-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0aee2-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0aee2-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0aee2-434">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="0aee2-436">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0aee2-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0aee2-437">Az.Monitor</span></span>
- <span data-ttu-id="0aee2-438">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0aee2-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0aee2-439">Az.KeyVault</span></span>
- <span data-ttu-id="0aee2-440">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="0aee2-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0aee2-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0aee2-441">Az.MachineLearning</span></span>
- <span data-ttu-id="0aee2-442">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0aee2-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0aee2-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0aee2-443">Az.Media</span></span>
- <span data-ttu-id="0aee2-444">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0aee2-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0aee2-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-445">Az.Network</span></span>
<span data-ttu-id="0aee2-446">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0aee2-447">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0aee2-447">New cmdlets added:</span></span>
        - <span data-ttu-id="0aee2-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0aee2-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0aee2-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0aee2-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aee2-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0aee2-456">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0aee2-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0aee2-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0aee2-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0aee2-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0aee2-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0aee2-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0aee2-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0aee2-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0aee2-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0aee2-462">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="0aee2-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0aee2-463">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0aee2-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0aee2-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0aee2-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0aee2-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0aee2-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0aee2-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0aee2-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0aee2-467">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0aee2-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0aee2-468">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0aee2-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0aee2-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="0aee2-470">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0aee2-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0aee2-471">Az.Profile</span></span>
- <span data-ttu-id="0aee2-472">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0aee2-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="0aee2-474">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0aee2-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-475">Az.Resources</span></span>
- <span data-ttu-id="0aee2-476">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0aee2-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0aee2-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="0aee2-478">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="0aee2-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0aee2-479">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0aee2-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0aee2-480">Az.SIgnalR</span></span>
- <span data-ttu-id="0aee2-481">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0aee2-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0aee2-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-482">Az.Sql</span></span>
- <span data-ttu-id="0aee2-483">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="0aee2-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0aee2-484">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0aee2-485">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0aee2-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-486">Az.Storage</span></span>
- <span data-ttu-id="0aee2-487">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0aee2-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-488">Az.Websites</span></span>
- <span data-ttu-id="0aee2-489">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0aee2-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0aee2-490">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0aee2-491">Generale</span><span class="sxs-lookup"><span data-stu-id="0aee2-491">General</span></span>

* <span data-ttu-id="0aee2-492">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0aee2-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0aee2-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-493">Az.Compute</span></span>

* <span data-ttu-id="0aee2-494">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0aee2-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="0aee2-496">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="0aee2-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0aee2-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0aee2-497">Az.FrontDoor</span></span>

* <span data-ttu-id="0aee2-498">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="0aee2-498">Fixed some broken links</span></span>
    - <span data-ttu-id="0aee2-499">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0aee2-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0aee2-500">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0aee2-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0aee2-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="0aee2-502">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee2-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0aee2-503">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="0aee2-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0aee2-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-504">Az.Resources</span></span>

* <span data-ttu-id="0aee2-505">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0aee2-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0aee2-506">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="0aee2-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0aee2-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-507">Az.Sql</span></span>

* <span data-ttu-id="0aee2-508">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0aee2-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0aee2-509">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="0aee2-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0aee2-510">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="0aee2-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0aee2-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-511">Az.Storage</span></span>

* <span data-ttu-id="0aee2-512">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0aee2-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0aee2-513">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="0aee2-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0aee2-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0aee2-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0aee2-515">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="0aee2-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="0aee2-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0aee2-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0aee2-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0aee2-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0aee2-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-518">Az.Websites</span></span>

* <span data-ttu-id="0aee2-519">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0aee2-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0aee2-520">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0aee2-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0aee2-521">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee2-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0aee2-522">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0aee2-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0aee2-523">Az.ApiManagement</span></span>
* <span data-ttu-id="0aee2-524">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0aee2-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0aee2-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0aee2-525">Az.Automation</span></span>
* <span data-ttu-id="0aee2-526">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="0aee2-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0aee2-527">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="0aee2-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0aee2-528">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="0aee2-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0aee2-529">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="0aee2-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0aee2-530">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="0aee2-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0aee2-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-531">Az.Compute</span></span>
* <span data-ttu-id="0aee2-532">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0aee2-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0aee2-533">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0aee2-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0aee2-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="0aee2-535">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0aee2-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0aee2-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0aee2-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0aee2-537">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="0aee2-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0aee2-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-538">Az.Network</span></span>
* <span data-ttu-id="0aee2-539">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0aee2-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0aee2-540">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="0aee2-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0aee2-541">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0aee2-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0aee2-542">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0aee2-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0aee2-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0aee2-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0aee2-544">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="0aee2-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0aee2-545">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="0aee2-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0aee2-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0aee2-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0aee2-547">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0aee2-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0aee2-548">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0aee2-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0aee2-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0aee2-549">Az.Relay</span></span>
* <span data-ttu-id="0aee2-550">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0aee2-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0aee2-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-551">Az.Resources</span></span>
* <span data-ttu-id="0aee2-552">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e</span><span class="sxs-lookup"><span data-stu-id="0aee2-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="0aee2-553">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="0aee2-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0aee2-554">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0aee2-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0aee2-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0aee2-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="0aee2-556">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0aee2-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0aee2-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-557">Az.Sql</span></span>
* <span data-ttu-id="0aee2-558">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="0aee2-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0aee2-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0aee2-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0aee2-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0aee2-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0aee2-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0aee2-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0aee2-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0aee2-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0aee2-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0aee2-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0aee2-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0aee2-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0aee2-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0aee2-567">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="0aee2-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0aee2-568">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="0aee2-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0aee2-569">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="0aee2-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0aee2-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0aee2-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0aee2-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0aee2-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0aee2-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0aee2-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0aee2-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0aee2-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0aee2-574">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0aee2-575">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0aee2-576">Generale</span><span class="sxs-lookup"><span data-stu-id="0aee2-576">General</span></span>
* <span data-ttu-id="0aee2-577">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="0aee2-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0aee2-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0aee2-578">Az.Profile</span></span>
* <span data-ttu-id="0aee2-579">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0aee2-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0aee2-580">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="0aee2-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0aee2-581">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0aee2-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0aee2-582">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="0aee2-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0aee2-583">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="0aee2-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0aee2-584">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0aee2-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0aee2-585">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="0aee2-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0aee2-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="0aee2-587">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0aee2-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-588">Az.Compute</span></span>
* <span data-ttu-id="0aee2-589">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0aee2-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0aee2-590">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0aee2-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0aee2-591">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="0aee2-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="0aee2-593">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0aee2-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0aee2-594">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="0aee2-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0aee2-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0aee2-595">Az.Insights</span></span>
* <span data-ttu-id="0aee2-596">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="0aee2-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0aee2-597">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="0aee2-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0aee2-598">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0aee2-599">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="0aee2-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-600">Az.Network</span></span>
* <span data-ttu-id="0aee2-601">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0aee2-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0aee2-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0aee2-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0aee2-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0aee2-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0aee2-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0aee2-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0aee2-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0aee2-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0aee2-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0aee2-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0aee2-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0aee2-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0aee2-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0aee2-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="0aee2-609">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="0aee2-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-610">Az.Resources</span></span>
* <span data-ttu-id="0aee2-611">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0aee2-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0aee2-612">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0aee2-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0aee2-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0aee2-613">Az.ServiceBus</span></span>
* <span data-ttu-id="0aee2-614">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="0aee2-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0aee2-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0aee2-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="0aee2-616">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="0aee2-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0aee2-617">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="0aee2-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0aee2-618">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0aee2-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0aee2-619">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0aee2-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0aee2-620">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0aee2-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0aee2-621">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0aee2-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0aee2-622">Az.Profile</span></span>
* <span data-ttu-id="0aee2-623">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="0aee2-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0aee2-624">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0aee2-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-625">Az.Compute</span></span>
* <span data-ttu-id="0aee2-626">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="0aee2-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0aee2-627">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aee2-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0aee2-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0aee2-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="0aee2-629">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0aee2-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0aee2-630">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0aee2-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0aee2-631">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0aee2-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0aee2-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0aee2-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0aee2-633">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0aee2-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-634">Az.Network</span></span>
* <span data-ttu-id="0aee2-635">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="0aee2-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0aee2-636">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aee2-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-637">Az.Resources</span></span>
* <span data-ttu-id="0aee2-638">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="0aee2-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0aee2-639">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="0aee2-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0aee2-640">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0aee2-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0aee2-641">Azure.Storage</span></span>
* <span data-ttu-id="0aee2-642">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="0aee2-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0aee2-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0aee2-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0aee2-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0aee2-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0aee2-645">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="0aee2-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0aee2-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0aee2-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0aee2-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0aee2-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="0aee2-648">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="0aee2-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0aee2-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0aee2-649">Az.Compute</span></span>
* <span data-ttu-id="0aee2-650">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="0aee2-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0aee2-651">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0aee2-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0aee2-652">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="0aee2-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0aee2-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0aee2-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0aee2-654">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="0aee2-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0aee2-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0aee2-655">Az.Network</span></span>
* <span data-ttu-id="0aee2-656">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0aee2-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0aee2-657">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0aee2-657">new cmdlets added</span></span>
    - <span data-ttu-id="0aee2-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0aee2-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0aee2-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0aee2-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0aee2-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0aee2-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0aee2-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0aee2-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0aee2-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0aee2-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0aee2-664">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="0aee2-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0aee2-665">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0aee2-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0aee2-666">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0aee2-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0aee2-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0aee2-667">Az.RedisCache</span></span>
* <span data-ttu-id="0aee2-668">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="0aee2-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0aee2-669">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="0aee2-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0aee2-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0aee2-670">Az.Resources</span></span>
* <span data-ttu-id="0aee2-671">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0aee2-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0aee2-672">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="0aee2-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0aee2-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0aee2-673">Az.Sql</span></span>
* <span data-ttu-id="0aee2-674">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="0aee2-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0aee2-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0aee2-675">Az.Websites</span></span>
* <span data-ttu-id="0aee2-676">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="0aee2-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0aee2-677">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="0aee2-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0aee2-678">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="0aee2-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0aee2-679">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="0aee2-679">Initial Release</span></span>