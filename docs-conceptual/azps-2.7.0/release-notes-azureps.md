---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319320"
---
## <a name="270---september-2019"></a><span data-ttu-id="ca34c-103">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ca34c-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-104">Az.ApiManagement</span></span>
* <span data-ttu-id="ca34c-105">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="ca34c-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ca34c-106">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="ca34c-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ca34c-107">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-108">Az.Automation</span></span>
* <span data-ttu-id="ca34c-109">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="ca34c-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ca34c-110">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ca34c-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ca34c-111">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="ca34c-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-112">Az.Compute</span></span>
* <span data-ttu-id="ca34c-113">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ca34c-114">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ca34c-115">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="ca34c-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ca34c-116">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ca34c-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ca34c-117">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ca34c-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ca34c-118">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ca34c-119">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ca34c-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ca34c-120">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="ca34c-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ca34c-121">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ca34c-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-122">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-123">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ca34c-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ca34c-124">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ca34c-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ca34c-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca34c-125">Az.HDInsight</span></span>
* <span data-ttu-id="ca34c-126">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ca34c-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca34c-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-127">Az.IotHub</span></span>
* <span data-ttu-id="ca34c-128">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="ca34c-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ca34c-129">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ca34c-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ca34c-130">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="ca34c-130">New cmdlets are:</span></span>
    - <span data-ttu-id="ca34c-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca34c-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca34c-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca34c-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca34c-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca34c-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca34c-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca34c-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-135">Az.Monitor</span></span>
* <span data-ttu-id="ca34c-136">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="ca34c-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ca34c-137">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="ca34c-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ca34c-138">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="ca34c-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ca34c-139">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ca34c-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ca34c-140">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="ca34c-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ca34c-141">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ca34c-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ca34c-142">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ca34c-143">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="ca34c-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ca34c-144">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ca34c-145">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ca34c-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ca34c-146">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ca34c-147">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ca34c-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ca34c-148">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="ca34c-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ca34c-149">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ca34c-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ca34c-150">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ca34c-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ca34c-151">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="ca34c-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ca34c-152">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="ca34c-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ca34c-153">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ca34c-154">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="ca34c-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ca34c-155">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-155">Overall improved help files</span></span>
* <span data-ttu-id="ca34c-156">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="ca34c-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-157">Az.Network</span></span>
* <span data-ttu-id="ca34c-158">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="ca34c-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="ca34c-159">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="ca34c-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ca34c-160">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="ca34c-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ca34c-161">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="ca34c-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ca34c-162">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="ca34c-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ca34c-163">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ca34c-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ca34c-164">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="ca34c-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ca34c-165">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ca34c-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ca34c-166">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ca34c-167">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ca34c-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ca34c-168">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ca34c-169">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="ca34c-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ca34c-170">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-170">New cmdlets</span></span>
        - <span data-ttu-id="ca34c-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ca34c-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ca34c-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ca34c-173">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ca34c-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca34c-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ca34c-174">New-VpnSite</span></span>
        - <span data-ttu-id="ca34c-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ca34c-175">Update-VpnSite</span></span>
        - <span data-ttu-id="ca34c-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-176">New-VpnConnection</span></span>
        - <span data-ttu-id="ca34c-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-177">Update-VpnConnection</span></span>
* <span data-ttu-id="ca34c-178">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="ca34c-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-180">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="ca34c-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ca34c-181">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="ca34c-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-182">Az.Resources</span></span>
* <span data-ttu-id="ca34c-183">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="ca34c-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-185">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ca34c-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ca34c-186">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="ca34c-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ca34c-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca34c-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca34c-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca34c-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca34c-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca34c-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca34c-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ca34c-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ca34c-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca34c-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca34c-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca34c-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca34c-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca34c-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca34c-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca34c-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca34c-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ca34c-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ca34c-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca34c-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca34c-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca34c-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca34c-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca34c-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca34c-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ca34c-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ca34c-200">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ca34c-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca34c-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca34c-201">Az.SignalR</span></span>
* <span data-ttu-id="ca34c-202">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="ca34c-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-203">Az.Sql</span></span>
* <span data-ttu-id="ca34c-204">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="ca34c-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ca34c-205">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="ca34c-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ca34c-206">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ca34c-207">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="ca34c-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ca34c-208">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ca34c-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-209">Az.Storage</span></span>
* <span data-ttu-id="ca34c-210">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ca34c-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ca34c-211">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ca34c-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ca34c-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ca34c-214">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="ca34c-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ca34c-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ca34c-216">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ca34c-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ca34c-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca34c-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca34c-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca34c-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca34c-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca34c-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca34c-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca34c-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-221">Az.Websites</span></span>
* <span data-ttu-id="ca34c-222">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="ca34c-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ca34c-223">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="ca34c-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ca34c-224">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="ca34c-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ca34c-225">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ca34c-226">Generale</span><span class="sxs-lookup"><span data-stu-id="ca34c-226">General</span></span>
* <span data-ttu-id="ca34c-227">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="ca34c-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca34c-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-228">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-229">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="ca34c-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ca34c-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ca34c-230">Az.Aks</span></span>
* <span data-ttu-id="ca34c-231">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="ca34c-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ca34c-232">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ca34c-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca34c-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-233">Az.ApiManagement</span></span>
* <span data-ttu-id="ca34c-234">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ca34c-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ca34c-235">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="ca34c-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ca34c-236">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="ca34c-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ca34c-237">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ca34c-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ca34c-238">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ca34c-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca34c-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-239">Az.Batch</span></span>
* <span data-ttu-id="ca34c-240">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ca34c-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca34c-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca34c-241">Az.Cdn</span></span>
* <span data-ttu-id="ca34c-242">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="ca34c-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-243">Az.Compute</span></span>
* <span data-ttu-id="ca34c-244">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ca34c-245">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca34c-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ca34c-246">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ca34c-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ca34c-247">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ca34c-248">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ca34c-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ca34c-249">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ca34c-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ca34c-250">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ca34c-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ca34c-251">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="ca34c-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-252">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-253">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ca34c-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ca34c-254">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ca34c-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ca34c-255">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ca34c-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ca34c-256">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="ca34c-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-258">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="ca34c-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca34c-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-259">Az.EventHub</span></span>
* <span data-ttu-id="ca34c-260">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ca34c-261">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ca34c-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ca34c-262">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ca34c-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ca34c-263">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ca34c-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ca34c-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ca34c-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ca34c-265">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="ca34c-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-266">Az.Monitor</span></span>
* <span data-ttu-id="ca34c-267">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-268">Az.Network</span></span>
* <span data-ttu-id="ca34c-269">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ca34c-270">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="ca34c-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ca34c-271">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="ca34c-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ca34c-272">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="ca34c-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ca34c-273">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="ca34c-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="ca34c-274">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ca34c-275">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ca34c-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-277">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="ca34c-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ca34c-278">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca34c-278">Added example</span></span>
    - <span data-ttu-id="ca34c-279">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="ca34c-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ca34c-280">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ca34c-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ca34c-281">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ca34c-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-283">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-284">Az.Resources</span></span>
