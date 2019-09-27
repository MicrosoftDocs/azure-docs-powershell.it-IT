---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226440"
---
## <a name="270---september-2019"></a><span data-ttu-id="18ace-101">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="18ace-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-102">Az.ApiManagement</span></span>
* <span data-ttu-id="18ace-103">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="18ace-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="18ace-104">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="18ace-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="18ace-105">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="18ace-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-106">Az.Automation</span></span>
* <span data-ttu-id="18ace-107">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="18ace-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="18ace-108">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="18ace-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="18ace-109">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="18ace-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-110">Az.Compute</span></span>
* <span data-ttu-id="18ace-111">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="18ace-112">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="18ace-113">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="18ace-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="18ace-114">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="18ace-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="18ace-115">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="18ace-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="18ace-116">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="18ace-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="18ace-117">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="18ace-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="18ace-118">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="18ace-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="18ace-119">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="18ace-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-120">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-121">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="18ace-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="18ace-122">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="18ace-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="18ace-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="18ace-123">Az.HDInsight</span></span>
* <span data-ttu-id="18ace-124">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="18ace-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="18ace-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-125">Az.IotHub</span></span>
* <span data-ttu-id="18ace-126">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="18ace-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="18ace-127">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="18ace-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="18ace-128">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="18ace-128">New cmdlets are:</span></span>
    - <span data-ttu-id="18ace-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="18ace-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="18ace-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="18ace-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="18ace-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="18ace-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="18ace-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="18ace-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-133">Az.Monitor</span></span>
* <span data-ttu-id="18ace-134">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="18ace-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="18ace-135">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="18ace-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="18ace-136">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="18ace-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="18ace-137">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="18ace-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="18ace-138">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="18ace-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="18ace-139">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="18ace-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="18ace-140">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ace-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="18ace-141">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="18ace-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="18ace-142">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="18ace-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="18ace-143">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="18ace-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="18ace-144">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="18ace-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="18ace-145">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="18ace-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="18ace-146">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="18ace-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="18ace-147">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="18ace-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="18ace-148">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="18ace-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="18ace-149">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="18ace-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="18ace-150">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="18ace-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="18ace-151">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="18ace-152">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="18ace-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="18ace-153">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-153">Overall improved help files</span></span>
* <span data-ttu-id="18ace-154">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="18ace-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-155">Az.Network</span></span>
* <span data-ttu-id="18ace-156">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="18ace-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="18ace-157">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="18ace-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="18ace-158">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="18ace-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="18ace-159">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="18ace-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="18ace-160">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="18ace-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="18ace-161">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="18ace-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="18ace-162">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="18ace-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="18ace-163">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18ace-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="18ace-164">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="18ace-165">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="18ace-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="18ace-166">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="18ace-167">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="18ace-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="18ace-168">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-168">New cmdlets</span></span>
        - <span data-ttu-id="18ace-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="18ace-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="18ace-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="18ace-171">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="18ace-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="18ace-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="18ace-172">New-VpnSite</span></span>
        - <span data-ttu-id="18ace-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="18ace-173">Update-VpnSite</span></span>
        - <span data-ttu-id="18ace-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-174">New-VpnConnection</span></span>
        - <span data-ttu-id="18ace-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-175">Update-VpnConnection</span></span>
* <span data-ttu-id="18ace-176">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="18ace-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-178">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="18ace-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="18ace-179">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="18ace-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-180">Az.Resources</span></span>
* <span data-ttu-id="18ace-181">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="18ace-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-183">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="18ace-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="18ace-184">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="18ace-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="18ace-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="18ace-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="18ace-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="18ace-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="18ace-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="18ace-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="18ace-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="18ace-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="18ace-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="18ace-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="18ace-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="18ace-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="18ace-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="18ace-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="18ace-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="18ace-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="18ace-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="18ace-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="18ace-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="18ace-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="18ace-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="18ace-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="18ace-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="18ace-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="18ace-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="18ace-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="18ace-198">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="18ace-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="18ace-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="18ace-199">Az.SignalR</span></span>
* <span data-ttu-id="18ace-200">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="18ace-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-201">Az.Sql</span></span>
* <span data-ttu-id="18ace-202">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="18ace-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="18ace-203">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="18ace-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="18ace-204">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="18ace-205">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="18ace-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="18ace-206">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="18ace-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-207">Az.Storage</span></span>
* <span data-ttu-id="18ace-208">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="18ace-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="18ace-209">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="18ace-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="18ace-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="18ace-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="18ace-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="18ace-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="18ace-212">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="18ace-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="18ace-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="18ace-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="18ace-214">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="18ace-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="18ace-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="18ace-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="18ace-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="18ace-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="18ace-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="18ace-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="18ace-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="18ace-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-219">Az.Websites</span></span>
* <span data-ttu-id="18ace-220">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="18ace-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="18ace-221">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="18ace-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="18ace-222">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="18ace-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="18ace-223">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="18ace-224">Generale</span><span class="sxs-lookup"><span data-stu-id="18ace-224">General</span></span>
* <span data-ttu-id="18ace-225">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="18ace-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="18ace-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-226">Az.Accounts</span></span>
* <span data-ttu-id="18ace-227">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="18ace-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="18ace-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="18ace-228">Az.Aks</span></span>
* <span data-ttu-id="18ace-229">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="18ace-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="18ace-230">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="18ace-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="18ace-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-231">Az.ApiManagement</span></span>
* <span data-ttu-id="18ace-232">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="18ace-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="18ace-233">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="18ace-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="18ace-234">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="18ace-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="18ace-235">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="18ace-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="18ace-236">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="18ace-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="18ace-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="18ace-237">Az.Batch</span></span>
* <span data-ttu-id="18ace-238">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="18ace-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="18ace-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="18ace-239">Az.Cdn</span></span>
* <span data-ttu-id="18ace-240">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="18ace-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-241">Az.Compute</span></span>
* <span data-ttu-id="18ace-242">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="18ace-243">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="18ace-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="18ace-244">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="18ace-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="18ace-245">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="18ace-246">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="18ace-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="18ace-247">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="18ace-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="18ace-248">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="18ace-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="18ace-249">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="18ace-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-250">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-251">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="18ace-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="18ace-252">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="18ace-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="18ace-253">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="18ace-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="18ace-254">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="18ace-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-256">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="18ace-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="18ace-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="18ace-257">Az.EventHub</span></span>
* <span data-ttu-id="18ace-258">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="18ace-259">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="18ace-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="18ace-260">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="18ace-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="18ace-261">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="18ace-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="18ace-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="18ace-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="18ace-263">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="18ace-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-264">Az.Monitor</span></span>
* <span data-ttu-id="18ace-265">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-266">Az.Network</span></span>
* <span data-ttu-id="18ace-267">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="18ace-268">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="18ace-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="18ace-269">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="18ace-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="18ace-270">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="18ace-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="18ace-271">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="18ace-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="18ace-272">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="18ace-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="18ace-273">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="18ace-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-275">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="18ace-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="18ace-276">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="18ace-276">Added example</span></span>
    - <span data-ttu-id="18ace-277">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="18ace-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="18ace-278">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="18ace-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="18ace-279">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="18ace-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-281">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-282">Az.Resources</span></span>
