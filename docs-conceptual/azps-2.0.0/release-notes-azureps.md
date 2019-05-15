---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048632"
---
## <a name="200---may-2019"></a><span data-ttu-id="f36cb-101">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-102">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-103">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="f36cb-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36cb-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36cb-105">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="f36cb-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f36cb-106">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="f36cb-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-107">Az.Compute</span></span>
* <span data-ttu-id="f36cb-108">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="f36cb-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f36cb-109">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f36cb-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f36cb-110">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f36cb-111">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f36cb-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f36cb-112">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f36cb-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f36cb-113">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f36cb-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f36cb-114">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="f36cb-114">Breaking changes</span></span>
    - <span data-ttu-id="f36cb-115">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f36cb-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f36cb-116">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f36cb-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f36cb-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f36cb-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="f36cb-118">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="f36cb-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f36cb-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f36cb-119">Az.Dns</span></span>
* <span data-ttu-id="f36cb-120">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="f36cb-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f36cb-121">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="f36cb-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f36cb-122">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="f36cb-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f36cb-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f36cb-123">Az.FrontDoor</span></span>
* <span data-ttu-id="f36cb-124">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f36cb-125">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="f36cb-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f36cb-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f36cb-126">Az.HDInsight</span></span>
* <span data-ttu-id="f36cb-127">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f36cb-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f36cb-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36cb-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f36cb-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36cb-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f36cb-130">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36cb-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f36cb-131">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="f36cb-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f36cb-132">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f36cb-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f36cb-133">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36cb-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36cb-134">Az.Monitor</span></span>
* <span data-ttu-id="f36cb-135">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="f36cb-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f36cb-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f36cb-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f36cb-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f36cb-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f36cb-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f36cb-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f36cb-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f36cb-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f36cb-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f36cb-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f36cb-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f36cb-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f36cb-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36cb-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36cb-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36cb-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36cb-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36cb-147">[Altre](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="f36cb-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f36cb-148">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="f36cb-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-149">Az.Network</span></span>
* <span data-ttu-id="f36cb-150">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="f36cb-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f36cb-151">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36cb-151">New cmdlets</span></span>
        - <span data-ttu-id="f36cb-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36cb-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="f36cb-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36cb-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f36cb-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36cb-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f36cb-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36cb-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f36cb-156">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f36cb-156">Updated cmdlets</span></span>
        - <span data-ttu-id="f36cb-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f36cb-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f36cb-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f36cb-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f36cb-159">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="f36cb-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f36cb-160">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="f36cb-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f36cb-161">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="f36cb-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36cb-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36cb-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36cb-163">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f36cb-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f36cb-164">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f36cb-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f36cb-165">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="f36cb-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36cb-167">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="f36cb-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f36cb-168">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f36cb-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f36cb-169">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f36cb-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f36cb-170">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="f36cb-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f36cb-171">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="f36cb-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f36cb-172">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="f36cb-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f36cb-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f36cb-173">Az.Relay</span></span>
* <span data-ttu-id="f36cb-174">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="f36cb-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36cb-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36cb-175">Az.ServiceBus</span></span>
* <span data-ttu-id="f36cb-176">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f36cb-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-177">Az.Storage</span></span>
* <span data-ttu-id="f36cb-178">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage.*' a 'Microsoft.Azure.Storage.*')</span><span class="sxs-lookup"><span data-stu-id="f36cb-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f36cb-179">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f36cb-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f36cb-180">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="f36cb-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f36cb-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="f36cb-182">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="f36cb-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f36cb-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f36cb-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f36cb-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-186">Az.Websites</span></span>
* <span data-ttu-id="f36cb-187">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f36cb-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f36cb-188">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="f36cb-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f36cb-189">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36cb-190">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="f36cb-190">Highlights since the last major release</span></span>
* <span data-ttu-id="f36cb-191">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f36cb-191">General availability of `Az` module</span></span>
* <span data-ttu-id="f36cb-192">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36cb-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36cb-193">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36cb-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36cb-194">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36cb-195">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f36cb-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36cb-196">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36cb-197">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="f36cb-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f36cb-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-198">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-199">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="f36cb-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f36cb-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f36cb-200">Az.Batch</span></span>
* <span data-ttu-id="f36cb-201">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36cb-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36cb-202">Az.Cdn</span></span>
* <span data-ttu-id="f36cb-203">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36cb-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36cb-205">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-206">Az.Compute</span></span>
* <span data-ttu-id="f36cb-207">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="f36cb-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f36cb-208">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-209">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="f36cb-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36cb-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36cb-210">Az.DataFactory</span></span>
* <span data-ttu-id="f36cb-211">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="f36cb-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-213">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36cb-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36cb-214">Az.EventGrid</span></span>
* <span data-ttu-id="f36cb-215">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f36cb-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36cb-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-216">Az.EventHub</span></span>
* <span data-ttu-id="f36cb-217">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f36cb-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f36cb-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f36cb-218">Az.HDInsight</span></span>
* <span data-ttu-id="f36cb-219">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36cb-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-220">Az.IotHub</span></span>
* <span data-ttu-id="f36cb-221">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36cb-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-222">Az.KeyVault</span></span>
* <span data-ttu-id="f36cb-223">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-224">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="f36cb-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f36cb-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f36cb-225">Az.MachineLearning</span></span>
* <span data-ttu-id="f36cb-226">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f36cb-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f36cb-227">Az.Media</span></span>
* <span data-ttu-id="f36cb-228">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36cb-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36cb-229">Az.Monitor</span></span>
  * <span data-ttu-id="f36cb-230">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="f36cb-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f36cb-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f36cb-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f36cb-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f36cb-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f36cb-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36cb-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f36cb-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36cb-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f36cb-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36cb-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f36cb-236">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f36cb-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-237">Az.Network</span></span>
* <span data-ttu-id="f36cb-238">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-239">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="f36cb-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f36cb-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f36cb-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="f36cb-241">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36cb-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36cb-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36cb-243">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f36cb-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f36cb-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f36cb-245">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36cb-247">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-248">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f36cb-249">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f36cb-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f36cb-250">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="f36cb-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f36cb-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f36cb-251">Az.RedisCache</span></span>
* <span data-ttu-id="f36cb-252">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-253">Az.Resources</span></span>
* <span data-ttu-id="f36cb-254">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="f36cb-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-255">Az.Sql</span></span>
* <span data-ttu-id="f36cb-256">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="f36cb-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f36cb-257">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-258">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="f36cb-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f36cb-259">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f36cb-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f36cb-260">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="f36cb-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f36cb-261">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="f36cb-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f36cb-262">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="f36cb-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-263">Az.Websites</span></span>
* <span data-ttu-id="f36cb-264">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="f36cb-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f36cb-265">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="f36cb-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36cb-266">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="f36cb-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f36cb-267">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f36cb-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f36cb-268">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36cb-269">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="f36cb-269">Highlights since the last major release</span></span>
* <span data-ttu-id="f36cb-270">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f36cb-270">General availability of `Az` module</span></span>
* <span data-ttu-id="f36cb-271">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36cb-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36cb-272">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36cb-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36cb-273">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36cb-274">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f36cb-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36cb-275">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36cb-276">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="f36cb-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f36cb-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-277">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-278">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f36cb-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36cb-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36cb-280">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="f36cb-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f36cb-281">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="f36cb-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36cb-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-282">Az.Automation</span></span>
* <span data-ttu-id="f36cb-283">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="f36cb-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f36cb-284">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="f36cb-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f36cb-285">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-286">Az.Compute</span></span>
* <span data-ttu-id="f36cb-287">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f36cb-288">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="f36cb-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f36cb-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="f36cb-290">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="f36cb-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36cb-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36cb-291">Az.DataFactory</span></span>
* <span data-ttu-id="f36cb-292">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f36cb-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f36cb-293">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f36cb-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-294">Az.Resources</span></span>
* <span data-ttu-id="f36cb-295">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="f36cb-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f36cb-296">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f36cb-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f36cb-297">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="f36cb-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f36cb-298">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f36cb-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f36cb-299">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="f36cb-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f36cb-300">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f36cb-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-301">Az.Sql</span></span>
* <span data-ttu-id="f36cb-302">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="f36cb-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-303">Az.Storage</span></span>
* <span data-ttu-id="f36cb-304">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="f36cb-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f36cb-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f36cb-305">New-AzStorageContext</span></span>
* <span data-ttu-id="f36cb-306">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="f36cb-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f36cb-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f36cb-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f36cb-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f36cb-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f36cb-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f36cb-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f36cb-311">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="f36cb-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f36cb-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f36cb-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f36cb-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f36cb-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f36cb-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f36cb-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f36cb-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f36cb-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f36cb-316">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36cb-317">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="f36cb-317">Highlights since the last major release</span></span>
* <span data-ttu-id="f36cb-318">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f36cb-318">General availability of `Az` module</span></span>
* <span data-ttu-id="f36cb-319">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36cb-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36cb-320">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36cb-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36cb-321">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36cb-322">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f36cb-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36cb-323">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36cb-324">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="f36cb-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36cb-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-325">Az.Automation</span></span>
* <span data-ttu-id="f36cb-326">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f36cb-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f36cb-327">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="f36cb-327">Dynamic grouping</span></span>
    * <span data-ttu-id="f36cb-328">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="f36cb-328">Pre-Post script</span></span>
    * <span data-ttu-id="f36cb-329">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="f36cb-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-330">Az.Compute</span></span>
* <span data-ttu-id="f36cb-331">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f36cb-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f36cb-332">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f36cb-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36cb-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-333">Az.KeyVault</span></span>
* <span data-ttu-id="f36cb-334">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-335">Az.Network</span></span>
* <span data-ttu-id="f36cb-336">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f36cb-337">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="f36cb-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36cb-339">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="f36cb-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f36cb-340">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="f36cb-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-341">Az.Resources</span></span>
* <span data-ttu-id="f36cb-342">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f36cb-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f36cb-343">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="f36cb-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-344">Az.Sql</span></span>
* <span data-ttu-id="f36cb-345">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="f36cb-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-346">Az.Storage</span></span>
* <span data-ttu-id="f36cb-347">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f36cb-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36cb-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36cb-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36cb-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f36cb-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f36cb-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f36cb-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f36cb-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-354">Az.Websites</span></span>
* <span data-ttu-id="f36cb-355">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="f36cb-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f36cb-356">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-357">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-358">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="f36cb-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f36cb-359">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36cb-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-360">Az.Automation</span></span>
* <span data-ttu-id="f36cb-361">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f36cb-362">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="f36cb-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f36cb-363">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="f36cb-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36cb-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36cb-364">Az.Cdn</span></span>
* <span data-ttu-id="f36cb-365">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="f36cb-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-366">Az.Compute</span></span>
* <span data-ttu-id="f36cb-367">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="f36cb-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36cb-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36cb-368">Az.DataFactory</span></span>
* <span data-ttu-id="f36cb-369">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f36cb-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36cb-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36cb-370">Az.LogicApp</span></span>
* <span data-ttu-id="f36cb-371">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="f36cb-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-372">Az.Network</span></span>
* <span data-ttu-id="f36cb-373">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36cb-375">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f36cb-376">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="f36cb-376">SDK Update</span></span>
* <span data-ttu-id="f36cb-377">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f36cb-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f36cb-378">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f36cb-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-379">Az.Resources</span></span>
* <span data-ttu-id="f36cb-380">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="f36cb-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f36cb-381">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f36cb-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f36cb-382">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f36cb-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f36cb-383">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f36cb-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f36cb-384">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f36cb-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f36cb-385">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f36cb-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-386">Az.Sql</span></span>
* <span data-ttu-id="f36cb-387">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f36cb-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f36cb-388">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="f36cb-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-389">Az.Storage</span></span>
* <span data-ttu-id="f36cb-390">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f36cb-391">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f36cb-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36cb-393">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="f36cb-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36cb-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-394">Az.Automation</span></span>
* <span data-ttu-id="f36cb-395">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f36cb-396">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f36cb-397">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36cb-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36cb-399">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f36cb-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-400">Az.Compute</span></span>
* <span data-ttu-id="f36cb-401">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="f36cb-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f36cb-402">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="f36cb-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f36cb-403">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f36cb-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f36cb-404">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f36cb-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-406">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="f36cb-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36cb-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-407">Az.EventHub</span></span>
* <span data-ttu-id="f36cb-408">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="f36cb-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f36cb-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-409">Az.KeyVault</span></span>
* <span data-ttu-id="f36cb-410">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f36cb-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36cb-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36cb-411">Az.LogicApp</span></span>
* <span data-ttu-id="f36cb-412">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f36cb-413">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="f36cb-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f36cb-414">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f36cb-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36cb-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36cb-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36cb-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36cb-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36cb-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36cb-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36cb-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f36cb-419">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f36cb-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36cb-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36cb-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36cb-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f36cb-424">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f36cb-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36cb-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36cb-425">Az.Monitor</span></span>
* <span data-ttu-id="f36cb-426">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="f36cb-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-427">Az.Network</span></span>
* <span data-ttu-id="f36cb-428">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f36cb-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36cb-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36cb-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36cb-430">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f36cb-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f36cb-431">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f36cb-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f36cb-432">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="f36cb-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f36cb-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-433">Az.Resources</span></span>
* <span data-ttu-id="f36cb-434">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f36cb-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f36cb-435">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f36cb-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f36cb-436">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f36cb-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f36cb-437">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="f36cb-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-438">Az.Sql</span></span>
* <span data-ttu-id="f36cb-439">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="f36cb-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f36cb-440">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="f36cb-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-441">Az.Websites</span></span>
* <span data-ttu-id="f36cb-442">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f36cb-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f36cb-443">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-444">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-445">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36cb-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36cb-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-446">Az.AnalysisServices</span></span>
<span data-ttu-id="f36cb-447">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f36cb-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-448">Az.Compute</span></span>
* <span data-ttu-id="f36cb-449">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="f36cb-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f36cb-450">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f36cb-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f36cb-451">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f36cb-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-452">Az.RecoveryServices</span></span>
<span data-ttu-id="f36cb-453">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f36cb-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-454">Az.Resources</span></span>
* <span data-ttu-id="f36cb-455">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="f36cb-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f36cb-456">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f36cb-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f36cb-457">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f36cb-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f36cb-458">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f36cb-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-459">Az.Sql</span></span>
* <span data-ttu-id="f36cb-460">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36cb-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f36cb-461">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="f36cb-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f36cb-462">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f36cb-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f36cb-463">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-464">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-465">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36cb-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36cb-467">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36cb-469">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f36cb-470">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-471">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-472">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f36cb-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36cb-473">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36cb-474">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f36cb-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f36cb-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f36cb-475">Az.Aks</span></span>
* <span data-ttu-id="f36cb-476">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36cb-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-477">Az.Automation</span></span>
* <span data-ttu-id="f36cb-478">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="f36cb-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f36cb-479">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36cb-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36cb-480">Az.Cdn</span></span>
* <span data-ttu-id="f36cb-481">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-482">Az.Compute</span></span>
* <span data-ttu-id="f36cb-483">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f36cb-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f36cb-484">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f36cb-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f36cb-485">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f36cb-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f36cb-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f36cb-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f36cb-487">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36cb-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36cb-488">Az.DataFactory</span></span>
* <span data-ttu-id="f36cb-489">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f36cb-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-491">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="f36cb-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f36cb-492">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f36cb-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f36cb-493">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36cb-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-494">Az.IotHub</span></span>
* <span data-ttu-id="f36cb-495">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f36cb-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36cb-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-496">Az.KeyVault</span></span>
* <span data-ttu-id="f36cb-497">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-498">Az.Network</span></span>
* <span data-ttu-id="f36cb-499">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-500">Az.Resources</span></span>
* <span data-ttu-id="f36cb-501">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="f36cb-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f36cb-502">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f36cb-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f36cb-503">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f36cb-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f36cb-504">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f36cb-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f36cb-505">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f36cb-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f36cb-506">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="f36cb-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f36cb-507">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f36cb-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36cb-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36cb-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36cb-509">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f36cb-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f36cb-510">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="f36cb-510">Fix some error messages.</span></span>
* <span data-ttu-id="f36cb-511">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="f36cb-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f36cb-512">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f36cb-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f36cb-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f36cb-513">Az.SignalR</span></span>
* <span data-ttu-id="f36cb-514">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-515">Az.Sql</span></span>
* <span data-ttu-id="f36cb-516">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36cb-517">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="f36cb-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f36cb-518">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="f36cb-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f36cb-519">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="f36cb-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-520">Az.Storage</span></span>
* <span data-ttu-id="f36cb-521">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36cb-522">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="f36cb-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f36cb-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f36cb-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f36cb-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f36cb-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f36cb-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f36cb-525">Az.TrafficManager</span></span>
* <span data-ttu-id="f36cb-526">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-527">Az.Websites</span></span>
* <span data-ttu-id="f36cb-528">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="f36cb-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36cb-529">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="f36cb-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f36cb-530">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="f36cb-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f36cb-531">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="f36cb-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36cb-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-532">Az.Accounts</span></span>
* <span data-ttu-id="f36cb-533">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f36cb-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-534">Az.Compute</span></span>
* <span data-ttu-id="f36cb-535">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f36cb-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f36cb-536">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="f36cb-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f36cb-537">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-539">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="f36cb-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f36cb-540">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="f36cb-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36cb-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36cb-541">Az.EventGrid</span></span>
* <span data-ttu-id="f36cb-542">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f36cb-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f36cb-543">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f36cb-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f36cb-544">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="f36cb-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f36cb-545">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="f36cb-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f36cb-546">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="f36cb-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f36cb-547">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="f36cb-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f36cb-548">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="f36cb-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f36cb-549">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="f36cb-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f36cb-550">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="f36cb-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f36cb-551">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="f36cb-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="f36cb-552">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f36cb-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f36cb-553">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f36cb-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36cb-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-554">Az.IotHub</span></span>
* <span data-ttu-id="f36cb-555">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="f36cb-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36cb-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36cb-556">Az.LogicApp</span></span>
* <span data-ttu-id="f36cb-557">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="f36cb-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-558">Az.Resources</span></span>
* <span data-ttu-id="f36cb-559">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f36cb-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f36cb-560">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f36cb-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f36cb-561">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f36cb-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f36cb-562">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f36cb-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f36cb-563">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="f36cb-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f36cb-564">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f36cb-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f36cb-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f36cb-565">Az.SignalR</span></span>
* <span data-ttu-id="f36cb-566">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-567">Az.Sql</span></span>
* <span data-ttu-id="f36cb-568">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="f36cb-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36cb-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-569">Az.Storage</span></span>
* <span data-ttu-id="f36cb-570">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="f36cb-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f36cb-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f36cb-571">New-AzStorageContext</span></span>
* <span data-ttu-id="f36cb-572">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="f36cb-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f36cb-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f36cb-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-574">Az.Websites</span></span>
* <span data-ttu-id="f36cb-575">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="f36cb-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f36cb-576">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f36cb-577">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f36cb-578">Generale</span><span class="sxs-lookup"><span data-stu-id="f36cb-578">General</span></span>

- <span data-ttu-id="f36cb-579">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="f36cb-579">General Availability of Az Module</span></span>
- <span data-ttu-id="f36cb-580">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="f36cb-580">Online help for each module</span></span>
- <span data-ttu-id="f36cb-581">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f36cb-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f36cb-582">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="f36cb-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f36cb-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-583">Az.Accounts</span></span>
- <span data-ttu-id="f36cb-584">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36cb-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="f36cb-585">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="f36cb-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f36cb-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36cb-586">Az.ApiManagement</span></span>
- <span data-ttu-id="f36cb-587">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="f36cb-587">Fixes for #7002</span></span>
- <span data-ttu-id="f36cb-588">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f36cb-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f36cb-589">Az.Batch</span></span>
- <span data-ttu-id="f36cb-590">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f36cb-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f36cb-591">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="f36cb-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f36cb-592">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f36cb-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f36cb-593">Az.Billing</span></span>
- <span data-ttu-id="f36cb-594">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f36cb-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-595">Az.CognitivServices</span></span>
- <span data-ttu-id="f36cb-596">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f36cb-597">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f36cb-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f36cb-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="f36cb-599">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f36cb-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f36cb-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f36cb-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f36cb-601">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="f36cb-603">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f36cb-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36cb-604">Az.Monitor</span></span>
- <span data-ttu-id="f36cb-605">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f36cb-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36cb-606">Az.KeyVault</span></span>
- <span data-ttu-id="f36cb-607">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="f36cb-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f36cb-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f36cb-608">Az.MachineLearning</span></span>
- <span data-ttu-id="f36cb-609">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f36cb-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f36cb-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f36cb-610">Az.Media</span></span>
- <span data-ttu-id="f36cb-611">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f36cb-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f36cb-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-612">Az.Network</span></span>
<span data-ttu-id="f36cb-613">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f36cb-614">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="f36cb-614">New cmdlets added:</span></span>
        - <span data-ttu-id="f36cb-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f36cb-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f36cb-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36cb-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f36cb-623">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36cb-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f36cb-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f36cb-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f36cb-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f36cb-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f36cb-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f36cb-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f36cb-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f36cb-629">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="f36cb-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f36cb-630">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f36cb-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f36cb-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36cb-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f36cb-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36cb-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f36cb-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36cb-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f36cb-634">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f36cb-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f36cb-635">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f36cb-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36cb-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="f36cb-637">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f36cb-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36cb-638">Az.Profile</span></span>
- <span data-ttu-id="f36cb-639">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36cb-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="f36cb-641">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f36cb-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-642">Az.Resources</span></span>
- <span data-ttu-id="f36cb-643">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f36cb-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36cb-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="f36cb-645">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f36cb-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f36cb-646">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f36cb-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f36cb-647">Az.SIgnalR</span></span>
- <span data-ttu-id="f36cb-648">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f36cb-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f36cb-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-649">Az.Sql</span></span>
- <span data-ttu-id="f36cb-650">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="f36cb-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f36cb-651">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f36cb-652">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f36cb-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-653">Az.Storage</span></span>
- <span data-ttu-id="f36cb-654">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f36cb-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-655">Az.Websites</span></span>
- <span data-ttu-id="f36cb-656">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36cb-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f36cb-657">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f36cb-658">Generale</span><span class="sxs-lookup"><span data-stu-id="f36cb-658">General</span></span>

* <span data-ttu-id="f36cb-659">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f36cb-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f36cb-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-660">Az.Compute</span></span>

* <span data-ttu-id="f36cb-661">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f36cb-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="f36cb-663">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="f36cb-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f36cb-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f36cb-664">Az.FrontDoor</span></span>

* <span data-ttu-id="f36cb-665">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="f36cb-665">Fixed some broken links</span></span>
    - <span data-ttu-id="f36cb-666">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f36cb-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f36cb-667">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f36cb-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f36cb-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="f36cb-669">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="f36cb-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f36cb-670">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="f36cb-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f36cb-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-671">Az.Resources</span></span>

* <span data-ttu-id="f36cb-672">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f36cb-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f36cb-673">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="f36cb-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f36cb-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-674">Az.Sql</span></span>

* <span data-ttu-id="f36cb-675">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f36cb-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f36cb-676">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="f36cb-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f36cb-677">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="f36cb-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f36cb-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-678">Az.Storage</span></span>

* <span data-ttu-id="f36cb-679">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f36cb-680">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="f36cb-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f36cb-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f36cb-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f36cb-682">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="f36cb-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="f36cb-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f36cb-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f36cb-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f36cb-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f36cb-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-685">Az.Websites</span></span>

* <span data-ttu-id="f36cb-686">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f36cb-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f36cb-687">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f36cb-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f36cb-688">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f36cb-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f36cb-689">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f36cb-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36cb-690">Az.ApiManagement</span></span>
* <span data-ttu-id="f36cb-691">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f36cb-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f36cb-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36cb-692">Az.Automation</span></span>
* <span data-ttu-id="f36cb-693">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="f36cb-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f36cb-694">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="f36cb-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f36cb-695">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="f36cb-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f36cb-696">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="f36cb-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f36cb-697">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="f36cb-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f36cb-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-698">Az.Compute</span></span>
* <span data-ttu-id="f36cb-699">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f36cb-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f36cb-700">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f36cb-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f36cb-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="f36cb-702">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f36cb-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f36cb-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f36cb-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f36cb-704">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="f36cb-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f36cb-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-705">Az.Network</span></span>
* <span data-ttu-id="f36cb-706">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f36cb-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f36cb-707">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="f36cb-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f36cb-708">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f36cb-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f36cb-709">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f36cb-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f36cb-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f36cb-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f36cb-711">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="f36cb-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f36cb-712">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="f36cb-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f36cb-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f36cb-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f36cb-714">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f36cb-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f36cb-715">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f36cb-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f36cb-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f36cb-716">Az.Relay</span></span>
* <span data-ttu-id="f36cb-717">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f36cb-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f36cb-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-718">Az.Resources</span></span>
* <span data-ttu-id="f36cb-719">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f36cb-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f36cb-720">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="f36cb-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f36cb-721">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f36cb-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f36cb-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36cb-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36cb-723">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="f36cb-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f36cb-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-724">Az.Sql</span></span>
* <span data-ttu-id="f36cb-725">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="f36cb-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f36cb-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36cb-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36cb-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36cb-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36cb-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36cb-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36cb-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36cb-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36cb-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36cb-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36cb-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36cb-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36cb-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f36cb-734">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="f36cb-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f36cb-735">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f36cb-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f36cb-736">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="f36cb-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f36cb-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f36cb-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f36cb-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f36cb-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f36cb-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f36cb-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f36cb-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f36cb-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f36cb-741">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f36cb-742">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f36cb-743">Generale</span><span class="sxs-lookup"><span data-stu-id="f36cb-743">General</span></span>
* <span data-ttu-id="f36cb-744">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="f36cb-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f36cb-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36cb-745">Az.Profile</span></span>
* <span data-ttu-id="f36cb-746">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36cb-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f36cb-747">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="f36cb-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f36cb-748">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f36cb-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f36cb-749">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="f36cb-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f36cb-750">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="f36cb-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f36cb-751">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="f36cb-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f36cb-752">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="f36cb-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36cb-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36cb-754">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f36cb-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-755">Az.Compute</span></span>
* <span data-ttu-id="f36cb-756">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f36cb-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f36cb-757">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f36cb-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f36cb-758">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="f36cb-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-760">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f36cb-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f36cb-761">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="f36cb-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f36cb-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f36cb-762">Az.Insights</span></span>
* <span data-ttu-id="f36cb-763">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="f36cb-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f36cb-764">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="f36cb-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f36cb-765">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f36cb-766">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="f36cb-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-767">Az.Network</span></span>
* <span data-ttu-id="f36cb-768">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f36cb-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f36cb-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f36cb-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f36cb-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f36cb-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f36cb-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f36cb-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f36cb-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f36cb-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f36cb-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f36cb-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f36cb-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f36cb-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36cb-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36cb-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36cb-776">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="f36cb-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-777">Az.Resources</span></span>
* <span data-ttu-id="f36cb-778">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f36cb-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f36cb-779">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f36cb-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36cb-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36cb-780">Az.ServiceBus</span></span>
* <span data-ttu-id="f36cb-781">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="f36cb-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36cb-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36cb-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36cb-783">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="f36cb-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f36cb-784">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f36cb-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f36cb-785">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f36cb-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f36cb-786">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f36cb-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f36cb-787">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f36cb-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f36cb-788">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f36cb-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36cb-789">Az.Profile</span></span>
* <span data-ttu-id="f36cb-790">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="f36cb-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f36cb-791">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36cb-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-792">Az.Compute</span></span>
* <span data-ttu-id="f36cb-793">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="f36cb-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f36cb-794">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f36cb-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36cb-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36cb-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36cb-796">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f36cb-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f36cb-797">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f36cb-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f36cb-798">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f36cb-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f36cb-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f36cb-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f36cb-800">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f36cb-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-801">Az.Network</span></span>
* <span data-ttu-id="f36cb-802">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="f36cb-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f36cb-803">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f36cb-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-804">Az.Resources</span></span>
* <span data-ttu-id="f36cb-805">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="f36cb-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f36cb-806">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="f36cb-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f36cb-807">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f36cb-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f36cb-808">Azure.Storage</span></span>
* <span data-ttu-id="f36cb-809">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="f36cb-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f36cb-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f36cb-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f36cb-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f36cb-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f36cb-812">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="f36cb-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f36cb-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f36cb-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f36cb-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36cb-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36cb-815">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="f36cb-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36cb-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36cb-816">Az.Compute</span></span>
* <span data-ttu-id="f36cb-817">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="f36cb-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f36cb-818">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f36cb-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f36cb-819">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="f36cb-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f36cb-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f36cb-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f36cb-821">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="f36cb-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36cb-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36cb-822">Az.Network</span></span>
* <span data-ttu-id="f36cb-823">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36cb-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f36cb-824">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36cb-824">new cmdlets added</span></span>
    - <span data-ttu-id="f36cb-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36cb-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36cb-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36cb-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36cb-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36cb-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36cb-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36cb-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36cb-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f36cb-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f36cb-831">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="f36cb-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f36cb-832">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f36cb-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f36cb-833">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f36cb-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f36cb-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f36cb-834">Az.RedisCache</span></span>
* <span data-ttu-id="f36cb-835">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="f36cb-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f36cb-836">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f36cb-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36cb-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36cb-837">Az.Resources</span></span>
* <span data-ttu-id="f36cb-838">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f36cb-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f36cb-839">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="f36cb-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36cb-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36cb-840">Az.Sql</span></span>
* <span data-ttu-id="f36cb-841">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="f36cb-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36cb-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36cb-842">Az.Websites</span></span>
* <span data-ttu-id="f36cb-843">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="f36cb-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f36cb-844">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="f36cb-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f36cb-845">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="f36cb-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f36cb-846">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="f36cb-846">Initial Release</span></span>