* <span data-ttu-id="ca34c-285">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ca34c-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ca34c-286">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="ca34c-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ca34c-287">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="ca34c-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ca34c-288">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-289">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-290">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ca34c-291">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ca34c-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ca34c-292">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="ca34c-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-294">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="ca34c-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ca34c-295">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ca34c-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ca34c-296">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ca34c-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ca34c-297">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="ca34c-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ca34c-298">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ca34c-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ca34c-299">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ca34c-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-300">Az.Sql</span></span>
* <span data-ttu-id="ca34c-301">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-302">Az.Storage</span></span>
* <span data-ttu-id="ca34c-303">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ca34c-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ca34c-304">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ca34c-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ca34c-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ca34c-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca34c-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ca34c-307">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ca34c-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ca34c-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca34c-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-309">Az.Websites</span></span>
* <span data-ttu-id="ca34c-310">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ca34c-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ca34c-311">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-312">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-313">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca34c-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ca34c-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ca34c-315">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="ca34c-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="ca34c-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-316">Az.Automation</span></span>
* <span data-ttu-id="ca34c-317">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="ca34c-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-319">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-320">Az.Compute</span></span>
* <span data-ttu-id="ca34c-321">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca34c-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ca34c-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca34c-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ca34c-323">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="ca34c-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ca34c-324">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ca34c-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-325">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-326">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ca34c-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ca34c-327">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="ca34c-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca34c-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-328">Az.EventHub</span></span>
* <span data-ttu-id="ca34c-329">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ca34c-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ca34c-330">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ca34c-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca34c-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-331">Az.KeyVault</span></span>
* <span data-ttu-id="ca34c-332">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="ca34c-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca34c-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-333">Az.LogicApp</span></span>
* <span data-ttu-id="ca34c-334">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="ca34c-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ca34c-335">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="ca34c-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ca34c-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-336">Az.ManagedServices</span></span>
* <span data-ttu-id="ca34c-337">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="ca34c-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-338">Az.Network</span></span>
* <span data-ttu-id="ca34c-339">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="ca34c-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ca34c-340">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-340">New cmdlets</span></span>
        - <span data-ttu-id="ca34c-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca34c-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca34c-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca34c-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca34c-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca34c-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca34c-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca34c-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ca34c-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ca34c-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ca34c-349">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="ca34c-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ca34c-350">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ca34c-351">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ca34c-352">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ca34c-353">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="ca34c-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ca34c-354">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="ca34c-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ca34c-355">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-355">Updated cmdlets</span></span>
        - <span data-ttu-id="ca34c-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca34c-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca34c-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ca34c-359">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ca34c-360">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ca34c-361">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ca34c-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca34c-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ca34c-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ca34c-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ca34c-365">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="ca34c-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ca34c-366">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="ca34c-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ca34c-367">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="ca34c-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-369">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="ca34c-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="ca34c-370">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="ca34c-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-372">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ca34c-373">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ca34c-374">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ca34c-375">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ca34c-376">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ca34c-377">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ca34c-378">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ca34c-379">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ca34c-380">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ca34c-381">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ca34c-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-382">Az.Resources</span></span>
- <span data-ttu-id="ca34c-383">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ca34c-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ca34c-384">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ca34c-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-385">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-386">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ca34c-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ca34c-387">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ca34c-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-388">Az.Sql</span></span>
* <span data-ttu-id="ca34c-389">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ca34c-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ca34c-390">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="ca34c-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ca34c-391">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="ca34c-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-392">Az.Storage</span></span>
* <span data-ttu-id="ca34c-393">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ca34c-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ca34c-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ca34c-394">Az.StorageSync</span></span>
* <span data-ttu-id="ca34c-395">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ca34c-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ca34c-396">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ca34c-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-397">Az.Websites</span></span>
* <span data-ttu-id="ca34c-398">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ca34c-399">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ca34c-400">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ca34c-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ca34c-401">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-402">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-403">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="ca34c-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ca34c-404">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="ca34c-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ca34c-405">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca34c-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ca34c-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ca34c-406">Az.Advisor</span></span>
* <span data-ttu-id="ca34c-407">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ca34c-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ca34c-408">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ca34c-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca34c-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-409">Az.ApiManagement</span></span>
* <span data-ttu-id="ca34c-410">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ca34c-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ca34c-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca34c-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ca34c-412">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="ca34c-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ca34c-413">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="ca34c-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ca34c-414">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ca34c-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ca34c-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca34c-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ca34c-416">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="ca34c-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-417">Az.Automation</span></span>
* <span data-ttu-id="ca34c-418">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="ca34c-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-419">Az.Compute</span></span>
* <span data-ttu-id="ca34c-420">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-421">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-422">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="ca34c-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca34c-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca34c-423">Az.EventGrid</span></span>
* <span data-ttu-id="ca34c-424">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="ca34c-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca34c-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-425">Az.IotHub</span></span>
* <span data-ttu-id="ca34c-426">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-427">Az.Network</span></span>
* <span data-ttu-id="ca34c-428">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="ca34c-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ca34c-429">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="ca34c-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca34c-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca34c-431">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ca34c-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ca34c-432">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ca34c-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-434">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ca34c-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-436">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="ca34c-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-437">Az.Resources</span></span>
    - <span data-ttu-id="ca34c-438">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="ca34c-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ca34c-439">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ca34c-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ca34c-440">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ca34c-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ca34c-441">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="ca34c-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-442">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-443">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ca34c-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-444">Az.Sql</span></span>
