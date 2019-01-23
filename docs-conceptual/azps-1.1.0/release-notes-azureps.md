---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342020"
---
## <a name="110---january-2019"></a><span data-ttu-id="113a1-101">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="113a1-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="113a1-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-102">Az.Accounts</span></span>
* <span data-ttu-id="113a1-103">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="113a1-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="113a1-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-104">Az.Compute</span></span>
* <span data-ttu-id="113a1-105">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="113a1-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="113a1-106">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="113a1-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="113a1-107">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="113a1-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="113a1-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="113a1-109">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="113a1-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="113a1-110">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="113a1-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="113a1-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="113a1-111">Az.EventGrid</span></span>
* <span data-ttu-id="113a1-112">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="113a1-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="113a1-113">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="113a1-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="113a1-114">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="113a1-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="113a1-115">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="113a1-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="113a1-116">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="113a1-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="113a1-117">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="113a1-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="113a1-118">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="113a1-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="113a1-119">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="113a1-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="113a1-120">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="113a1-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="113a1-121">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="113a1-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="113a1-122">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="113a1-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="113a1-123">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="113a1-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="113a1-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="113a1-124">Az.IotHub</span></span>
* <span data-ttu-id="113a1-125">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="113a1-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="113a1-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="113a1-126">Az.LogicApp</span></span>
* <span data-ttu-id="113a1-127">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="113a1-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="113a1-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-128">Az.Resources</span></span>
* <span data-ttu-id="113a1-129">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="113a1-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="113a1-130">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="113a1-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="113a1-131">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="113a1-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="113a1-132">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="113a1-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="113a1-133">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="113a1-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="113a1-134">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="113a1-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="113a1-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="113a1-135">Az.SignalR</span></span>
* <span data-ttu-id="113a1-136">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="113a1-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-137">Az.Sql</span></span>
* <span data-ttu-id="113a1-138">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="113a1-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="113a1-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="113a1-139">Az.Storage</span></span>
* <span data-ttu-id="113a1-140">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="113a1-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="113a1-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="113a1-141">New-AzStorageContext</span></span>
* <span data-ttu-id="113a1-142">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="113a1-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="113a1-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="113a1-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="113a1-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="113a1-144">Az.Websites</span></span>
* <span data-ttu-id="113a1-145">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="113a1-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="113a1-146">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="113a1-147">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="113a1-148">Generale</span><span class="sxs-lookup"><span data-stu-id="113a1-148">General</span></span>

- <span data-ttu-id="113a1-149">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="113a1-149">General Availability of Az Module</span></span>
- <span data-ttu-id="113a1-150">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="113a1-150">Online help for each module</span></span>
- <span data-ttu-id="113a1-151">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="113a1-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="113a1-152">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="113a1-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="113a1-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-153">Az.Accounts</span></span>
- <span data-ttu-id="113a1-154">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="113a1-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="113a1-155">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="113a1-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="113a1-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="113a1-156">Az.ApiManagement</span></span>
- <span data-ttu-id="113a1-157">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="113a1-157">Fixes for #7002</span></span>
- <span data-ttu-id="113a1-158">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="113a1-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="113a1-159">Az.Batch</span></span>
- <span data-ttu-id="113a1-160">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="113a1-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="113a1-161">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="113a1-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="113a1-162">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="113a1-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="113a1-163">Az.Billing</span></span>
- <span data-ttu-id="113a1-164">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="113a1-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="113a1-165">Az.CognitivServices</span></span>
- <span data-ttu-id="113a1-166">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="113a1-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="113a1-167">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="113a1-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="113a1-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="113a1-169">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="113a1-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="113a1-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="113a1-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="113a1-171">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="113a1-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="113a1-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="113a1-173">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="113a1-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="113a1-174">Az.Monitor</span></span>
- <span data-ttu-id="113a1-175">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="113a1-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="113a1-176">Az.KeyVault</span></span>
- <span data-ttu-id="113a1-177">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="113a1-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="113a1-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="113a1-178">Az.MachineLearning</span></span>
- <span data-ttu-id="113a1-179">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="113a1-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="113a1-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="113a1-180">Az.Media</span></span>
- <span data-ttu-id="113a1-181">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="113a1-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="113a1-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="113a1-182">Az.Network</span></span>
<span data-ttu-id="113a1-183">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="113a1-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="113a1-184">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="113a1-184">New cmdlets added:</span></span>
        - <span data-ttu-id="113a1-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="113a1-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="113a1-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="113a1-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="113a1-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="113a1-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="113a1-193">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="113a1-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="113a1-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="113a1-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="113a1-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="113a1-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="113a1-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="113a1-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="113a1-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="113a1-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="113a1-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="113a1-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="113a1-199">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="113a1-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="113a1-200">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="113a1-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="113a1-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="113a1-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="113a1-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="113a1-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="113a1-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="113a1-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="113a1-204">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="113a1-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="113a1-205">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="113a1-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="113a1-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="113a1-207">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="113a1-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="113a1-208">Az.Profile</span></span>
