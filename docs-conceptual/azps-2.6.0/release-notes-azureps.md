---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052635"
---
## <a name="260---august-2019"></a><span data-ttu-id="a6e0b-101">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a6e0b-102">Generale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-102">General</span></span>
* <span data-ttu-id="a6e0b-103">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="a6e0b-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-104">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-105">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e0b-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e0b-106">Az.Aks</span></span>
* <span data-ttu-id="a6e0b-107">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a6e0b-108">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a6e0b-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e0b-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-109">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e0b-110">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a6e0b-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a6e0b-111">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="a6e0b-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a6e0b-112">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a6e0b-113">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a6e0b-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a6e0b-114">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e0b-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-115">Az.Batch</span></span>
* <span data-ttu-id="a6e0b-116">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="a6e0b-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e0b-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e0b-117">Az.Cdn</span></span>
* <span data-ttu-id="a6e0b-118">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="a6e0b-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-119">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-120">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a6e0b-121">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6e0b-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a6e0b-122">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a6e0b-123">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a6e0b-124">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a6e0b-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a6e0b-125">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a6e0b-126">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a6e0b-127">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-128">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-129">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="a6e0b-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a6e0b-130">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a6e0b-131">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a6e0b-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a6e0b-132">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="a6e0b-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-134">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e0b-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-135">Az.EventHub</span></span>
* <span data-ttu-id="a6e0b-136">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a6e0b-137">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a6e0b-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a6e0b-138">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a6e0b-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a6e0b-139">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a6e0b-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a6e0b-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a6e0b-141">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e0b-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-142">Az.Monitor</span></span>
* <span data-ttu-id="a6e0b-143">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="a6e0b-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-144">Az.Network</span></span>
* <span data-ttu-id="a6e0b-145">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a6e0b-146">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a6e0b-147">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a6e0b-148">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a6e0b-149">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="a6e0b-150">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a6e0b-151">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a6e0b-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-153">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a6e0b-154">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a6e0b-154">Added example</span></span>
    - <span data-ttu-id="a6e0b-155">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a6e0b-156">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a6e0b-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a6e0b-157">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a6e0b-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-159">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-160">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-161">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="a6e0b-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a6e0b-162">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="a6e0b-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a6e0b-163">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="a6e0b-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a6e0b-164">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="a6e0b-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-165">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-166">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a6e0b-167">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a6e0b-168">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="a6e0b-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-170">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a6e0b-171">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a6e0b-172">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a6e0b-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a6e0b-173">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a6e0b-174">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a6e0b-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a6e0b-175">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-176">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-177">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-178">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-179">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a6e0b-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a6e0b-180">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="a6e0b-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a6e0b-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a6e0b-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a6e0b-183">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="a6e0b-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a6e0b-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-185">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-186">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a6e0b-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a6e0b-187">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-188">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-189">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6e0b-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a6e0b-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a6e0b-191">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-192">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-193">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="a6e0b-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-195">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-196">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-197">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a6e0b-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a6e0b-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a6e0b-199">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="a6e0b-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a6e0b-200">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a6e0b-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-201">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-202">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a6e0b-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a6e0b-203">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e0b-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-204">Az.EventHub</span></span>
* <span data-ttu-id="a6e0b-205">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e0b-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a6e0b-206">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-207">Az.KeyVault</span></span>
* <span data-ttu-id="a6e0b-208">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e0b-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-209">Az.LogicApp</span></span>
* <span data-ttu-id="a6e0b-210">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="a6e0b-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a6e0b-211">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="a6e0b-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a6e0b-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-212">Az.ManagedServices</span></span>
* <span data-ttu-id="a6e0b-213">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-214">Az.Network</span></span>
* <span data-ttu-id="a6e0b-215">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a6e0b-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a6e0b-216">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-216">New cmdlets</span></span>
        - <span data-ttu-id="a6e0b-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e0b-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e0b-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e0b-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e0b-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e0b-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e0b-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a6e0b-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a6e0b-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a6e0b-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a6e0b-225">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="a6e0b-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a6e0b-226">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a6e0b-227">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag per indicare l'abilitazione o la disabilitazione dell'applicazione dei criteri di rete su endpoint privati in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="a6e0b-228">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag per indicare l'abilitazione o la disabilitazione dell'applicazione dei criteri di rete sul servizio di collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a6e0b-229">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="a6e0b-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a6e0b-230">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="a6e0b-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a6e0b-231">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-231">Updated cmdlets</span></span>
        - <span data-ttu-id="a6e0b-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e0b-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a6e0b-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a6e0b-235">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a6e0b-236">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a6e0b-237">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e0b-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a6e0b-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a6e0b-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a6e0b-241">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="a6e0b-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a6e0b-242">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a6e0b-243">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-245">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="a6e0b-246">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-248">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a6e0b-249">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a6e0b-250">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a6e0b-251">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a6e0b-252">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a6e0b-253">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a6e0b-254">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a6e0b-255">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a6e0b-256">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a6e0b-257">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-258">Az.Resources</span></span>