* <span data-ttu-id="ca34c-445">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="ca34c-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ca34c-446">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ca34c-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca34c-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca34c-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca34c-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ca34c-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ca34c-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca34c-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ca34c-453">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="ca34c-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-454">Az.Storage</span></span>
* <span data-ttu-id="ca34c-455">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ca34c-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca34c-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ca34c-457">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="ca34c-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ca34c-458">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="ca34c-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ca34c-459">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ca34c-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ca34c-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ca34c-462">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="ca34c-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ca34c-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca34c-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ca34c-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca34c-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ca34c-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ca34c-465">Az.StorageSync</span></span>
* <span data-ttu-id="ca34c-466">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ca34c-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ca34c-467">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-468">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-469">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="ca34c-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ca34c-470">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ca34c-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ca34c-471">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="ca34c-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ca34c-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ca34c-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ca34c-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ca34c-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-474">Az.Compute</span></span>
* <span data-ttu-id="ca34c-475">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ca34c-476">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="ca34c-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ca34c-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ca34c-477">Az.Dns</span></span>
* <span data-ttu-id="ca34c-478">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca34c-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca34c-479">Az.EventGrid</span></span>
* <span data-ttu-id="ca34c-480">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ca34c-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ca34c-481">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-481">New cmdlets:</span></span>
    - <span data-ttu-id="ca34c-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca34c-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca34c-483">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca34c-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca34c-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca34c-485">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ca34c-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca34c-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca34c-487">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca34c-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ca34c-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ca34c-489">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca34c-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ca34c-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ca34c-491">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="ca34c-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ca34c-492">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ca34c-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ca34c-493">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ca34c-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ca34c-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ca34c-495">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="ca34c-496">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ca34c-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ca34c-497">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ca34c-498">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="ca34c-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ca34c-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ca34c-500">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ca34c-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ca34c-501">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ca34c-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ca34c-502">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="ca34c-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ca34c-503">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ca34c-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ca34c-504">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="ca34c-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ca34c-505">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ca34c-506">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ca34c-507">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="ca34c-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ca34c-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ca34c-509">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ca34c-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ca34c-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ca34c-511">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ca34c-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ca34c-512">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ca34c-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca34c-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca34c-513">Az.FrontDoor</span></span>
* <span data-ttu-id="ca34c-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ca34c-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ca34c-515">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ca34c-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ca34c-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ca34c-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ca34c-517">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="ca34c-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-518">Az.Network</span></span>
* <span data-ttu-id="ca34c-519">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ca34c-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ca34c-520">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-520">New cmdlets</span></span>
        - <span data-ttu-id="ca34c-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ca34c-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ca34c-522">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ca34c-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ca34c-523">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-523">New cmdlets</span></span> 
        - <span data-ttu-id="ca34c-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ca34c-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ca34c-525">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ca34c-526">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-526">New cmdlets</span></span> 
        - <span data-ttu-id="ca34c-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="ca34c-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca34c-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca34c-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca34c-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ca34c-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ca34c-532">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca34c-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ca34c-533">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-533">New cmdlets</span></span>
        - <span data-ttu-id="ca34c-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca34c-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca34c-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca34c-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca34c-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca34c-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca34c-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ca34c-538">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ca34c-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ca34c-539">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ca34c-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ca34c-540">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ca34c-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ca34c-541">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ca34c-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ca34c-542">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ca34c-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ca34c-543">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca34c-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ca34c-544">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ca34c-545">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="ca34c-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ca34c-546">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ca34c-547">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="ca34c-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ca34c-548">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ca34c-549">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ca34c-550">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ca34c-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ca34c-551">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ca34c-552">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="ca34c-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ca34c-553">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ca34c-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ca34c-554">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ca34c-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ca34c-555">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ca34c-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ca34c-556">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ca34c-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="ca34c-557">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca34c-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="ca34c-558">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ca34c-559">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ca34c-560">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-562">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ca34c-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-563">Az.Resources</span></span>