- <span data-ttu-id="113a1-209">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="113a1-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="113a1-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="113a1-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="113a1-211">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="113a1-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-212">Az.Resources</span></span>
- <span data-ttu-id="113a1-213">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="113a1-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="113a1-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="113a1-215">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="113a1-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="113a1-216">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="113a1-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="113a1-217">Az.SIgnalR</span></span>
- <span data-ttu-id="113a1-218">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="113a1-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="113a1-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-219">Az.Sql</span></span>
- <span data-ttu-id="113a1-220">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="113a1-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="113a1-221">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="113a1-222">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="113a1-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="113a1-223">Az.Storage</span></span>
- <span data-ttu-id="113a1-224">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="113a1-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="113a1-225">Az.Websites</span></span>
- <span data-ttu-id="113a1-226">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="113a1-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="113a1-227">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="113a1-228">Generale</span><span class="sxs-lookup"><span data-stu-id="113a1-228">General</span></span>

* <span data-ttu-id="113a1-229">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="113a1-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="113a1-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-230">Az.Compute</span></span>

* <span data-ttu-id="113a1-231">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="113a1-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="113a1-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="113a1-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="113a1-233">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="113a1-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="113a1-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="113a1-234">Az.FrontDoor</span></span>

* <span data-ttu-id="113a1-235">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="113a1-235">Fixed some broken links</span></span>
    - <span data-ttu-id="113a1-236">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="113a1-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="113a1-237">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="113a1-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="113a1-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="113a1-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="113a1-239">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="113a1-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="113a1-240">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="113a1-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="113a1-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-241">Az.Resources</span></span>

* <span data-ttu-id="113a1-242">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="113a1-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="113a1-243">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="113a1-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="113a1-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-244">Az.Sql</span></span>

* <span data-ttu-id="113a1-245">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="113a1-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="113a1-246">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="113a1-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="113a1-247">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="113a1-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="113a1-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="113a1-248">Az.Storage</span></span>

* <span data-ttu-id="113a1-249">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="113a1-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="113a1-250">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="113a1-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="113a1-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="113a1-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="113a1-252">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="113a1-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="113a1-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="113a1-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="113a1-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="113a1-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="113a1-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="113a1-255">Az.Websites</span></span>