* <span data-ttu-id="18ace-283">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="18ace-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="18ace-284">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="18ace-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="18ace-285">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="18ace-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="18ace-286">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-287">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-288">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="18ace-289">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="18ace-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="18ace-290">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="18ace-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-292">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="18ace-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="18ace-293">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="18ace-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="18ace-294">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="18ace-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="18ace-295">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="18ace-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="18ace-296">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="18ace-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="18ace-297">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="18ace-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-298">Az.Sql</span></span>
* <span data-ttu-id="18ace-299">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="18ace-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-300">Az.Storage</span></span>
* <span data-ttu-id="18ace-301">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="18ace-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="18ace-302">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="18ace-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="18ace-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="18ace-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="18ace-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="18ace-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="18ace-305">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="18ace-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="18ace-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="18ace-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-307">Az.Websites</span></span>
* <span data-ttu-id="18ace-308">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18ace-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="18ace-309">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-310">Az.Accounts</span></span>
* <span data-ttu-id="18ace-311">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="18ace-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="18ace-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="18ace-313">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="18ace-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="18ace-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-314">Az.Automation</span></span>
* <span data-ttu-id="18ace-315">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="18ace-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-317">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="18ace-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-318">Az.Compute</span></span>
* <span data-ttu-id="18ace-319">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18ace-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="18ace-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="18ace-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="18ace-321">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="18ace-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="18ace-322">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="18ace-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-323">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-324">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="18ace-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="18ace-325">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="18ace-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="18ace-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="18ace-326">Az.EventHub</span></span>
* <span data-ttu-id="18ace-327">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="18ace-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="18ace-328">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="18ace-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="18ace-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-329">Az.KeyVault</span></span>
* <span data-ttu-id="18ace-330">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="18ace-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="18ace-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="18ace-331">Az.LogicApp</span></span>
* <span data-ttu-id="18ace-332">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="18ace-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="18ace-333">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="18ace-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="18ace-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="18ace-334">Az.ManagedServices</span></span>
* <span data-ttu-id="18ace-335">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="18ace-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-336">Az.Network</span></span>
* <span data-ttu-id="18ace-337">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="18ace-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="18ace-338">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-338">New cmdlets</span></span>
        - <span data-ttu-id="18ace-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ace-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="18ace-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="18ace-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="18ace-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="18ace-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="18ace-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="18ace-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="18ace-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="18ace-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="18ace-347">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="18ace-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="18ace-348">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="18ace-349">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="18ace-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="18ace-350">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="18ace-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="18ace-351">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="18ace-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="18ace-352">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="18ace-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="18ace-353">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-353">Updated cmdlets</span></span>
        - <span data-ttu-id="18ace-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="18ace-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="18ace-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="18ace-357">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="18ace-358">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="18ace-359">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="18ace-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="18ace-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="18ace-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="18ace-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="18ace-363">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="18ace-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="18ace-364">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="18ace-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="18ace-365">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="18ace-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-367">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="18ace-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="18ace-368">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="18ace-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-370">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="18ace-371">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="18ace-372">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="18ace-373">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="18ace-374">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="18ace-375">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="18ace-376">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="18ace-377">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="18ace-378">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="18ace-379">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="18ace-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-380">Az.Resources</span></span>
- <span data-ttu-id="18ace-381">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="18ace-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="18ace-382">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="18ace-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-383">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-384">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="18ace-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="18ace-385">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="18ace-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-386">Az.Sql</span></span>
* <span data-ttu-id="18ace-387">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="18ace-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="18ace-388">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="18ace-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="18ace-389">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="18ace-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-390">Az.Storage</span></span>
* <span data-ttu-id="18ace-391">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="18ace-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="18ace-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="18ace-392">Az.StorageSync</span></span>
* <span data-ttu-id="18ace-393">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="18ace-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="18ace-394">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="18ace-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-395">Az.Websites</span></span>
* <span data-ttu-id="18ace-396">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18ace-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="18ace-397">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="18ace-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="18ace-398">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="18ace-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="18ace-399">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-400">Az.Accounts</span></span>
* <span data-ttu-id="18ace-401">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="18ace-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="18ace-402">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="18ace-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="18ace-403">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="18ace-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="18ace-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="18ace-404">Az.Advisor</span></span>
* <span data-ttu-id="18ace-405">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="18ace-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="18ace-406">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="18ace-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="18ace-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-407">Az.ApiManagement</span></span>
* <span data-ttu-id="18ace-408">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="18ace-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="18ace-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="18ace-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="18ace-410">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="18ace-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="18ace-411">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="18ace-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="18ace-412">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="18ace-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="18ace-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="18ace-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="18ace-414">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="18ace-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-415">Az.Automation</span></span>
* <span data-ttu-id="18ace-416">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="18ace-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-417">Az.Compute</span></span>
* <span data-ttu-id="18ace-418">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-419">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-420">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="18ace-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="18ace-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="18ace-421">Az.EventGrid</span></span>
* <span data-ttu-id="18ace-422">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="18ace-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="18ace-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-423">Az.IotHub</span></span>
* <span data-ttu-id="18ace-424">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ace-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-425">Az.Network</span></span>
* <span data-ttu-id="18ace-426">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="18ace-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="18ace-427">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="18ace-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="18ace-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="18ace-429">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="18ace-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="18ace-430">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="18ace-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-432">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="18ace-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-434">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="18ace-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-435">Az.Resources</span></span>
    - <span data-ttu-id="18ace-436">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="18ace-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="18ace-437">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="18ace-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="18ace-438">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="18ace-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="18ace-439">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="18ace-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-440">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-441">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="18ace-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-442">Az.Sql</span></span>