* <span data-ttu-id="ca34c-564">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="ca34c-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ca34c-565">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ca34c-566">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ca34c-567">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="ca34c-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-569">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="ca34c-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-570">Az.Sql</span></span>
* <span data-ttu-id="ca34c-571">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ca34c-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ca34c-572">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ca34c-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ca34c-573">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="ca34c-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ca34c-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca34c-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca34c-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca34c-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca34c-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca34c-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca34c-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ca34c-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ca34c-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ca34c-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-579">Az.Storage</span></span>
* <span data-ttu-id="ca34c-580">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ca34c-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="ca34c-582">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="ca34c-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ca34c-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-584">Az.Websites</span></span>
* <span data-ttu-id="ca34c-585">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="ca34c-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ca34c-586">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ca34c-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ca34c-587">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ca34c-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca34c-588">Az.Cdn</span></span>
* <span data-ttu-id="ca34c-589">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="ca34c-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-590">Az.Compute</span></span>
* <span data-ttu-id="ca34c-591">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ca34c-592">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ca34c-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca34c-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-593">Az.EventHub</span></span>
* <span data-ttu-id="ca34c-594">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="ca34c-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ca34c-595">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca34c-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-596">Az.Network</span></span>
* <span data-ttu-id="ca34c-597">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ca34c-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ca34c-598">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="ca34c-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca34c-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca34c-600">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ca34c-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-602">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="ca34c-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-603">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-604">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca34c-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-606">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ca34c-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ca34c-607">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-608">Az.Sql</span></span>
* <span data-ttu-id="ca34c-609">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="ca34c-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ca34c-610">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ca34c-611">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ca34c-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ca34c-612">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ca34c-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-613">Az.Websites</span></span>
* <span data-ttu-id="ca34c-614">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="ca34c-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ca34c-615">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ca34c-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-616">Az.ApiManagement</span></span>
* <span data-ttu-id="ca34c-617">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="ca34c-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ca34c-618">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ca34c-619">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ca34c-620">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="ca34c-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ca34c-621">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ca34c-622">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="ca34c-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ca34c-623">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ca34c-624">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ca34c-625">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ca34c-626">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="ca34c-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ca34c-627">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ca34c-628">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="ca34c-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ca34c-629">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="ca34c-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ca34c-630">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ca34c-631">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ca34c-632">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ca34c-633">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ca34c-634">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ca34c-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ca34c-635">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="ca34c-636">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ca34c-637">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="ca34c-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ca34c-638">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ca34c-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ca34c-639">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="ca34c-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ca34c-640">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="ca34c-641">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ca34c-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ca34c-642">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ca34c-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ca34c-643">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ca34c-644">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ca34c-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ca34c-645">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ca34c-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ca34c-646">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="ca34c-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ca34c-647">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="ca34c-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="ca34c-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ca34c-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ca34c-649">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ca34c-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ca34c-650">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca34c-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ca34c-651">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ca34c-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ca34c-652">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="ca34c-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ca34c-653">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="ca34c-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ca34c-654">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="ca34c-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ca34c-655">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="ca34c-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ca34c-656">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca34c-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="ca34c-657">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ca34c-658">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca34c-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ca34c-659">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ca34c-660">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ca34c-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ca34c-661">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca34c-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ca34c-662">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ca34c-663">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca34c-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="ca34c-664">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ca34c-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ca34c-665">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ca34c-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ca34c-666">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ca34c-667">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ca34c-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ca34c-668">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ca34c-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ca34c-669">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="ca34c-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ca34c-670">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ca34c-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ca34c-671">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="ca34c-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ca34c-672">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ca34c-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ca34c-673">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca34c-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ca34c-674">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ca34c-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ca34c-675">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ca34c-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ca34c-676">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ca34c-677">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca34c-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ca34c-678">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ca34c-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ca34c-679">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ca34c-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ca34c-680">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ca34c-681">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="ca34c-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ca34c-682">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ca34c-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ca34c-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ca34c-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ca34c-684">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ca34c-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ca34c-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ca34c-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ca34c-686">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca34c-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ca34c-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ca34c-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ca34c-688">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ca34c-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ca34c-689">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ca34c-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ca34c-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ca34c-691">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ca34c-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="ca34c-692">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca34c-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ca34c-693">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ca34c-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-694">Az.Automation</span></span>
* <span data-ttu-id="ca34c-695">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="ca34c-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ca34c-696">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ca34c-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ca34c-697">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ca34c-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ca34c-698">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="ca34c-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ca34c-699">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ca34c-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ca34c-700">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="ca34c-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ca34c-701">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-702">Az.Compute</span></span>
* <span data-ttu-id="ca34c-703">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ca34c-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ca34c-704">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="ca34c-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-706">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-707">Az.Monitor</span></span>
* <span data-ttu-id="ca34c-708">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-709">Az.Network</span></span>
* <span data-ttu-id="ca34c-710">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="ca34c-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ca34c-711">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ca34c-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca34c-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca34c-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ca34c-713">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ca34c-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-714">Az.Resources</span></span>
* <span data-ttu-id="ca34c-715">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="ca34c-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-716">Az.Sql</span></span>
* <span data-ttu-id="ca34c-717">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ca34c-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ca34c-718">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-719">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-720">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="ca34c-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-722">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ca34c-723">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="ca34c-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-724">Az.Compute</span></span>
* <span data-ttu-id="ca34c-725">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="ca34c-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ca34c-726">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ca34c-727">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ca34c-728">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ca34c-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ca34c-729">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ca34c-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ca34c-730">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca34c-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="ca34c-731">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ca34c-731">Breaking changes</span></span>
    - <span data-ttu-id="ca34c-732">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ca34c-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ca34c-733">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ca34c-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ca34c-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ca34c-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="ca34c-735">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="ca34c-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ca34c-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ca34c-736">Az.Dns</span></span>
* <span data-ttu-id="ca34c-737">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="ca34c-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ca34c-738">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="ca34c-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ca34c-739">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="ca34c-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca34c-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca34c-740">Az.FrontDoor</span></span>
* <span data-ttu-id="ca34c-741">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ca34c-742">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ca34c-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ca34c-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca34c-743">Az.HDInsight</span></span>
* <span data-ttu-id="ca34c-744">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ca34c-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca34c-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ca34c-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca34c-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ca34c-747">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca34c-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ca34c-748">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="ca34c-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ca34c-749">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ca34c-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ca34c-750">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-751">Az.Monitor</span></span>
* <span data-ttu-id="ca34c-752">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="ca34c-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="ca34c-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ca34c-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ca34c-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ca34c-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ca34c-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ca34c-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ca34c-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ca34c-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ca34c-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ca34c-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ca34c-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ca34c-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca34c-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca34c-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca34c-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca34c-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca34c-764">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="ca34c-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ca34c-765">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ca34c-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-766">Az.Network</span></span>
* <span data-ttu-id="ca34c-767">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ca34c-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ca34c-768">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-768">New cmdlets</span></span>
        - <span data-ttu-id="ca34c-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="ca34c-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ca34c-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ca34c-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ca34c-773">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ca34c-773">Updated cmdlets</span></span>
        - <span data-ttu-id="ca34c-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ca34c-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ca34c-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ca34c-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ca34c-776">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ca34c-777">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ca34c-778">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ca34c-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca34c-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca34c-780">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ca34c-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ca34c-781">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ca34c-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ca34c-782">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-784">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="ca34c-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ca34c-785">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ca34c-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ca34c-786">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ca34c-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ca34c-787">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ca34c-788">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="ca34c-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ca34c-789">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="ca34c-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ca34c-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ca34c-790">Az.Relay</span></span>