- <span data-ttu-id="a6e0b-259">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a6e0b-260">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a6e0b-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-261">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-262">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e0b-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a6e0b-263">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-264">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-265">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a6e0b-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a6e0b-266">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="a6e0b-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a6e0b-267">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-268">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-269">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e0b-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e0b-270">Az.StorageSync</span></span>
* <span data-ttu-id="a6e0b-271">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a6e0b-272">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="a6e0b-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-273">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-274">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a6e0b-275">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a6e0b-276">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a6e0b-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a6e0b-277">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-278">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-279">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a6e0b-280">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a6e0b-281">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6e0b-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a6e0b-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-282">Az.Advisor</span></span>
* <span data-ttu-id="a6e0b-283">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a6e0b-284">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a6e0b-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-285">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e0b-286">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a6e0b-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a6e0b-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a6e0b-288">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a6e0b-289">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a6e0b-290">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a6e0b-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a6e0b-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a6e0b-292">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-293">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-294">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-295">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-296">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-297">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-298">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e0b-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e0b-299">Az.EventGrid</span></span>
* <span data-ttu-id="a6e0b-300">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e0b-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-301">Az.IotHub</span></span>
* <span data-ttu-id="a6e0b-302">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-303">Az.Network</span></span>
* <span data-ttu-id="a6e0b-304">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="a6e0b-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a6e0b-305">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e0b-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e0b-307">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a6e0b-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a6e0b-308">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a6e0b-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-310">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a6e0b-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-312">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="a6e0b-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-313">Az.Resources</span></span>
    - <span data-ttu-id="a6e0b-314">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="a6e0b-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a6e0b-315">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="a6e0b-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a6e0b-316">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="a6e0b-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a6e0b-317">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-318">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-319">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a6e0b-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-320">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-321">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="a6e0b-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a6e0b-322">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a6e0b-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e0b-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e0b-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a6e0b-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a6e0b-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a6e0b-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a6e0b-329">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="a6e0b-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-330">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-331">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a6e0b-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e0b-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a6e0b-333">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="a6e0b-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a6e0b-334">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="a6e0b-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a6e0b-335">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a6e0b-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a6e0b-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a6e0b-338">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="a6e0b-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a6e0b-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e0b-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a6e0b-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a6e0b-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a6e0b-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a6e0b-341">Az.StorageSync</span></span>
* <span data-ttu-id="a6e0b-342">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a6e0b-343">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-344">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-345">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="a6e0b-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a6e0b-346">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a6e0b-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a6e0b-347">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="a6e0b-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a6e0b-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a6e0b-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a6e0b-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a6e0b-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-350">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-351">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a6e0b-352">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a6e0b-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a6e0b-353">Az.Dns</span></span>
* <span data-ttu-id="a6e0b-354">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e0b-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e0b-355">Az.EventGrid</span></span>
* <span data-ttu-id="a6e0b-356">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a6e0b-357">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-357">New cmdlets:</span></span>
    - <span data-ttu-id="a6e0b-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e0b-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e0b-359">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e0b-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e0b-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e0b-361">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a6e0b-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6e0b-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a6e0b-363">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e0b-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a6e0b-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a6e0b-365">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e0b-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a6e0b-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a6e0b-367">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a6e0b-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a6e0b-369">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a6e0b-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6e0b-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a6e0b-371">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="a6e0b-372">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a6e0b-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a6e0b-373">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a6e0b-374">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="a6e0b-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e0b-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a6e0b-376">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e0b-377">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e0b-378">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a6e0b-379">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a6e0b-380">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a6e0b-381">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a6e0b-382">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a6e0b-383">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="a6e0b-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e0b-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a6e0b-385">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a6e0b-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a6e0b-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a6e0b-387">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a6e0b-388">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e0b-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-389">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e0b-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a6e0b-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a6e0b-391">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a6e0b-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a6e0b-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a6e0b-393">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="a6e0b-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-394">Az.Network</span></span>