* <span data-ttu-id="18ace-443">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="18ace-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="18ace-444">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="18ace-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="18ace-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="18ace-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="18ace-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="18ace-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="18ace-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="18ace-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="18ace-451">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="18ace-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-452">Az.Storage</span></span>
* <span data-ttu-id="18ace-453">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="18ace-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="18ace-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="18ace-455">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="18ace-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="18ace-456">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="18ace-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="18ace-457">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="18ace-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="18ace-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="18ace-460">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="18ace-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="18ace-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="18ace-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="18ace-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="18ace-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="18ace-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="18ace-463">Az.StorageSync</span></span>
* <span data-ttu-id="18ace-464">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="18ace-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="18ace-465">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-466">Az.Accounts</span></span>
* <span data-ttu-id="18ace-467">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="18ace-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="18ace-468">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="18ace-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="18ace-469">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="18ace-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="18ace-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="18ace-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="18ace-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="18ace-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-472">Az.Compute</span></span>
* <span data-ttu-id="18ace-473">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="18ace-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="18ace-474">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="18ace-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="18ace-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="18ace-475">Az.Dns</span></span>
* <span data-ttu-id="18ace-476">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="18ace-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="18ace-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="18ace-477">Az.EventGrid</span></span>
* <span data-ttu-id="18ace-478">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="18ace-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="18ace-479">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-479">New cmdlets:</span></span>
    - <span data-ttu-id="18ace-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="18ace-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="18ace-481">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="18ace-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="18ace-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="18ace-483">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="18ace-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="18ace-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="18ace-485">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="18ace-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="18ace-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="18ace-487">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="18ace-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="18ace-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="18ace-489">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="18ace-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="18ace-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="18ace-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="18ace-491">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="18ace-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="18ace-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="18ace-493">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="18ace-494">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="18ace-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="18ace-495">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="18ace-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="18ace-496">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="18ace-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="18ace-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="18ace-498">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="18ace-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="18ace-499">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="18ace-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="18ace-500">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="18ace-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="18ace-501">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="18ace-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="18ace-502">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="18ace-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="18ace-503">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="18ace-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="18ace-504">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="18ace-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="18ace-505">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="18ace-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="18ace-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="18ace-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="18ace-507">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="18ace-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="18ace-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="18ace-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="18ace-509">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="18ace-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="18ace-510">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="18ace-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="18ace-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="18ace-511">Az.FrontDoor</span></span>
* <span data-ttu-id="18ace-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="18ace-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="18ace-513">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="18ace-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="18ace-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="18ace-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="18ace-515">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="18ace-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-516">Az.Network</span></span>
* <span data-ttu-id="18ace-517">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="18ace-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="18ace-518">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-518">New cmdlets</span></span>
        - <span data-ttu-id="18ace-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="18ace-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="18ace-520">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="18ace-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="18ace-521">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-521">New cmdlets</span></span> 
        - <span data-ttu-id="18ace-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="18ace-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="18ace-523">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="18ace-524">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-524">New cmdlets</span></span> 
        - <span data-ttu-id="18ace-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="18ace-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="18ace-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18ace-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="18ace-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="18ace-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="18ace-530">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ace-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="18ace-531">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-531">New cmdlets</span></span>
        - <span data-ttu-id="18ace-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ace-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="18ace-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ace-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="18ace-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ace-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="18ace-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="18ace-536">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="18ace-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="18ace-537">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="18ace-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="18ace-538">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="18ace-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="18ace-539">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="18ace-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="18ace-540">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="18ace-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="18ace-541">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18ace-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="18ace-542">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="18ace-543">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="18ace-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="18ace-544">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="18ace-545">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="18ace-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="18ace-546">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="18ace-547">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="18ace-548">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="18ace-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="18ace-549">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="18ace-550">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="18ace-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="18ace-551">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="18ace-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="18ace-552">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="18ace-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="18ace-553">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="18ace-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="18ace-554">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="18ace-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="18ace-555">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="18ace-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="18ace-556">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="18ace-557">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="18ace-558">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-560">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="18ace-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-561">Az.Resources</span></span>