* <span data-ttu-id="ca34c-791">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="ca34c-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-792">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-793">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca34c-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-794">Az.Storage</span></span>
* <span data-ttu-id="ca34c-795">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ca34c-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ca34c-796">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ca34c-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ca34c-797">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ca34c-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ca34c-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="ca34c-799">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ca34c-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ca34c-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ca34c-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ca34c-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-803">Az.Websites</span></span>
* <span data-ttu-id="ca34c-804">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ca34c-805">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="ca34c-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ca34c-806">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca34c-807">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ca34c-807">Highlights since the last major release</span></span>
* <span data-ttu-id="ca34c-808">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ca34c-808">General availability of `Az` module</span></span>
* <span data-ttu-id="ca34c-809">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca34c-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca34c-810">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca34c-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca34c-811">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca34c-812">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ca34c-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca34c-813">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca34c-814">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca34c-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-815">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-816">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="ca34c-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca34c-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-817">Az.Batch</span></span>
* <span data-ttu-id="ca34c-818">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca34c-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca34c-819">Az.Cdn</span></span>
* <span data-ttu-id="ca34c-820">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-822">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-823">Az.Compute</span></span>
* <span data-ttu-id="ca34c-824">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="ca34c-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ca34c-825">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-826">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ca34c-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-827">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-828">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="ca34c-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-830">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca34c-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca34c-831">Az.EventGrid</span></span>
* <span data-ttu-id="ca34c-832">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ca34c-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca34c-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-833">Az.EventHub</span></span>
* <span data-ttu-id="ca34c-834">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca34c-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="ca34c-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca34c-835">Az.HDInsight</span></span>
* <span data-ttu-id="ca34c-836">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca34c-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-837">Az.IotHub</span></span>
* <span data-ttu-id="ca34c-838">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca34c-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-839">Az.KeyVault</span></span>
* <span data-ttu-id="ca34c-840">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-841">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ca34c-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ca34c-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca34c-842">Az.MachineLearning</span></span>
* <span data-ttu-id="ca34c-843">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ca34c-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ca34c-844">Az.Media</span></span>
* <span data-ttu-id="ca34c-845">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-846">Az.Monitor</span></span>
  * <span data-ttu-id="ca34c-847">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ca34c-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ca34c-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ca34c-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ca34c-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ca34c-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ca34c-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca34c-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ca34c-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca34c-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ca34c-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca34c-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ca34c-853">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ca34c-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-854">Az.Network</span></span>
* <span data-ttu-id="ca34c-855">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-856">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ca34c-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ca34c-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ca34c-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="ca34c-858">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-860">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ca34c-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ca34c-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ca34c-862">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-864">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-865">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ca34c-866">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ca34c-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ca34c-867">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="ca34c-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca34c-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca34c-868">Az.RedisCache</span></span>
* <span data-ttu-id="ca34c-869">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-870">Az.Resources</span></span>
* <span data-ttu-id="ca34c-871">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ca34c-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-872">Az.Sql</span></span>
* <span data-ttu-id="ca34c-873">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="ca34c-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ca34c-874">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-875">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="ca34c-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ca34c-876">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ca34c-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ca34c-877">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="ca34c-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ca34c-878">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="ca34c-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ca34c-879">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ca34c-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-880">Az.Websites</span></span>
* <span data-ttu-id="ca34c-881">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="ca34c-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ca34c-882">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ca34c-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca34c-883">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="ca34c-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ca34c-884">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ca34c-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ca34c-885">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca34c-886">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ca34c-886">Highlights since the last major release</span></span>
* <span data-ttu-id="ca34c-887">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ca34c-887">General availability of `Az` module</span></span>
* <span data-ttu-id="ca34c-888">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca34c-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca34c-889">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca34c-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca34c-890">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca34c-891">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ca34c-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca34c-892">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca34c-893">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca34c-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-894">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-895">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ca34c-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca34c-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca34c-897">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="ca34c-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ca34c-898">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ca34c-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-899">Az.Automation</span></span>
* <span data-ttu-id="ca34c-900">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="ca34c-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ca34c-901">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="ca34c-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ca34c-902">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-903">Az.Compute</span></span>
* <span data-ttu-id="ca34c-904">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ca34c-905">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="ca34c-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ca34c-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="ca34c-907">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="ca34c-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-908">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-909">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ca34c-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ca34c-910">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ca34c-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-911">Az.Resources</span></span>
* <span data-ttu-id="ca34c-912">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="ca34c-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ca34c-913">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ca34c-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ca34c-914">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="ca34c-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ca34c-915">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ca34c-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ca34c-916">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="ca34c-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ca34c-917">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ca34c-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-918">Az.Sql</span></span>
* <span data-ttu-id="ca34c-919">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="ca34c-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-920">Az.Storage</span></span>
* <span data-ttu-id="ca34c-921">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="ca34c-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ca34c-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca34c-922">New-AzStorageContext</span></span>
* <span data-ttu-id="ca34c-923">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ca34c-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ca34c-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ca34c-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ca34c-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ca34c-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ca34c-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ca34c-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ca34c-928">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="ca34c-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ca34c-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ca34c-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ca34c-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ca34c-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca34c-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ca34c-933">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca34c-934">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ca34c-934">Highlights since the last major release</span></span>
* <span data-ttu-id="ca34c-935">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ca34c-935">General availability of `Az` module</span></span>
* <span data-ttu-id="ca34c-936">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca34c-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca34c-937">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca34c-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca34c-938">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca34c-939">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ca34c-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca34c-940">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca34c-941">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-942">Az.Automation</span></span>
* <span data-ttu-id="ca34c-943">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca34c-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ca34c-944">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="ca34c-944">Dynamic grouping</span></span>
    * <span data-ttu-id="ca34c-945">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="ca34c-945">Pre-Post script</span></span>
    * <span data-ttu-id="ca34c-946">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="ca34c-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-947">Az.Compute</span></span>