* <span data-ttu-id="a6e0b-395">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a6e0b-396">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-396">New cmdlets</span></span>
        - <span data-ttu-id="a6e0b-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a6e0b-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a6e0b-398">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a6e0b-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a6e0b-399">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-399">New cmdlets</span></span> 
        - <span data-ttu-id="a6e0b-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a6e0b-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a6e0b-401">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a6e0b-402">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-402">New cmdlets</span></span> 
        - <span data-ttu-id="a6e0b-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="a6e0b-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e0b-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a6e0b-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a6e0b-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a6e0b-408">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e0b-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a6e0b-409">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-409">New cmdlets</span></span>
        - <span data-ttu-id="a6e0b-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e0b-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e0b-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e0b-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e0b-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6e0b-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a6e0b-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a6e0b-414">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a6e0b-415">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a6e0b-416">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a6e0b-417">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a6e0b-418">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a6e0b-419">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e0b-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a6e0b-420">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a6e0b-421">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a6e0b-422">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a6e0b-423">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="a6e0b-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a6e0b-424">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a6e0b-425">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a6e0b-426">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a6e0b-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a6e0b-427">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a6e0b-428">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a6e0b-429">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a6e0b-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a6e0b-430">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a6e0b-431">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a6e0b-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a6e0b-432">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a6e0b-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="a6e0b-433">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="a6e0b-434">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a6e0b-435">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a6e0b-436">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-438">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-439">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-440">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="a6e0b-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a6e0b-441">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a6e0b-442">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a6e0b-443">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-445">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="a6e0b-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-446">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-447">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a6e0b-448">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a6e0b-449">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="a6e0b-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a6e0b-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e0b-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e0b-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e0b-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e0b-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6e0b-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a6e0b-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a6e0b-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a6e0b-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a6e0b-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-455">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-456">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a6e0b-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="a6e0b-458">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="a6e0b-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a6e0b-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-460">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-461">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="a6e0b-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a6e0b-462">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6e0b-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a6e0b-463">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a6e0b-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e0b-464">Az.Cdn</span></span>
* <span data-ttu-id="a6e0b-465">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-466">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-467">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a6e0b-468">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e0b-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-469">Az.EventHub</span></span>
* <span data-ttu-id="a6e0b-470">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="a6e0b-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a6e0b-471">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e0b-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-472">Az.Network</span></span>
* <span data-ttu-id="a6e0b-473">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="a6e0b-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a6e0b-474">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="a6e0b-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e0b-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e0b-476">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-478">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-479">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-480">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e0b-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-482">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a6e0b-483">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-484">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-485">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a6e0b-486">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a6e0b-487">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a6e0b-488">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-489">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-490">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a6e0b-491">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a6e0b-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-492">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e0b-493">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a6e0b-494">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a6e0b-495">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a6e0b-496">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a6e0b-497">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a6e0b-498">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="a6e0b-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a6e0b-499">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a6e0b-500">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a6e0b-501">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a6e0b-502">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="a6e0b-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a6e0b-503">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a6e0b-504">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="a6e0b-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a6e0b-505">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="a6e0b-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a6e0b-506">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a6e0b-507">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a6e0b-508">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a6e0b-509">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a6e0b-510">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="a6e0b-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a6e0b-511">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a6e0b-512">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a6e0b-513">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="a6e0b-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a6e0b-514">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a6e0b-515">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a6e0b-516">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a6e0b-517">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a6e0b-518">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a6e0b-519">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a6e0b-520">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a6e0b-521">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a6e0b-522">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a6e0b-523">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="a6e0b-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a6e0b-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a6e0b-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a6e0b-525">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a6e0b-526">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a6e0b-527">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a6e0b-528">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="a6e0b-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a6e0b-529">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a6e0b-530">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a6e0b-531">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a6e0b-532">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a6e0b-533">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a6e0b-534">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a6e0b-535">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a6e0b-536">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a6e0b-537">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a6e0b-538">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a6e0b-539">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a6e0b-540">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a6e0b-541">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a6e0b-542">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a6e0b-543">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a6e0b-544">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a6e0b-545">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a6e0b-546">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a6e0b-547">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a6e0b-548">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a6e0b-549">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a6e0b-550">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a6e0b-551">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a6e0b-552">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a6e0b-553">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a6e0b-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a6e0b-554">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a6e0b-555">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a6e0b-556">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a6e0b-557">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a6e0b-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a6e0b-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a6e0b-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a6e0b-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a6e0b-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a6e0b-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a6e0b-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a6e0b-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a6e0b-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a6e0b-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a6e0b-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a6e0b-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a6e0b-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a6e0b-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a6e0b-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-570">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-571">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a6e0b-572">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a6e0b-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a6e0b-573">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a6e0b-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a6e0b-574">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a6e0b-575">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a6e0b-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a6e0b-576">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a6e0b-577">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-578">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-579">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a6e0b-580">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="a6e0b-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-582">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e0b-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-583">Az.Monitor</span></span>
* <span data-ttu-id="a6e0b-584">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="a6e0b-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-585">Az.Network</span></span>
* <span data-ttu-id="a6e0b-586">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="a6e0b-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a6e0b-587">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="a6e0b-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e0b-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a6e0b-589">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-590">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-591">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-592">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-593">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="a6e0b-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a6e0b-594">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-595">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-596">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="a6e0b-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-598">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a6e0b-599">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-600">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-601">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a6e0b-602">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a6e0b-603">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a6e0b-604">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a6e0b-605">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a6e0b-606">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6e0b-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a6e0b-607">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-607">Breaking changes</span></span>
    - <span data-ttu-id="a6e0b-608">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a6e0b-609">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a6e0b-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a6e0b-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="a6e0b-611">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="a6e0b-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a6e0b-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a6e0b-612">Az.Dns</span></span>