* <span data-ttu-id="18ace-562">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="18ace-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="18ace-563">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="18ace-564">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="18ace-565">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="18ace-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-567">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="18ace-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-568">Az.Sql</span></span>
* <span data-ttu-id="18ace-569">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="18ace-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="18ace-570">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="18ace-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="18ace-571">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="18ace-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="18ace-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18ace-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="18ace-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18ace-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="18ace-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18ace-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="18ace-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="18ace-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="18ace-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="18ace-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-577">Az.Storage</span></span>
* <span data-ttu-id="18ace-578">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="18ace-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="18ace-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="18ace-580">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="18ace-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="18ace-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-582">Az.Websites</span></span>
* <span data-ttu-id="18ace-583">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="18ace-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="18ace-584">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="18ace-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="18ace-585">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="18ace-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="18ace-586">Az.Cdn</span></span>
* <span data-ttu-id="18ace-587">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="18ace-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-588">Az.Compute</span></span>
* <span data-ttu-id="18ace-589">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="18ace-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="18ace-590">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="18ace-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="18ace-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="18ace-591">Az.EventHub</span></span>
* <span data-ttu-id="18ace-592">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="18ace-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="18ace-593">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ace-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-594">Az.Network</span></span>
* <span data-ttu-id="18ace-595">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="18ace-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="18ace-596">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="18ace-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="18ace-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="18ace-598">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="18ace-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-600">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="18ace-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-601">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-602">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ace-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-604">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="18ace-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="18ace-605">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="18ace-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-606">Az.Sql</span></span>
* <span data-ttu-id="18ace-607">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="18ace-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="18ace-608">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="18ace-609">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="18ace-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="18ace-610">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="18ace-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-611">Az.Websites</span></span>
* <span data-ttu-id="18ace-612">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="18ace-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="18ace-613">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="18ace-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-614">Az.ApiManagement</span></span>
* <span data-ttu-id="18ace-615">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="18ace-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="18ace-616">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="18ace-617">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="18ace-618">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="18ace-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="18ace-619">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="18ace-620">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="18ace-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="18ace-621">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="18ace-622">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="18ace-623">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="18ace-624">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="18ace-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="18ace-625">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="18ace-626">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="18ace-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="18ace-627">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="18ace-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="18ace-628">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="18ace-629">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="18ace-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="18ace-630">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="18ace-631">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="18ace-632">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="18ace-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="18ace-633">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="18ace-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="18ace-634">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="18ace-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="18ace-635">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="18ace-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="18ace-636">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="18ace-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="18ace-637">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="18ace-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="18ace-638">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="18ace-639">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="18ace-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="18ace-640">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="18ace-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="18ace-641">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="18ace-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="18ace-642">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="18ace-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="18ace-643">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="18ace-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="18ace-644">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="18ace-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="18ace-645">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="18ace-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="18ace-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="18ace-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="18ace-647">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="18ace-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="18ace-648">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="18ace-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="18ace-649">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="18ace-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="18ace-650">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="18ace-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="18ace-651">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="18ace-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="18ace-652">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="18ace-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="18ace-653">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="18ace-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="18ace-654">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="18ace-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="18ace-655">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="18ace-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="18ace-656">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="18ace-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="18ace-657">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="18ace-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="18ace-658">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="18ace-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="18ace-659">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="18ace-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="18ace-660">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="18ace-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="18ace-661">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="18ace-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="18ace-662">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="18ace-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="18ace-663">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="18ace-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="18ace-664">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="18ace-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="18ace-665">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="18ace-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="18ace-666">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="18ace-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="18ace-667">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="18ace-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="18ace-668">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="18ace-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="18ace-669">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="18ace-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="18ace-670">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="18ace-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="18ace-671">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="18ace-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="18ace-672">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="18ace-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="18ace-673">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="18ace-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="18ace-674">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="18ace-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="18ace-675">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="18ace-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="18ace-676">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="18ace-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="18ace-677">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="18ace-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="18ace-678">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="18ace-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="18ace-679">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="18ace-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="18ace-680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="18ace-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="18ace-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="18ace-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="18ace-682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="18ace-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="18ace-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="18ace-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="18ace-684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="18ace-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="18ace-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="18ace-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="18ace-686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="18ace-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="18ace-687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="18ace-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="18ace-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="18ace-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="18ace-689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="18ace-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="18ace-690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="18ace-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="18ace-691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="18ace-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-692">Az.Automation</span></span>
* <span data-ttu-id="18ace-693">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="18ace-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="18ace-694">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="18ace-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="18ace-695">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="18ace-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="18ace-696">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="18ace-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="18ace-697">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="18ace-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="18ace-698">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="18ace-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="18ace-699">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="18ace-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-700">Az.Compute</span></span>
* <span data-ttu-id="18ace-701">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="18ace-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="18ace-702">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="18ace-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-704">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-705">Az.Monitor</span></span>
* <span data-ttu-id="18ace-706">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-707">Az.Network</span></span>
* <span data-ttu-id="18ace-708">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="18ace-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="18ace-709">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="18ace-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="18ace-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="18ace-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="18ace-711">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ace-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-712">Az.Resources</span></span>
* <span data-ttu-id="18ace-713">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="18ace-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-714">Az.Sql</span></span>
* <span data-ttu-id="18ace-715">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="18ace-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="18ace-716">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-717">Az.Accounts</span></span>
* <span data-ttu-id="18ace-718">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="18ace-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-720">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="18ace-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="18ace-721">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="18ace-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-722">Az.Compute</span></span>
* <span data-ttu-id="18ace-723">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="18ace-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="18ace-724">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="18ace-725">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="18ace-726">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="18ace-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="18ace-727">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="18ace-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="18ace-728">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="18ace-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="18ace-729">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="18ace-729">Breaking changes</span></span>
    - <span data-ttu-id="18ace-730">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="18ace-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="18ace-731">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="18ace-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="18ace-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="18ace-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="18ace-733">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="18ace-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="18ace-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="18ace-734">Az.Dns</span></span>
* <span data-ttu-id="18ace-735">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="18ace-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="18ace-736">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="18ace-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="18ace-737">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="18ace-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="18ace-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="18ace-738">Az.FrontDoor</span></span>
* <span data-ttu-id="18ace-739">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="18ace-740">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="18ace-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="18ace-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="18ace-741">Az.HDInsight</span></span>
* <span data-ttu-id="18ace-742">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="18ace-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="18ace-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="18ace-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="18ace-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="18ace-745">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="18ace-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="18ace-746">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="18ace-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="18ace-747">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="18ace-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="18ace-748">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="18ace-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-749">Az.Monitor</span></span>
* <span data-ttu-id="18ace-750">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="18ace-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="18ace-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="18ace-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="18ace-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="18ace-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="18ace-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="18ace-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="18ace-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="18ace-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="18ace-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="18ace-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="18ace-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="18ace-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="18ace-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="18ace-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="18ace-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="18ace-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="18ace-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="18ace-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="18ace-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="18ace-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="18ace-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="18ace-762">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="18ace-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="18ace-763">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="18ace-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-764">Az.Network</span></span>
* <span data-ttu-id="18ace-765">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="18ace-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="18ace-766">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-766">New cmdlets</span></span>
        - <span data-ttu-id="18ace-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="18ace-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="18ace-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="18ace-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="18ace-771">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18ace-771">Updated cmdlets</span></span>
        - <span data-ttu-id="18ace-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="18ace-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="18ace-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="18ace-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="18ace-774">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="18ace-775">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="18ace-776">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="18ace-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="18ace-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="18ace-778">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="18ace-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="18ace-779">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="18ace-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="18ace-780">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="18ace-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-782">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="18ace-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="18ace-783">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="18ace-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="18ace-784">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="18ace-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="18ace-785">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="18ace-786">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="18ace-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="18ace-787">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="18ace-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="18ace-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="18ace-788">Az.Relay</span></span>