* <span data-ttu-id="113a1-256">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="113a1-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="113a1-257">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="113a1-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="113a1-258">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="113a1-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="113a1-259">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="113a1-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="113a1-260">Az.ApiManagement</span></span>
* <span data-ttu-id="113a1-261">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="113a1-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="113a1-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="113a1-262">Az.Automation</span></span>
* <span data-ttu-id="113a1-263">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="113a1-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="113a1-264">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="113a1-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="113a1-265">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="113a1-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="113a1-266">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="113a1-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="113a1-267">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="113a1-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="113a1-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-268">Az.Compute</span></span>
* <span data-ttu-id="113a1-269">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="113a1-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="113a1-270">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="113a1-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="113a1-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="113a1-272">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="113a1-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="113a1-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="113a1-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="113a1-274">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="113a1-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="113a1-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="113a1-275">Az.Network</span></span>
* <span data-ttu-id="113a1-276">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="113a1-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="113a1-277">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="113a1-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="113a1-278">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="113a1-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="113a1-279">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="113a1-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="113a1-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="113a1-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="113a1-281">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="113a1-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="113a1-282">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="113a1-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="113a1-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="113a1-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="113a1-284">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="113a1-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="113a1-285">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="113a1-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="113a1-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="113a1-286">Az.Relay</span></span>
* <span data-ttu-id="113a1-287">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="113a1-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="113a1-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-288">Az.Resources</span></span>
* <span data-ttu-id="113a1-289">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="113a1-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="113a1-290">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="113a1-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="113a1-291">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="113a1-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="113a1-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="113a1-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="113a1-293">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="113a1-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="113a1-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-294">Az.Sql</span></span>
* <span data-ttu-id="113a1-295">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="113a1-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="113a1-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="113a1-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="113a1-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="113a1-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="113a1-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="113a1-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="113a1-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="113a1-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="113a1-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="113a1-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="113a1-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="113a1-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="113a1-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="113a1-304">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="113a1-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="113a1-305">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="113a1-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="113a1-306">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="113a1-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="113a1-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="113a1-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="113a1-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="113a1-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="113a1-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="113a1-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="113a1-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="113a1-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="113a1-311">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="113a1-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="113a1-312">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="113a1-313">Generale</span><span class="sxs-lookup"><span data-stu-id="113a1-313">General</span></span>
* <span data-ttu-id="113a1-314">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="113a1-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="113a1-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="113a1-315">Az.Profile</span></span>
* <span data-ttu-id="113a1-316">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="113a1-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="113a1-317">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="113a1-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="113a1-318">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="113a1-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="113a1-319">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="113a1-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="113a1-320">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="113a1-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="113a1-321">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="113a1-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="113a1-322">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="113a1-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="113a1-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="113a1-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="113a1-324">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="113a1-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="113a1-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-325">Az.Compute</span></span>
* <span data-ttu-id="113a1-326">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="113a1-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="113a1-327">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="113a1-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="113a1-328">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="113a1-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="113a1-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="113a1-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="113a1-330">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="113a1-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="113a1-331">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="113a1-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="113a1-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="113a1-332">Az.Insights</span></span>
* <span data-ttu-id="113a1-333">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="113a1-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="113a1-334">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="113a1-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="113a1-335">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="113a1-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="113a1-336">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="113a1-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="113a1-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="113a1-337">Az.Network</span></span>
* <span data-ttu-id="113a1-338">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="113a1-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="113a1-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="113a1-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="113a1-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="113a1-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="113a1-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="113a1-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="113a1-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="113a1-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="113a1-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="113a1-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="113a1-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="113a1-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="113a1-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="113a1-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="113a1-346">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="113a1-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="113a1-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-347">Az.Resources</span></span>
* <span data-ttu-id="113a1-348">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="113a1-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="113a1-349">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="113a1-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="113a1-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="113a1-350">Az.ServiceBus</span></span>
* <span data-ttu-id="113a1-351">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="113a1-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="113a1-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="113a1-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="113a1-353">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="113a1-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="113a1-354">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="113a1-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="113a1-355">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="113a1-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="113a1-356">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="113a1-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="113a1-357">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="113a1-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="113a1-358">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="113a1-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="113a1-359">Az.Profile</span></span>
* <span data-ttu-id="113a1-360">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="113a1-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="113a1-361">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="113a1-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="113a1-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-362">Az.Compute</span></span>
* <span data-ttu-id="113a1-363">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="113a1-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="113a1-364">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="113a1-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="113a1-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="113a1-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="113a1-366">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="113a1-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="113a1-367">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="113a1-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="113a1-368">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="113a1-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="113a1-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="113a1-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="113a1-370">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="113a1-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="113a1-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="113a1-371">Az.Network</span></span>
* <span data-ttu-id="113a1-372">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="113a1-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="113a1-373">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="113a1-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="113a1-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-374">Az.Resources</span></span>
* <span data-ttu-id="113a1-375">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="113a1-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="113a1-376">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="113a1-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="113a1-377">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="113a1-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="113a1-378">Azure.Storage</span></span>
* <span data-ttu-id="113a1-379">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="113a1-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="113a1-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="113a1-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="113a1-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="113a1-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="113a1-382">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="113a1-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="113a1-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="113a1-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="113a1-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="113a1-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="113a1-385">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="113a1-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="113a1-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="113a1-386">Az.Compute</span></span>
* <span data-ttu-id="113a1-387">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="113a1-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="113a1-388">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="113a1-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="113a1-389">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="113a1-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="113a1-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="113a1-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="113a1-391">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="113a1-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="113a1-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="113a1-392">Az.Network</span></span>
* <span data-ttu-id="113a1-393">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="113a1-394">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="113a1-394">new cmdlets added</span></span>
    - <span data-ttu-id="113a1-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="113a1-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="113a1-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="113a1-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="113a1-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="113a1-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="113a1-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="113a1-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="113a1-401">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="113a1-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="113a1-402">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="113a1-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="113a1-403">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="113a1-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="113a1-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="113a1-404">Az.RedisCache</span></span>
* <span data-ttu-id="113a1-405">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="113a1-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="113a1-406">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="113a1-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="113a1-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="113a1-407">Az.Resources</span></span>
* <span data-ttu-id="113a1-408">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="113a1-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="113a1-409">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="113a1-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="113a1-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="113a1-410">Az.Sql</span></span>
* <span data-ttu-id="113a1-411">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="113a1-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="113a1-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="113a1-412">Az.Websites</span></span>
* <span data-ttu-id="113a1-413">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="113a1-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="113a1-414">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="113a1-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="113a1-415">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="113a1-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="113a1-416">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="113a1-416">Initial Release</span></span>