* <span data-ttu-id="ca34c-948">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ca34c-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ca34c-949">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ca34c-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca34c-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-950">Az.KeyVault</span></span>
* <span data-ttu-id="ca34c-951">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-952">Az.Network</span></span>
* <span data-ttu-id="ca34c-953">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ca34c-954">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="ca34c-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-956">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="ca34c-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ca34c-957">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="ca34c-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-958">Az.Resources</span></span>
* <span data-ttu-id="ca34c-959">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ca34c-960">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="ca34c-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-961">Az.Sql</span></span>
* <span data-ttu-id="ca34c-962">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ca34c-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-963">Az.Storage</span></span>
* <span data-ttu-id="ca34c-964">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ca34c-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca34c-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca34c-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca34c-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ca34c-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ca34c-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ca34c-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ca34c-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-971">Az.Websites</span></span>
* <span data-ttu-id="ca34c-972">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="ca34c-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ca34c-973">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-974">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-975">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="ca34c-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ca34c-976">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-977">Az.Automation</span></span>
* <span data-ttu-id="ca34c-978">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ca34c-979">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="ca34c-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ca34c-980">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="ca34c-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca34c-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca34c-981">Az.Cdn</span></span>
* <span data-ttu-id="ca34c-982">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="ca34c-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-983">Az.Compute</span></span>
* <span data-ttu-id="ca34c-984">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="ca34c-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-985">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-986">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ca34c-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca34c-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-987">Az.LogicApp</span></span>
* <span data-ttu-id="ca34c-988">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="ca34c-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-989">Az.Network</span></span>
* <span data-ttu-id="ca34c-990">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-992">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ca34c-993">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="ca34c-993">SDK Update</span></span>
* <span data-ttu-id="ca34c-994">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ca34c-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ca34c-995">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ca34c-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-996">Az.Resources</span></span>
* <span data-ttu-id="ca34c-997">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="ca34c-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ca34c-998">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ca34c-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ca34c-999">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ca34c-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ca34c-1000">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ca34c-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ca34c-1001">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ca34c-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ca34c-1002">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ca34c-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1003">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1004">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ca34c-1005">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1006">Az.Storage</span></span>
* <span data-ttu-id="ca34c-1007">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ca34c-1008">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ca34c-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca34c-1010">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="ca34c-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-1011">Az.Automation</span></span>
* <span data-ttu-id="ca34c-1012">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ca34c-1013">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ca34c-1014">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-1016">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1017">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1018">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="ca34c-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ca34c-1019">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="ca34c-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ca34c-1020">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ca34c-1021">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-1023">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="ca34c-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca34c-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-1024">Az.EventHub</span></span>
* <span data-ttu-id="ca34c-1025">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="ca34c-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ca34c-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-1026">Az.KeyVault</span></span>
* <span data-ttu-id="ca34c-1027">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ca34c-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca34c-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-1028">Az.LogicApp</span></span>
* <span data-ttu-id="ca34c-1029">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ca34c-1030">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="ca34c-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ca34c-1031">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ca34c-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca34c-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca34c-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca34c-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca34c-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca34c-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca34c-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca34c-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ca34c-1036">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ca34c-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca34c-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca34c-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca34c-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ca34c-1041">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ca34c-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca34c-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-1042">Az.Monitor</span></span>
* <span data-ttu-id="ca34c-1043">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ca34c-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1044">Az.Network</span></span>
* <span data-ttu-id="ca34c-1045">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ca34c-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca34c-1047">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ca34c-1048">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ca34c-1049">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ca34c-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1050">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1051">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ca34c-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ca34c-1052">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ca34c-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ca34c-1053">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ca34c-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ca34c-1054">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ca34c-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1055">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1056">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="ca34c-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ca34c-1057">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="ca34c-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1058">Az.Websites</span></span>
* <span data-ttu-id="ca34c-1059">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ca34c-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ca34c-1060">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1061">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-1062">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca34c-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca34c-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="ca34c-1064">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1065">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1066">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="ca34c-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ca34c-1067">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ca34c-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ca34c-1068">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="ca34c-1070">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1071">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1072">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ca34c-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ca34c-1073">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ca34c-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ca34c-1074">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ca34c-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ca34c-1075">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ca34c-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1076">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1077">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca34c-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ca34c-1078">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="ca34c-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ca34c-1079">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ca34c-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ca34c-1080">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1081">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-1082">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca34c-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca34c-1084">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca34c-1086">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ca34c-1087">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1088">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-1089">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ca34c-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca34c-1090">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca34c-1091">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ca34c-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ca34c-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ca34c-1092">Az.Aks</span></span>
* <span data-ttu-id="ca34c-1093">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca34c-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-1094">Az.Automation</span></span>
* <span data-ttu-id="ca34c-1095">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="ca34c-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ca34c-1096">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca34c-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca34c-1097">Az.Cdn</span></span>
* <span data-ttu-id="ca34c-1098">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1099">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1100">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ca34c-1101">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca34c-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ca34c-1102">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ca34c-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ca34c-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca34c-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ca34c-1104">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca34c-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca34c-1105">Az.DataFactory</span></span>
* <span data-ttu-id="ca34c-1106">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ca34c-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-1108">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ca34c-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ca34c-1109">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ca34c-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ca34c-1110">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca34c-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-1111">Az.IotHub</span></span>
* <span data-ttu-id="ca34c-1112">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca34c-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-1113">Az.KeyVault</span></span>
* <span data-ttu-id="ca34c-1114">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1115">Az.Network</span></span>
* <span data-ttu-id="ca34c-1116">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1117">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1118">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="ca34c-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ca34c-1119">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ca34c-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ca34c-1120">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ca34c-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ca34c-1121">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ca34c-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ca34c-1122">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ca34c-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ca34c-1123">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="ca34c-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ca34c-1124">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ca34c-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-1126">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ca34c-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ca34c-1127">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1127">Fix some error messages.</span></span>
* <span data-ttu-id="ca34c-1128">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ca34c-1129">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca34c-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca34c-1130">Az.SignalR</span></span>
* <span data-ttu-id="ca34c-1131">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1132">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1133">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca34c-1134">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="ca34c-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ca34c-1135">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="ca34c-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ca34c-1136">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ca34c-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1137">Az.Storage</span></span>
* <span data-ttu-id="ca34c-1138">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca34c-1139">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ca34c-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ca34c-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ca34c-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ca34c-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ca34c-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ca34c-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="ca34c-1143">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1144">Az.Websites</span></span>
* <span data-ttu-id="ca34c-1145">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ca34c-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca34c-1146">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ca34c-1147">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="ca34c-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ca34c-1148">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ca34c-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca34c-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1149">Az.Accounts</span></span>
* <span data-ttu-id="ca34c-1150">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ca34c-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1151">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1152">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ca34c-1153">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ca34c-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ca34c-1154">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-1156">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ca34c-1157">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="ca34c-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca34c-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca34c-1158">Az.EventGrid</span></span>
* <span data-ttu-id="ca34c-1159">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ca34c-1160">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ca34c-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ca34c-1161">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ca34c-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ca34c-1162">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ca34c-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ca34c-1163">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ca34c-1164">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ca34c-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ca34c-1165">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ca34c-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ca34c-1166">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ca34c-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ca34c-1167">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ca34c-1168">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ca34c-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="ca34c-1169">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ca34c-1170">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca34c-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-1171">Az.IotHub</span></span>
* <span data-ttu-id="ca34c-1172">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="ca34c-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca34c-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca34c-1173">Az.LogicApp</span></span>
* <span data-ttu-id="ca34c-1174">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="ca34c-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1175">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1176">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ca34c-1177">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ca34c-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ca34c-1178">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ca34c-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ca34c-1179">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ca34c-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ca34c-1180">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ca34c-1181">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ca34c-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca34c-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca34c-1182">Az.SignalR</span></span>
* <span data-ttu-id="ca34c-1183">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1184">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1185">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca34c-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1186">Az.Storage</span></span>
* <span data-ttu-id="ca34c-1187">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="ca34c-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ca34c-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca34c-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="ca34c-1189">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="ca34c-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ca34c-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca34c-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1191">Az.Websites</span></span>
* <span data-ttu-id="ca34c-1192">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ca34c-1193">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ca34c-1194">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ca34c-1195">Generale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1195">General</span></span>