* <span data-ttu-id="18ace-789">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="18ace-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-790">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-791">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18ace-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-792">Az.Storage</span></span>
* <span data-ttu-id="18ace-793">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="18ace-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="18ace-794">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="18ace-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="18ace-795">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="18ace-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="18ace-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="18ace-797">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="18ace-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="18ace-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="18ace-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="18ace-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-801">Az.Websites</span></span>
* <span data-ttu-id="18ace-802">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18ace-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="18ace-803">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="18ace-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="18ace-804">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="18ace-805">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="18ace-805">Highlights since the last major release</span></span>
* <span data-ttu-id="18ace-806">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="18ace-806">General availability of `Az` module</span></span>
* <span data-ttu-id="18ace-807">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="18ace-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="18ace-808">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="18ace-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="18ace-809">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="18ace-810">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="18ace-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="18ace-811">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="18ace-812">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="18ace-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="18ace-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-813">Az.Accounts</span></span>
* <span data-ttu-id="18ace-814">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="18ace-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="18ace-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="18ace-815">Az.Batch</span></span>
* <span data-ttu-id="18ace-816">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="18ace-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="18ace-817">Az.Cdn</span></span>
* <span data-ttu-id="18ace-818">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-820">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-821">Az.Compute</span></span>
* <span data-ttu-id="18ace-822">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="18ace-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="18ace-823">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-824">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="18ace-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-825">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-826">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="18ace-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-828">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="18ace-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="18ace-829">Az.EventGrid</span></span>
* <span data-ttu-id="18ace-830">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="18ace-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="18ace-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="18ace-831">Az.EventHub</span></span>
* <span data-ttu-id="18ace-832">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18ace-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="18ace-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="18ace-833">Az.HDInsight</span></span>
* <span data-ttu-id="18ace-834">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="18ace-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-835">Az.IotHub</span></span>
* <span data-ttu-id="18ace-836">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="18ace-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-837">Az.KeyVault</span></span>
* <span data-ttu-id="18ace-838">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-839">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="18ace-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="18ace-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="18ace-840">Az.MachineLearning</span></span>
* <span data-ttu-id="18ace-841">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="18ace-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="18ace-842">Az.Media</span></span>
* <span data-ttu-id="18ace-843">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-844">Az.Monitor</span></span>
  * <span data-ttu-id="18ace-845">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="18ace-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="18ace-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="18ace-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="18ace-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="18ace-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="18ace-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="18ace-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="18ace-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="18ace-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="18ace-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="18ace-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="18ace-851">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="18ace-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-852">Az.Network</span></span>
* <span data-ttu-id="18ace-853">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-854">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="18ace-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="18ace-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="18ace-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="18ace-856">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-858">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="18ace-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="18ace-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="18ace-860">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-862">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-863">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="18ace-864">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="18ace-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="18ace-865">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="18ace-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="18ace-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="18ace-866">Az.RedisCache</span></span>
* <span data-ttu-id="18ace-867">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-868">Az.Resources</span></span>
* <span data-ttu-id="18ace-869">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="18ace-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-870">Az.Sql</span></span>
* <span data-ttu-id="18ace-871">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="18ace-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="18ace-872">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-873">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="18ace-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="18ace-874">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="18ace-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="18ace-875">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="18ace-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="18ace-876">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="18ace-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="18ace-877">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="18ace-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-878">Az.Websites</span></span>
* <span data-ttu-id="18ace-879">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="18ace-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="18ace-880">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="18ace-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="18ace-881">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="18ace-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="18ace-882">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="18ace-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="18ace-883">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="18ace-884">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="18ace-884">Highlights since the last major release</span></span>
* <span data-ttu-id="18ace-885">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="18ace-885">General availability of `Az` module</span></span>
* <span data-ttu-id="18ace-886">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="18ace-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="18ace-887">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="18ace-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="18ace-888">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="18ace-889">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="18ace-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="18ace-890">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="18ace-891">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="18ace-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="18ace-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-892">Az.Accounts</span></span>
* <span data-ttu-id="18ace-893">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="18ace-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="18ace-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="18ace-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="18ace-895">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="18ace-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="18ace-896">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="18ace-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-897">Az.Automation</span></span>
* <span data-ttu-id="18ace-898">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="18ace-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="18ace-899">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="18ace-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="18ace-900">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-901">Az.Compute</span></span>
* <span data-ttu-id="18ace-902">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="18ace-903">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="18ace-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="18ace-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="18ace-905">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="18ace-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-906">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-907">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="18ace-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="18ace-908">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="18ace-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-909">Az.Resources</span></span>
* <span data-ttu-id="18ace-910">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="18ace-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="18ace-911">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="18ace-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="18ace-912">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="18ace-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="18ace-913">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="18ace-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="18ace-914">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="18ace-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="18ace-915">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="18ace-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-916">Az.Sql</span></span>
* <span data-ttu-id="18ace-917">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="18ace-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-918">Az.Storage</span></span>
* <span data-ttu-id="18ace-919">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="18ace-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="18ace-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="18ace-920">New-AzStorageContext</span></span>
* <span data-ttu-id="18ace-921">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="18ace-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="18ace-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="18ace-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="18ace-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="18ace-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="18ace-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="18ace-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="18ace-926">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="18ace-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="18ace-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="18ace-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="18ace-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="18ace-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="18ace-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="18ace-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="18ace-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="18ace-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="18ace-931">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="18ace-932">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="18ace-932">Highlights since the last major release</span></span>
* <span data-ttu-id="18ace-933">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="18ace-933">General availability of `Az` module</span></span>
* <span data-ttu-id="18ace-934">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="18ace-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="18ace-935">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="18ace-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="18ace-936">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="18ace-937">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="18ace-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="18ace-938">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="18ace-939">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="18ace-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-940">Az.Automation</span></span>
* <span data-ttu-id="18ace-941">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="18ace-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="18ace-942">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="18ace-942">Dynamic grouping</span></span>
    * <span data-ttu-id="18ace-943">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="18ace-943">Pre-Post script</span></span>
    * <span data-ttu-id="18ace-944">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="18ace-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-945">Az.Compute</span></span>