* <span data-ttu-id="a6e0b-613">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="a6e0b-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a6e0b-614">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a6e0b-615">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a6e0b-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-616">Az.FrontDoor</span></span>
* <span data-ttu-id="a6e0b-617">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a6e0b-618">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a6e0b-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e0b-619">Az.HDInsight</span></span>
* <span data-ttu-id="a6e0b-620">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a6e0b-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e0b-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a6e0b-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e0b-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a6e0b-623">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a6e0b-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a6e0b-624">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a6e0b-625">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a6e0b-626">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e0b-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-627">Az.Monitor</span></span>
* <span data-ttu-id="a6e0b-628">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a6e0b-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a6e0b-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a6e0b-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a6e0b-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a6e0b-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a6e0b-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a6e0b-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a6e0b-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a6e0b-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a6e0b-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a6e0b-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e0b-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e0b-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e0b-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e0b-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a6e0b-640">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="a6e0b-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a6e0b-641">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-642">Az.Network</span></span>
* <span data-ttu-id="a6e0b-643">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="a6e0b-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a6e0b-644">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-644">New cmdlets</span></span>
        - <span data-ttu-id="a6e0b-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="a6e0b-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a6e0b-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a6e0b-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a6e0b-649">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-649">Updated cmdlets</span></span>
        - <span data-ttu-id="a6e0b-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a6e0b-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a6e0b-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a6e0b-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a6e0b-652">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a6e0b-653">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a6e0b-654">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e0b-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e0b-656">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a6e0b-657">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a6e0b-658">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-660">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a6e0b-661">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a6e0b-662">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a6e0b-663">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a6e0b-664">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a6e0b-665">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a6e0b-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a6e0b-666">Az.Relay</span></span>
* <span data-ttu-id="a6e0b-667">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="a6e0b-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-668">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-669">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-670">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-671">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="a6e0b-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a6e0b-672">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a6e0b-673">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a6e0b-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="a6e0b-675">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a6e0b-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a6e0b-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a6e0b-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-679">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-680">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a6e0b-681">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a6e0b-682">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e0b-683">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-683">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e0b-684">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-684">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e0b-685">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e0b-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e0b-686">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e0b-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e0b-687">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e0b-688">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a6e0b-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e0b-689">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e0b-690">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-691">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-692">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="a6e0b-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a6e0b-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-693">Az.Batch</span></span>
* <span data-ttu-id="a6e0b-694">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e0b-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e0b-695">Az.Cdn</span></span>
* <span data-ttu-id="a6e0b-696">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-698">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-699">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-700">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="a6e0b-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a6e0b-701">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-702">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-703">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-704">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-706">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e0b-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e0b-707">Az.EventGrid</span></span>
* <span data-ttu-id="a6e0b-708">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e0b-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-709">Az.EventHub</span></span>
* <span data-ttu-id="a6e0b-710">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a6e0b-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a6e0b-711">Az.HDInsight</span></span>
* <span data-ttu-id="a6e0b-712">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e0b-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-713">Az.IotHub</span></span>
* <span data-ttu-id="a6e0b-714">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-715">Az.KeyVault</span></span>
* <span data-ttu-id="a6e0b-716">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-717">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a6e0b-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6e0b-718">Az.MachineLearning</span></span>
* <span data-ttu-id="a6e0b-719">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a6e0b-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a6e0b-720">Az.Media</span></span>
* <span data-ttu-id="a6e0b-721">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e0b-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-722">Az.Monitor</span></span>
  * <span data-ttu-id="a6e0b-723">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a6e0b-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a6e0b-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a6e0b-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a6e0b-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a6e0b-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a6e0b-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a6e0b-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a6e0b-729">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a6e0b-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-730">Az.Network</span></span>