- <span data-ttu-id="ca34c-1196">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="ca34c-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="ca34c-1197">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="ca34c-1197">Online help for each module</span></span>
- <span data-ttu-id="ca34c-1198">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ca34c-1199">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="ca34c-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ca34c-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1200">Az.Accounts</span></span>
- <span data-ttu-id="ca34c-1201">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="ca34c-1202">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="ca34c-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ca34c-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="ca34c-1204">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="ca34c-1204">Fixes for #7002</span></span>
- <span data-ttu-id="ca34c-1205">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ca34c-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca34c-1206">Az.Batch</span></span>
- <span data-ttu-id="ca34c-1207">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ca34c-1208">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ca34c-1209">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ca34c-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ca34c-1210">Az.Billing</span></span>
- <span data-ttu-id="ca34c-1211">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ca34c-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="ca34c-1213">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ca34c-1214">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ca34c-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ca34c-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="ca34c-1216">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ca34c-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ca34c-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ca34c-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ca34c-1218">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="ca34c-1220">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ca34c-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca34c-1221">Az.Monitor</span></span>
- <span data-ttu-id="ca34c-1222">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ca34c-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca34c-1223">Az.KeyVault</span></span>
- <span data-ttu-id="ca34c-1224">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="ca34c-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ca34c-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca34c-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="ca34c-1226">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ca34c-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ca34c-1227">Az.Media</span></span>
- <span data-ttu-id="ca34c-1228">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ca34c-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ca34c-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1229">Az.Network</span></span>
<span data-ttu-id="ca34c-1230">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ca34c-1231">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ca34c-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="ca34c-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ca34c-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ca34c-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca34c-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ca34c-1240">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ca34c-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca34c-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ca34c-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ca34c-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca34c-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ca34c-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ca34c-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ca34c-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ca34c-1247">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ca34c-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ca34c-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca34c-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ca34c-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca34c-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ca34c-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca34c-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ca34c-1251">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ca34c-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ca34c-1252">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ca34c-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="ca34c-1254">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ca34c-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1255">Az.Profile</span></span>
- <span data-ttu-id="ca34c-1256">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca34c-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="ca34c-1258">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ca34c-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1259">Az.Resources</span></span>
- <span data-ttu-id="ca34c-1260">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ca34c-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="ca34c-1262">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ca34c-1263">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ca34c-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ca34c-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="ca34c-1265">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ca34c-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ca34c-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1266">Az.Sql</span></span>
- <span data-ttu-id="ca34c-1267">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="ca34c-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ca34c-1268">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ca34c-1269">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ca34c-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1270">Az.Storage</span></span>
- <span data-ttu-id="ca34c-1271">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ca34c-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1272">Az.Websites</span></span>
- <span data-ttu-id="ca34c-1273">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ca34c-1274">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ca34c-1275">Generale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1275">General</span></span>

* <span data-ttu-id="ca34c-1276">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ca34c-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ca34c-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1277">Az.Compute</span></span>

* <span data-ttu-id="ca34c-1278">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="ca34c-1280">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="ca34c-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ca34c-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca34c-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="ca34c-1282">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ca34c-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="ca34c-1283">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ca34c-1284">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ca34c-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="ca34c-1286">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ca34c-1287">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ca34c-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1288">Az.Resources</span></span>