* <span data-ttu-id="18ace-946">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="18ace-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="18ace-947">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="18ace-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="18ace-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-948">Az.KeyVault</span></span>
* <span data-ttu-id="18ace-949">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-950">Az.Network</span></span>
* <span data-ttu-id="18ace-951">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="18ace-952">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="18ace-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-954">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="18ace-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="18ace-955">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="18ace-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-956">Az.Resources</span></span>
* <span data-ttu-id="18ace-957">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="18ace-958">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="18ace-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-959">Az.Sql</span></span>
* <span data-ttu-id="18ace-960">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="18ace-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-961">Az.Storage</span></span>
* <span data-ttu-id="18ace-962">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="18ace-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="18ace-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="18ace-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="18ace-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="18ace-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="18ace-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="18ace-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="18ace-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="18ace-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="18ace-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-969">Az.Websites</span></span>
* <span data-ttu-id="18ace-970">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="18ace-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="18ace-971">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-972">Az.Accounts</span></span>
* <span data-ttu-id="18ace-973">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="18ace-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="18ace-974">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-975">Az.Automation</span></span>
* <span data-ttu-id="18ace-976">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="18ace-977">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="18ace-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="18ace-978">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="18ace-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="18ace-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="18ace-979">Az.Cdn</span></span>
* <span data-ttu-id="18ace-980">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="18ace-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-981">Az.Compute</span></span>
* <span data-ttu-id="18ace-982">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="18ace-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-983">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-984">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="18ace-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="18ace-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="18ace-985">Az.LogicApp</span></span>
* <span data-ttu-id="18ace-986">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="18ace-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-987">Az.Network</span></span>
* <span data-ttu-id="18ace-988">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="18ace-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-990">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="18ace-991">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="18ace-991">SDK Update</span></span>
* <span data-ttu-id="18ace-992">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="18ace-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="18ace-993">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="18ace-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-994">Az.Resources</span></span>
* <span data-ttu-id="18ace-995">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="18ace-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="18ace-996">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="18ace-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="18ace-997">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="18ace-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="18ace-998">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="18ace-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="18ace-999">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="18ace-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="18ace-1000">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="18ace-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1001">Az.Sql</span></span>
* <span data-ttu-id="18ace-1002">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="18ace-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="18ace-1003">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="18ace-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1004">Az.Storage</span></span>
* <span data-ttu-id="18ace-1005">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="18ace-1006">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="18ace-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="18ace-1008">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="18ace-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-1009">Az.Automation</span></span>
* <span data-ttu-id="18ace-1010">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="18ace-1011">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="18ace-1012">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-1014">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="18ace-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1015">Az.Compute</span></span>
* <span data-ttu-id="18ace-1016">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="18ace-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="18ace-1017">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="18ace-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="18ace-1018">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="18ace-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="18ace-1019">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="18ace-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-1021">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="18ace-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="18ace-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="18ace-1022">Az.EventHub</span></span>
* <span data-ttu-id="18ace-1023">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="18ace-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="18ace-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-1024">Az.KeyVault</span></span>
* <span data-ttu-id="18ace-1025">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18ace-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="18ace-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="18ace-1026">Az.LogicApp</span></span>
* <span data-ttu-id="18ace-1027">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="18ace-1028">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="18ace-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="18ace-1029">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="18ace-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18ace-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="18ace-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18ace-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="18ace-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18ace-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="18ace-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18ace-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="18ace-1034">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="18ace-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="18ace-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="18ace-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="18ace-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="18ace-1039">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="18ace-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="18ace-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-1040">Az.Monitor</span></span>
* <span data-ttu-id="18ace-1041">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="18ace-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1042">Az.Network</span></span>
* <span data-ttu-id="18ace-1043">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="18ace-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="18ace-1045">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="18ace-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="18ace-1046">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18ace-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="18ace-1047">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="18ace-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="18ace-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1048">Az.Resources</span></span>
* <span data-ttu-id="18ace-1049">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="18ace-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="18ace-1050">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="18ace-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="18ace-1051">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="18ace-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="18ace-1052">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="18ace-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1053">Az.Sql</span></span>
* <span data-ttu-id="18ace-1054">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="18ace-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="18ace-1055">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="18ace-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1056">Az.Websites</span></span>
* <span data-ttu-id="18ace-1057">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="18ace-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="18ace-1058">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1059">Az.Accounts</span></span>
* <span data-ttu-id="18ace-1060">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="18ace-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="18ace-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="18ace-1062">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="18ace-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1063">Az.Compute</span></span>
* <span data-ttu-id="18ace-1064">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="18ace-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="18ace-1065">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="18ace-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="18ace-1066">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="18ace-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="18ace-1068">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="18ace-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1069">Az.Resources</span></span>
* <span data-ttu-id="18ace-1070">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="18ace-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="18ace-1071">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="18ace-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="18ace-1072">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="18ace-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="18ace-1073">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="18ace-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1074">Az.Sql</span></span>
* <span data-ttu-id="18ace-1075">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="18ace-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="18ace-1076">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="18ace-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="18ace-1077">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="18ace-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="18ace-1078">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1079">Az.Accounts</span></span>
* <span data-ttu-id="18ace-1080">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="18ace-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="18ace-1082">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="18ace-1084">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="18ace-1085">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1086">Az.Accounts</span></span>
* <span data-ttu-id="18ace-1087">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="18ace-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="18ace-1088">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="18ace-1089">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="18ace-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="18ace-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="18ace-1090">Az.Aks</span></span>
* <span data-ttu-id="18ace-1091">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="18ace-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-1092">Az.Automation</span></span>
* <span data-ttu-id="18ace-1093">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="18ace-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="18ace-1094">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="18ace-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="18ace-1095">Az.Cdn</span></span>
* <span data-ttu-id="18ace-1096">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1097">Az.Compute</span></span>
* <span data-ttu-id="18ace-1098">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="18ace-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="18ace-1099">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="18ace-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="18ace-1100">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="18ace-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="18ace-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="18ace-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="18ace-1102">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="18ace-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="18ace-1103">Az.DataFactory</span></span>
* <span data-ttu-id="18ace-1104">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="18ace-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-1106">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="18ace-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="18ace-1107">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="18ace-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="18ace-1108">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="18ace-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-1109">Az.IotHub</span></span>
* <span data-ttu-id="18ace-1110">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="18ace-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="18ace-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-1111">Az.KeyVault</span></span>
* <span data-ttu-id="18ace-1112">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1113">Az.Network</span></span>
* <span data-ttu-id="18ace-1114">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1115">Az.Resources</span></span>
* <span data-ttu-id="18ace-1116">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="18ace-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="18ace-1117">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="18ace-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="18ace-1118">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="18ace-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="18ace-1119">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="18ace-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="18ace-1120">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="18ace-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="18ace-1121">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="18ace-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="18ace-1122">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="18ace-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-1124">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="18ace-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="18ace-1125">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="18ace-1125">Fix some error messages.</span></span>
* <span data-ttu-id="18ace-1126">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="18ace-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="18ace-1127">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="18ace-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="18ace-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="18ace-1128">Az.SignalR</span></span>
* <span data-ttu-id="18ace-1129">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1130">Az.Sql</span></span>
* <span data-ttu-id="18ace-1131">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="18ace-1132">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="18ace-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="18ace-1133">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="18ace-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="18ace-1134">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="18ace-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1135">Az.Storage</span></span>
* <span data-ttu-id="18ace-1136">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="18ace-1137">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="18ace-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="18ace-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="18ace-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="18ace-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="18ace-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="18ace-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="18ace-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="18ace-1141">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1142">Az.Websites</span></span>
* <span data-ttu-id="18ace-1143">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="18ace-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="18ace-1144">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="18ace-1145">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="18ace-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="18ace-1146">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="18ace-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="18ace-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1147">Az.Accounts</span></span>
* <span data-ttu-id="18ace-1148">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="18ace-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1149">Az.Compute</span></span>
* <span data-ttu-id="18ace-1150">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="18ace-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="18ace-1151">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="18ace-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="18ace-1152">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-1154">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="18ace-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="18ace-1155">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="18ace-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="18ace-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="18ace-1156">Az.EventGrid</span></span>
* <span data-ttu-id="18ace-1157">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="18ace-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="18ace-1158">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="18ace-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="18ace-1159">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="18ace-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="18ace-1160">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="18ace-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="18ace-1161">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="18ace-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="18ace-1162">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="18ace-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="18ace-1163">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="18ace-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="18ace-1164">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="18ace-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="18ace-1165">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="18ace-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="18ace-1166">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="18ace-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="18ace-1167">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="18ace-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="18ace-1168">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18ace-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="18ace-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-1169">Az.IotHub</span></span>
* <span data-ttu-id="18ace-1170">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="18ace-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="18ace-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="18ace-1171">Az.LogicApp</span></span>
* <span data-ttu-id="18ace-1172">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="18ace-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1173">Az.Resources</span></span>
* <span data-ttu-id="18ace-1174">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="18ace-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="18ace-1175">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="18ace-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="18ace-1176">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18ace-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="18ace-1177">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="18ace-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="18ace-1178">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="18ace-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="18ace-1179">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="18ace-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="18ace-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="18ace-1180">Az.SignalR</span></span>
* <span data-ttu-id="18ace-1181">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1182">Az.Sql</span></span>
* <span data-ttu-id="18ace-1183">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="18ace-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="18ace-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1184">Az.Storage</span></span>
* <span data-ttu-id="18ace-1185">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="18ace-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="18ace-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="18ace-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="18ace-1187">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="18ace-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="18ace-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="18ace-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1189">Az.Websites</span></span>
* <span data-ttu-id="18ace-1190">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="18ace-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="18ace-1191">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="18ace-1192">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="18ace-1193">Generale</span><span class="sxs-lookup"><span data-stu-id="18ace-1193">General</span></span>