* <span data-ttu-id="a6e0b-731">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-732">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a6e0b-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a6e0b-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="a6e0b-734">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-736">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a6e0b-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a6e0b-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a6e0b-738">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-740">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-741">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a6e0b-742">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a6e0b-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a6e0b-743">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="a6e0b-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e0b-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e0b-744">Az.RedisCache</span></span>
* <span data-ttu-id="a6e0b-745">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-746">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-747">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-748">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-749">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="a6e0b-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a6e0b-750">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-751">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a6e0b-752">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a6e0b-753">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a6e0b-754">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a6e0b-755">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-756">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-757">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a6e0b-758">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a6e0b-759">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a6e0b-760">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a6e0b-761">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e0b-762">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-762">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e0b-763">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-763">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e0b-764">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e0b-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e0b-765">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e0b-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e0b-766">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e0b-767">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a6e0b-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e0b-768">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e0b-769">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-770">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-771">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e0b-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e0b-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e0b-773">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a6e0b-774">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-775">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-776">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a6e0b-777">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a6e0b-778">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-779">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-780">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a6e0b-781">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a6e0b-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6e0b-783">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-784">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-785">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a6e0b-786">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-787">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-788">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a6e0b-789">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a6e0b-790">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="a6e0b-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a6e0b-791">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a6e0b-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a6e0b-792">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a6e0b-793">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a6e0b-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-794">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-795">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-796">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-797">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="a6e0b-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a6e0b-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6e0b-798">New-AzStorageContext</span></span>
* <span data-ttu-id="a6e0b-799">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a6e0b-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e0b-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a6e0b-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a6e0b-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a6e0b-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a6e0b-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a6e0b-804">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="a6e0b-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a6e0b-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a6e0b-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a6e0b-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a6e0b-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6e0b-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a6e0b-809">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a6e0b-810">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-810">Highlights since the last major release</span></span>
* <span data-ttu-id="a6e0b-811">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-811">General availability of `Az` module</span></span>
* <span data-ttu-id="a6e0b-812">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a6e0b-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a6e0b-813">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a6e0b-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a6e0b-814">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a6e0b-815">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a6e0b-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e0b-816">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a6e0b-817">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-818">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-819">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a6e0b-820">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="a6e0b-820">Dynamic grouping</span></span>
    * <span data-ttu-id="a6e0b-821">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="a6e0b-821">Pre-Post script</span></span>
    * <span data-ttu-id="a6e0b-822">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="a6e0b-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-823">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-824">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a6e0b-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a6e0b-825">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-826">Az.KeyVault</span></span>