* <span data-ttu-id="ca34c-1289">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ca34c-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ca34c-1290">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ca34c-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1291">Az.Sql</span></span>

* <span data-ttu-id="ca34c-1292">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ca34c-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ca34c-1293">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="ca34c-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ca34c-1294">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ca34c-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1295">Az.Storage</span></span>

* <span data-ttu-id="ca34c-1296">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ca34c-1297">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="ca34c-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ca34c-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ca34c-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ca34c-1299">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="ca34c-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="ca34c-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca34c-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ca34c-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca34c-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ca34c-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1302">Az.Websites</span></span>

* <span data-ttu-id="ca34c-1303">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ca34c-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ca34c-1304">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ca34c-1305">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ca34c-1306">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ca34c-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca34c-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="ca34c-1308">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ca34c-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca34c-1309">Az.Automation</span></span>
* <span data-ttu-id="ca34c-1310">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="ca34c-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ca34c-1311">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ca34c-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ca34c-1312">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="ca34c-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ca34c-1313">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ca34c-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ca34c-1314">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="ca34c-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ca34c-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1315">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1316">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ca34c-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ca34c-1317">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ca34c-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="ca34c-1319">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ca34c-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ca34c-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ca34c-1321">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="ca34c-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ca34c-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1322">Az.Network</span></span>
* <span data-ttu-id="ca34c-1323">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ca34c-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ca34c-1324">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="ca34c-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ca34c-1325">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ca34c-1326">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ca34c-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ca34c-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ca34c-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ca34c-1328">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ca34c-1329">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ca34c-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ca34c-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ca34c-1331">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ca34c-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ca34c-1332">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca34c-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ca34c-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ca34c-1333">Az.Relay</span></span>
* <span data-ttu-id="ca34c-1334">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ca34c-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1335">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1336">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ca34c-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ca34c-1337">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="ca34c-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ca34c-1338">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ca34c-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ca34c-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-1340">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ca34c-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1341">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1342">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="ca34c-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ca34c-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca34c-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca34c-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca34c-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca34c-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca34c-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca34c-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca34c-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca34c-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca34c-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca34c-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca34c-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca34c-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ca34c-1351">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ca34c-1352">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ca34c-1353">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ca34c-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ca34c-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ca34c-1356">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ca34c-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ca34c-1358">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ca34c-1359">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ca34c-1360">Generale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1360">General</span></span>
* <span data-ttu-id="ca34c-1361">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="ca34c-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ca34c-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1362">Az.Profile</span></span>
* <span data-ttu-id="ca34c-1363">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca34c-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ca34c-1364">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="ca34c-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ca34c-1365">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ca34c-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ca34c-1366">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="ca34c-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ca34c-1367">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="ca34c-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ca34c-1368">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ca34c-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ca34c-1369">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="ca34c-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-1371">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1372">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1373">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca34c-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ca34c-1374">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ca34c-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ca34c-1375">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-1377">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ca34c-1378">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ca34c-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ca34c-1379">Az.Insights</span></span>
* <span data-ttu-id="ca34c-1380">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="ca34c-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ca34c-1381">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="ca34c-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ca34c-1382">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ca34c-1383">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="ca34c-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1384">Az.Network</span></span>
* <span data-ttu-id="ca34c-1385">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca34c-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ca34c-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca34c-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ca34c-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ca34c-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ca34c-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ca34c-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ca34c-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ca34c-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ca34c-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca34c-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ca34c-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ca34c-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca34c-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca34c-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca34c-1393">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="ca34c-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1394">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1395">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ca34c-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ca34c-1396">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca34c-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca34c-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="ca34c-1398">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca34c-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca34c-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca34c-1400">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ca34c-1401">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ca34c-1402">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ca34c-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ca34c-1403">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ca34c-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ca34c-1404">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ca34c-1405">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ca34c-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1406">Az.Profile</span></span>
* <span data-ttu-id="ca34c-1407">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="ca34c-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ca34c-1408">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca34c-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1409">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1410">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="ca34c-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ca34c-1411">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca34c-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca34c-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca34c-1413">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ca34c-1414">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ca34c-1415">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ca34c-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ca34c-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1418">Az.Network</span></span>
* <span data-ttu-id="ca34c-1419">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ca34c-1420">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1421">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1422">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ca34c-1423">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ca34c-1424">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ca34c-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1425">Azure.Storage</span></span>
* <span data-ttu-id="ca34c-1426">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="ca34c-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ca34c-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca34c-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ca34c-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ca34c-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ca34c-1429">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="ca34c-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ca34c-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ca34c-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ca34c-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca34c-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca34c-1432">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca34c-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca34c-1433">Az.Compute</span></span>
* <span data-ttu-id="ca34c-1434">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="ca34c-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ca34c-1435">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ca34c-1436">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="ca34c-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ca34c-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ca34c-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ca34c-1438">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ca34c-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca34c-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca34c-1439">Az.Network</span></span>
* <span data-ttu-id="ca34c-1440">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ca34c-1441">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1441">new cmdlets added</span></span>
    - <span data-ttu-id="ca34c-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca34c-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca34c-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca34c-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca34c-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca34c-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ca34c-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ca34c-1448">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="ca34c-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ca34c-1449">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ca34c-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ca34c-1450">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ca34c-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca34c-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca34c-1451">Az.RedisCache</span></span>
* <span data-ttu-id="ca34c-1452">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="ca34c-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ca34c-1453">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ca34c-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca34c-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca34c-1454">Az.Resources</span></span>
* <span data-ttu-id="ca34c-1455">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ca34c-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ca34c-1456">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="ca34c-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca34c-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca34c-1457">Az.Sql</span></span>
* <span data-ttu-id="ca34c-1458">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="ca34c-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca34c-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca34c-1459">Az.Websites</span></span>
* <span data-ttu-id="ca34c-1460">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="ca34c-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ca34c-1461">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="ca34c-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ca34c-1462">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="ca34c-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ca34c-1463">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="ca34c-1463">Initial Release</span></span>