- <span data-ttu-id="18ace-1194">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="18ace-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="18ace-1195">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="18ace-1195">Online help for each module</span></span>
- <span data-ttu-id="18ace-1196">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="18ace-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="18ace-1197">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="18ace-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="18ace-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1198">Az.Accounts</span></span>
- <span data-ttu-id="18ace-1199">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="18ace-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="18ace-1200">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="18ace-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="18ace-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="18ace-1202">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="18ace-1202">Fixes for #7002</span></span>
- <span data-ttu-id="18ace-1203">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="18ace-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="18ace-1204">Az.Batch</span></span>
- <span data-ttu-id="18ace-1205">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="18ace-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="18ace-1206">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="18ace-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="18ace-1207">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="18ace-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="18ace-1208">Az.Billing</span></span>
- <span data-ttu-id="18ace-1209">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="18ace-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="18ace-1211">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="18ace-1212">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="18ace-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="18ace-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="18ace-1214">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="18ace-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="18ace-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="18ace-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="18ace-1216">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="18ace-1218">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="18ace-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="18ace-1219">Az.Monitor</span></span>
- <span data-ttu-id="18ace-1220">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="18ace-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="18ace-1221">Az.KeyVault</span></span>
- <span data-ttu-id="18ace-1222">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="18ace-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="18ace-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="18ace-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="18ace-1224">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="18ace-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="18ace-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="18ace-1225">Az.Media</span></span>
- <span data-ttu-id="18ace-1226">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="18ace-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="18ace-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1227">Az.Network</span></span>
<span data-ttu-id="18ace-1228">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="18ace-1229">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="18ace-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="18ace-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="18ace-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="18ace-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="18ace-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ace-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="18ace-1238">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18ace-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="18ace-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18ace-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="18ace-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="18ace-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="18ace-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="18ace-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="18ace-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="18ace-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="18ace-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="18ace-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="18ace-1245">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="18ace-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="18ace-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="18ace-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="18ace-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="18ace-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="18ace-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="18ace-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="18ace-1249">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="18ace-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="18ace-1250">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="18ace-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="18ace-1252">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="18ace-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="18ace-1253">Az.Profile</span></span>
- <span data-ttu-id="18ace-1254">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="18ace-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="18ace-1256">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="18ace-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1257">Az.Resources</span></span>
- <span data-ttu-id="18ace-1258">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="18ace-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="18ace-1260">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="18ace-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="18ace-1261">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="18ace-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="18ace-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="18ace-1263">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="18ace-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="18ace-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1264">Az.Sql</span></span>
- <span data-ttu-id="18ace-1265">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="18ace-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="18ace-1266">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="18ace-1267">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="18ace-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1268">Az.Storage</span></span>
- <span data-ttu-id="18ace-1269">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="18ace-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1270">Az.Websites</span></span>
- <span data-ttu-id="18ace-1271">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="18ace-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="18ace-1272">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="18ace-1273">Generale</span><span class="sxs-lookup"><span data-stu-id="18ace-1273">General</span></span>

* <span data-ttu-id="18ace-1274">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="18ace-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="18ace-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1275">Az.Compute</span></span>

* <span data-ttu-id="18ace-1276">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="18ace-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="18ace-1278">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="18ace-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="18ace-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="18ace-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="18ace-1280">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="18ace-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="18ace-1281">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="18ace-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="18ace-1282">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="18ace-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="18ace-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="18ace-1284">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="18ace-1285">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="18ace-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="18ace-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1286">Az.Resources</span></span>

* <span data-ttu-id="18ace-1287">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="18ace-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="18ace-1288">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="18ace-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="18ace-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1289">Az.Sql</span></span>

* <span data-ttu-id="18ace-1290">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="18ace-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="18ace-1291">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="18ace-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="18ace-1292">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="18ace-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="18ace-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1293">Az.Storage</span></span>

* <span data-ttu-id="18ace-1294">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="18ace-1295">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="18ace-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="18ace-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="18ace-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="18ace-1297">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="18ace-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="18ace-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="18ace-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="18ace-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="18ace-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="18ace-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1300">Az.Websites</span></span>