* <span data-ttu-id="a6e0b-827">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-828">Az.Network</span></span>
* <span data-ttu-id="a6e0b-829">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a6e0b-830">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-832">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="a6e0b-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a6e0b-833">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="a6e0b-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-834">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-835">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a6e0b-836">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-837">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-838">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-839">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-840">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a6e0b-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e0b-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e0b-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a6e0b-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a6e0b-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a6e0b-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a6e0b-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a6e0b-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-847">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-848">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="a6e0b-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a6e0b-849">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-850">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-851">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="a6e0b-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a6e0b-852">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-853">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-854">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a6e0b-855">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a6e0b-856">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e0b-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e0b-857">Az.Cdn</span></span>
* <span data-ttu-id="a6e0b-858">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-859">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-860">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="a6e0b-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-861">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-862">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a6e0b-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e0b-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-863">Az.LogicApp</span></span>
* <span data-ttu-id="a6e0b-864">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-865">Az.Network</span></span>
* <span data-ttu-id="a6e0b-866">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-868">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a6e0b-869">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="a6e0b-869">SDK Update</span></span>
* <span data-ttu-id="a6e0b-870">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a6e0b-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a6e0b-871">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a6e0b-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-872">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-873">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a6e0b-874">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a6e0b-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a6e0b-875">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a6e0b-876">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a6e0b-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a6e0b-877">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a6e0b-878">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a6e0b-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-879">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-880">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a6e0b-881">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-882">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-883">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a6e0b-884">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a6e0b-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e0b-886">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="a6e0b-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-887">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-888">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a6e0b-889">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a6e0b-890">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-892">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-893">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-894">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="a6e0b-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a6e0b-895">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="a6e0b-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a6e0b-896">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a6e0b-897">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-899">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a6e0b-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-900">Az.EventHub</span></span>
* <span data-ttu-id="a6e0b-901">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-902">Az.KeyVault</span></span>
* <span data-ttu-id="a6e0b-903">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6e0b-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e0b-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-904">Az.LogicApp</span></span>
* <span data-ttu-id="a6e0b-905">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a6e0b-906">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="a6e0b-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a6e0b-907">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a6e0b-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e0b-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e0b-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a6e0b-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a6e0b-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a6e0b-912">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a6e0b-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e0b-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e0b-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a6e0b-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a6e0b-917">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a6e0b-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a6e0b-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-918">Az.Monitor</span></span>
* <span data-ttu-id="a6e0b-919">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-920">Az.Network</span></span>
* <span data-ttu-id="a6e0b-921">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a6e0b-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="a6e0b-923">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a6e0b-924">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a6e0b-925">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a6e0b-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-926">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-927">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a6e0b-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6e0b-928">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a6e0b-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a6e0b-929">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a6e0b-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a6e0b-930">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a6e0b-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-931">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-932">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="a6e0b-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a6e0b-933">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="a6e0b-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-934">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-935">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a6e0b-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a6e0b-936">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-937">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-938">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6e0b-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e0b-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-939">Az.AnalysisServices</span></span>
<span data-ttu-id="a6e0b-940">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-941">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-942">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="a6e0b-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a6e0b-943">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a6e0b-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a6e0b-944">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-945">Az.RecoveryServices</span></span>
<span data-ttu-id="a6e0b-946">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-947">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-948">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="a6e0b-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a6e0b-949">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a6e0b-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a6e0b-950">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a6e0b-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a6e0b-951">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a6e0b-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-952">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-953">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a6e0b-954">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="a6e0b-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a6e0b-955">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a6e0b-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a6e0b-956">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-957">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-958">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a6e0b-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="a6e0b-960">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="a6e0b-962">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a6e0b-963">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-964">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-965">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a6e0b-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a6e0b-966">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e0b-967">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a6e0b-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a6e0b-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a6e0b-968">Az.Aks</span></span>
* <span data-ttu-id="a6e0b-969">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a6e0b-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-970">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-971">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a6e0b-972">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a6e0b-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a6e0b-973">Az.Cdn</span></span>
* <span data-ttu-id="a6e0b-974">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-975">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-976">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a6e0b-977">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6e0b-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a6e0b-978">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a6e0b-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a6e0b-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a6e0b-980">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a6e0b-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e0b-981">Az.DataFactory</span></span>
* <span data-ttu-id="a6e0b-982">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a6e0b-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-984">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="a6e0b-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a6e0b-985">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a6e0b-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a6e0b-986">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e0b-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-987">Az.IotHub</span></span>
* <span data-ttu-id="a6e0b-988">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-989">Az.KeyVault</span></span>
* <span data-ttu-id="a6e0b-990">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-991">Az.Network</span></span>
* <span data-ttu-id="a6e0b-992">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-993">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-994">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="a6e0b-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a6e0b-995">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6e0b-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a6e0b-996">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="a6e0b-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a6e0b-997">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a6e0b-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a6e0b-998">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a6e0b-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a6e0b-999">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="a6e0b-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a6e0b-1000">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-1002">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a6e0b-1003">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1003">Fix some error messages.</span></span>
* <span data-ttu-id="a6e0b-1004">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a6e0b-1005">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e0b-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1006">Az.SignalR</span></span>
* <span data-ttu-id="a6e0b-1007">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1008">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-1009">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e0b-1010">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a6e0b-1011">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a6e0b-1012">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1013">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-1014">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e0b-1015">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a6e0b-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a6e0b-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a6e0b-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="a6e0b-1019">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1020">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-1021">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a6e0b-1022">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a6e0b-1023">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a6e0b-1024">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a6e0b-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1025">Az.Accounts</span></span>
* <span data-ttu-id="a6e0b-1026">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1027">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-1028">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a6e0b-1029">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a6e0b-1030">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-1032">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a6e0b-1033">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a6e0b-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1034">Az.EventGrid</span></span>
* <span data-ttu-id="a6e0b-1035">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a6e0b-1036">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a6e0b-1037">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6e0b-1038">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6e0b-1039">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6e0b-1040">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a6e0b-1041">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a6e0b-1042">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a6e0b-1043">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a6e0b-1044">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="a6e0b-1045">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a6e0b-1046">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a6e0b-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1047">Az.IotHub</span></span>
* <span data-ttu-id="a6e0b-1048">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a6e0b-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1049">Az.LogicApp</span></span>
* <span data-ttu-id="a6e0b-1050">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1051">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-1052">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a6e0b-1053">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a6e0b-1054">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6e0b-1055">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a6e0b-1056">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a6e0b-1057">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a6e0b-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1058">Az.SignalR</span></span>
* <span data-ttu-id="a6e0b-1059">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1060">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-1061">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a6e0b-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1062">Az.Storage</span></span>
* <span data-ttu-id="a6e0b-1063">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a6e0b-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="a6e0b-1065">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a6e0b-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1067">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-1068">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a6e0b-1069">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a6e0b-1070">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a6e0b-1071">Generale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1071">General</span></span>