* <span data-ttu-id="18ace-1301">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18ace-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="18ace-1302">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="18ace-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="18ace-1303">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="18ace-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="18ace-1304">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="18ace-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="18ace-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="18ace-1306">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="18ace-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="18ace-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="18ace-1307">Az.Automation</span></span>
* <span data-ttu-id="18ace-1308">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="18ace-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="18ace-1309">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="18ace-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="18ace-1310">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="18ace-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="18ace-1311">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="18ace-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="18ace-1312">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="18ace-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="18ace-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1313">Az.Compute</span></span>
* <span data-ttu-id="18ace-1314">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="18ace-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="18ace-1315">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="18ace-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="18ace-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="18ace-1317">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="18ace-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="18ace-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="18ace-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="18ace-1319">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="18ace-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="18ace-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1320">Az.Network</span></span>
* <span data-ttu-id="18ace-1321">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="18ace-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="18ace-1322">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="18ace-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="18ace-1323">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="18ace-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="18ace-1324">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="18ace-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="18ace-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="18ace-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="18ace-1326">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="18ace-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="18ace-1327">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="18ace-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="18ace-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="18ace-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="18ace-1329">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="18ace-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="18ace-1330">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="18ace-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="18ace-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="18ace-1331">Az.Relay</span></span>
* <span data-ttu-id="18ace-1332">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="18ace-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="18ace-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1333">Az.Resources</span></span>
* <span data-ttu-id="18ace-1334">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="18ace-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="18ace-1335">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="18ace-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="18ace-1336">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="18ace-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="18ace-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-1338">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="18ace-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="18ace-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1339">Az.Sql</span></span>
* <span data-ttu-id="18ace-1340">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="18ace-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="18ace-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="18ace-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="18ace-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="18ace-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="18ace-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="18ace-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="18ace-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="18ace-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="18ace-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="18ace-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="18ace-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="18ace-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="18ace-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="18ace-1349">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="18ace-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="18ace-1350">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="18ace-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="18ace-1351">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="18ace-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="18ace-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="18ace-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="18ace-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="18ace-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="18ace-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="18ace-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="18ace-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="18ace-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="18ace-1356">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="18ace-1357">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="18ace-1358">Generale</span><span class="sxs-lookup"><span data-stu-id="18ace-1358">General</span></span>
* <span data-ttu-id="18ace-1359">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="18ace-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="18ace-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="18ace-1360">Az.Profile</span></span>
* <span data-ttu-id="18ace-1361">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="18ace-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="18ace-1362">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="18ace-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="18ace-1363">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="18ace-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="18ace-1364">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="18ace-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="18ace-1365">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="18ace-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="18ace-1366">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="18ace-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="18ace-1367">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="18ace-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-1369">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="18ace-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1370">Az.Compute</span></span>
* <span data-ttu-id="18ace-1371">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="18ace-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="18ace-1372">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="18ace-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="18ace-1373">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="18ace-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-1375">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="18ace-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="18ace-1376">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="18ace-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="18ace-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="18ace-1377">Az.Insights</span></span>
* <span data-ttu-id="18ace-1378">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="18ace-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="18ace-1379">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="18ace-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="18ace-1380">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="18ace-1381">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="18ace-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1382">Az.Network</span></span>
* <span data-ttu-id="18ace-1383">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="18ace-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="18ace-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="18ace-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="18ace-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="18ace-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="18ace-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="18ace-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="18ace-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="18ace-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="18ace-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="18ace-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="18ace-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="18ace-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="18ace-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="18ace-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="18ace-1391">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="18ace-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1392">Az.Resources</span></span>
* <span data-ttu-id="18ace-1393">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="18ace-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="18ace-1394">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="18ace-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="18ace-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="18ace-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="18ace-1396">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="18ace-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="18ace-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="18ace-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="18ace-1398">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="18ace-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="18ace-1399">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="18ace-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="18ace-1400">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="18ace-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="18ace-1401">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="18ace-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="18ace-1402">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="18ace-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="18ace-1403">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="18ace-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="18ace-1404">Az.Profile</span></span>
* <span data-ttu-id="18ace-1405">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="18ace-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="18ace-1406">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="18ace-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1407">Az.Compute</span></span>
* <span data-ttu-id="18ace-1408">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="18ace-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="18ace-1409">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ace-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="18ace-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18ace-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="18ace-1411">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="18ace-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="18ace-1412">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18ace-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="18ace-1413">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="18ace-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="18ace-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="18ace-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="18ace-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18ace-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1416">Az.Network</span></span>
* <span data-ttu-id="18ace-1417">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="18ace-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="18ace-1418">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ace-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1419">Az.Resources</span></span>
* <span data-ttu-id="18ace-1420">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="18ace-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="18ace-1421">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="18ace-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="18ace-1422">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="18ace-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="18ace-1423">Azure.Storage</span></span>
* <span data-ttu-id="18ace-1424">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="18ace-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="18ace-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="18ace-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="18ace-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="18ace-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="18ace-1427">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="18ace-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="18ace-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="18ace-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="18ace-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="18ace-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="18ace-1430">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="18ace-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="18ace-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="18ace-1431">Az.Compute</span></span>
* <span data-ttu-id="18ace-1432">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="18ace-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="18ace-1433">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="18ace-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="18ace-1434">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="18ace-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="18ace-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="18ace-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="18ace-1436">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="18ace-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="18ace-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="18ace-1437">Az.Network</span></span>
* <span data-ttu-id="18ace-1438">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="18ace-1439">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="18ace-1439">new cmdlets added</span></span>
    - <span data-ttu-id="18ace-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="18ace-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="18ace-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="18ace-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="18ace-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="18ace-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="18ace-1446">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="18ace-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="18ace-1447">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="18ace-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="18ace-1448">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="18ace-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="18ace-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="18ace-1449">Az.RedisCache</span></span>
* <span data-ttu-id="18ace-1450">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="18ace-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="18ace-1451">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="18ace-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="18ace-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="18ace-1452">Az.Resources</span></span>
* <span data-ttu-id="18ace-1453">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18ace-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="18ace-1454">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="18ace-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="18ace-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="18ace-1455">Az.Sql</span></span>
* <span data-ttu-id="18ace-1456">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="18ace-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="18ace-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="18ace-1457">Az.Websites</span></span>
* <span data-ttu-id="18ace-1458">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="18ace-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="18ace-1459">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="18ace-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="18ace-1460">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="18ace-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="18ace-1461">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="18ace-1461">Initial Release</span></span>