- <span data-ttu-id="a6e0b-1072">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="a6e0b-1073">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1073">Online help for each module</span></span>
- <span data-ttu-id="a6e0b-1074">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a6e0b-1075">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a6e0b-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1076">Az.Accounts</span></span>
- <span data-ttu-id="a6e0b-1077">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="a6e0b-1078">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6e0b-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="a6e0b-1080">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1080">Fixes for #7002</span></span>
- <span data-ttu-id="a6e0b-1081">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a6e0b-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1082">Az.Batch</span></span>
- <span data-ttu-id="a6e0b-1083">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a6e0b-1084">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a6e0b-1085">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a6e0b-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1086">Az.Billing</span></span>
- <span data-ttu-id="a6e0b-1087">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a6e0b-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="a6e0b-1089">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a6e0b-1090">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6e0b-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="a6e0b-1092">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a6e0b-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a6e0b-1094">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="a6e0b-1096">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a6e0b-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1097">Az.Monitor</span></span>
- <span data-ttu-id="a6e0b-1098">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a6e0b-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1099">Az.KeyVault</span></span>
- <span data-ttu-id="a6e0b-1100">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a6e0b-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="a6e0b-1102">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a6e0b-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1103">Az.Media</span></span>
- <span data-ttu-id="a6e0b-1104">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6e0b-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1105">Az.Network</span></span>
<span data-ttu-id="a6e0b-1106">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a6e0b-1107">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="a6e0b-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a6e0b-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a6e0b-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a6e0b-1116">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a6e0b-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a6e0b-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6e0b-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a6e0b-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a6e0b-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a6e0b-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a6e0b-1123">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a6e0b-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6e0b-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a6e0b-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a6e0b-1127">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a6e0b-1128">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a6e0b-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="a6e0b-1130">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a6e0b-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1131">Az.Profile</span></span>
- <span data-ttu-id="a6e0b-1132">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="a6e0b-1134">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e0b-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1135">Az.Resources</span></span>
- <span data-ttu-id="a6e0b-1136">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="a6e0b-1138">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a6e0b-1139">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a6e0b-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="a6e0b-1141">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e0b-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1142">Az.Sql</span></span>
- <span data-ttu-id="a6e0b-1143">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a6e0b-1144">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a6e0b-1145">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6e0b-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1146">Az.Storage</span></span>
- <span data-ttu-id="a6e0b-1147">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6e0b-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1148">Az.Websites</span></span>
- <span data-ttu-id="a6e0b-1149">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a6e0b-1150">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a6e0b-1151">Generale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1151">General</span></span>

* <span data-ttu-id="a6e0b-1152">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6e0b-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1153">Az.Compute</span></span>

* <span data-ttu-id="a6e0b-1154">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="a6e0b-1156">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a6e0b-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="a6e0b-1158">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="a6e0b-1159">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a6e0b-1160">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a6e0b-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="a6e0b-1162">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a6e0b-1163">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e0b-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1164">Az.Resources</span></span>

* <span data-ttu-id="a6e0b-1165">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a6e0b-1166">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e0b-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1167">Az.Sql</span></span>

* <span data-ttu-id="a6e0b-1168">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a6e0b-1169">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a6e0b-1170">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a6e0b-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1171">Az.Storage</span></span>

* <span data-ttu-id="a6e0b-1172">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a6e0b-1173">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a6e0b-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6e0b-1175">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="a6e0b-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a6e0b-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a6e0b-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1178">Az.Websites</span></span>

* <span data-ttu-id="a6e0b-1179">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a6e0b-1180">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a6e0b-1181">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a6e0b-1182">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a6e0b-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="a6e0b-1184">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a6e0b-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1185">Az.Automation</span></span>
* <span data-ttu-id="a6e0b-1186">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a6e0b-1187">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a6e0b-1188">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a6e0b-1189">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a6e0b-1190">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a6e0b-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1191">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-1192">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a6e0b-1193">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a6e0b-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="a6e0b-1195">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a6e0b-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a6e0b-1197">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a6e0b-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1198">Az.Network</span></span>
* <span data-ttu-id="a6e0b-1199">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a6e0b-1200">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a6e0b-1201">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a6e0b-1202">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a6e0b-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a6e0b-1204">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a6e0b-1205">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a6e0b-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a6e0b-1207">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a6e0b-1208">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a6e0b-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1209">Az.Relay</span></span>
* <span data-ttu-id="a6e0b-1210">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a6e0b-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1211">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-1212">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a6e0b-1213">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a6e0b-1214">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-1216">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a6e0b-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1217">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-1218">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a6e0b-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e0b-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e0b-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e0b-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a6e0b-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e0b-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e0b-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a6e0b-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a6e0b-1227">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a6e0b-1228">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a6e0b-1229">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a6e0b-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6e0b-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a6e0b-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a6e0b-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a6e0b-1234">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a6e0b-1235">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a6e0b-1236">Generale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1236">General</span></span>
* <span data-ttu-id="a6e0b-1237">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a6e0b-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1238">Az.Profile</span></span>
* <span data-ttu-id="a6e0b-1239">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a6e0b-1240">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a6e0b-1241">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a6e0b-1242">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a6e0b-1243">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a6e0b-1244">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a6e0b-1245">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-1247">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1248">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-1249">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a6e0b-1250">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a6e0b-1251">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-1253">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a6e0b-1254">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a6e0b-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1255">Az.Insights</span></span>
* <span data-ttu-id="a6e0b-1256">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a6e0b-1257">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a6e0b-1258">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a6e0b-1259">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1260">Az.Network</span></span>
* <span data-ttu-id="a6e0b-1261">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a6e0b-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a6e0b-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a6e0b-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a6e0b-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a6e0b-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a6e0b-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a6e0b-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="a6e0b-1269">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1270">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-1271">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a6e0b-1272">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a6e0b-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="a6e0b-1274">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a6e0b-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="a6e0b-1276">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a6e0b-1277">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a6e0b-1278">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a6e0b-1279">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a6e0b-1280">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a6e0b-1281">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a6e0b-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1282">Az.Profile</span></span>
* <span data-ttu-id="a6e0b-1283">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a6e0b-1284">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1285">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-1286">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a6e0b-1287">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a6e0b-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="a6e0b-1289">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a6e0b-1290">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a6e0b-1291">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6e0b-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a6e0b-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1294">Az.Network</span></span>
* <span data-ttu-id="a6e0b-1295">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a6e0b-1296">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1297">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-1298">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a6e0b-1299">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a6e0b-1300">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a6e0b-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1301">Azure.Storage</span></span>
* <span data-ttu-id="a6e0b-1302">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a6e0b-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a6e0b-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a6e0b-1305">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a6e0b-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a6e0b-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="a6e0b-1308">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a6e0b-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1309">Az.Compute</span></span>
* <span data-ttu-id="a6e0b-1310">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a6e0b-1311">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a6e0b-1312">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a6e0b-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a6e0b-1314">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a6e0b-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1315">Az.Network</span></span>
* <span data-ttu-id="a6e0b-1316">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a6e0b-1317">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1317">new cmdlets added</span></span>
    - <span data-ttu-id="a6e0b-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e0b-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e0b-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e0b-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a6e0b-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a6e0b-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a6e0b-1324">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a6e0b-1325">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a6e0b-1326">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a6e0b-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1327">Az.RedisCache</span></span>
* <span data-ttu-id="a6e0b-1328">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a6e0b-1329">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a6e0b-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1330">Az.Resources</span></span>
* <span data-ttu-id="a6e0b-1331">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a6e0b-1332">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a6e0b-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1333">Az.Sql</span></span>
* <span data-ttu-id="a6e0b-1334">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a6e0b-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1335">Az.Websites</span></span>
* <span data-ttu-id="a6e0b-1336">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a6e0b-1337">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a6e0b-1338">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a6e0b-1339">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="a6e0b-1339">Initial Release</span></span>