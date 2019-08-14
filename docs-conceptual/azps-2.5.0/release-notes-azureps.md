---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861183"
---
## <a name="250---july-2019"></a><span data-ttu-id="941b5-101">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-102">Az.Accounts</span></span>
* <span data-ttu-id="941b5-103">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="941b5-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="941b5-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="941b5-105">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="941b5-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="941b5-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-106">Az.Automation</span></span>
* <span data-ttu-id="941b5-107">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="941b5-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-109">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="941b5-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-110">Az.Compute</span></span>
* <span data-ttu-id="941b5-111">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="941b5-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="941b5-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="941b5-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="941b5-113">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="941b5-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="941b5-114">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="941b5-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-115">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-116">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="941b5-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="941b5-117">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="941b5-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="941b5-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="941b5-118">Az.EventHub</span></span>
* <span data-ttu-id="941b5-119">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="941b5-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="941b5-120">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="941b5-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="941b5-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-121">Az.KeyVault</span></span>
* <span data-ttu-id="941b5-122">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="941b5-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="941b5-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="941b5-123">Az.LogicApp</span></span>
* <span data-ttu-id="941b5-124">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="941b5-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="941b5-125">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="941b5-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="941b5-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="941b5-126">Az.ManagedServices</span></span>
* <span data-ttu-id="941b5-127">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="941b5-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-128">Az.Network</span></span>
* <span data-ttu-id="941b5-129">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="941b5-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="941b5-130">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-130">New cmdlets</span></span>
        - <span data-ttu-id="941b5-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="941b5-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="941b5-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="941b5-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="941b5-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="941b5-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="941b5-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="941b5-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="941b5-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="941b5-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="941b5-139">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="941b5-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="941b5-140">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="941b5-141">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag per indicare l'abilitazione o la disabilitazione dell'applicazione dei criteri di rete su endpoint privati in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="941b5-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="941b5-142">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag per indicare l'abilitazione o la disabilitazione dell'applicazione dei criteri di rete sul servizio di collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="941b5-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="941b5-143">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="941b5-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="941b5-144">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="941b5-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="941b5-145">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-145">Updated cmdlets</span></span>
        - <span data-ttu-id="941b5-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="941b5-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="941b5-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="941b5-149">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="941b5-150">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="941b5-151">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="941b5-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="941b5-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="941b5-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="941b5-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="941b5-155">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="941b5-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="941b5-156">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="941b5-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="941b5-157">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="941b5-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="941b5-159">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="941b5-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="941b5-160">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="941b5-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-162">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="941b5-163">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="941b5-164">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="941b5-165">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="941b5-166">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="941b5-167">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="941b5-168">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="941b5-169">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="941b5-170">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="941b5-171">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="941b5-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-172">Az.Resources</span></span>
- <span data-ttu-id="941b5-173">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="941b5-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="941b5-174">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="941b5-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="941b5-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="941b5-175">Az.ServiceBus</span></span>
* <span data-ttu-id="941b5-176">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="941b5-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="941b5-177">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="941b5-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-178">Az.Sql</span></span>
* <span data-ttu-id="941b5-179">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="941b5-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="941b5-180">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="941b5-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="941b5-181">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="941b5-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-182">Az.Storage</span></span>
* <span data-ttu-id="941b5-183">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="941b5-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="941b5-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="941b5-184">Az.StorageSync</span></span>
* <span data-ttu-id="941b5-185">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="941b5-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="941b5-186">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="941b5-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-187">Az.Websites</span></span>
* <span data-ttu-id="941b5-188">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="941b5-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="941b5-189">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="941b5-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="941b5-190">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="941b5-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="941b5-191">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-192">Az.Accounts</span></span>
* <span data-ttu-id="941b5-193">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="941b5-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="941b5-194">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="941b5-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="941b5-195">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="941b5-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="941b5-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="941b5-196">Az.Advisor</span></span>
* <span data-ttu-id="941b5-197">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="941b5-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="941b5-198">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="941b5-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="941b5-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-199">Az.ApiManagement</span></span>
* <span data-ttu-id="941b5-200">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="941b5-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="941b5-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="941b5-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="941b5-202">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="941b5-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="941b5-203">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="941b5-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="941b5-204">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="941b5-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="941b5-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="941b5-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="941b5-206">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="941b5-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-207">Az.Automation</span></span>
* <span data-ttu-id="941b5-208">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="941b5-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-209">Az.Compute</span></span>
* <span data-ttu-id="941b5-210">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-211">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-212">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="941b5-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="941b5-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="941b5-213">Az.EventGrid</span></span>
* <span data-ttu-id="941b5-214">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="941b5-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="941b5-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="941b5-215">Az.IotHub</span></span>
* <span data-ttu-id="941b5-216">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="941b5-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-217">Az.Network</span></span>
* <span data-ttu-id="941b5-218">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="941b5-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="941b5-219">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="941b5-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="941b5-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="941b5-221">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="941b5-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="941b5-222">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="941b5-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="941b5-224">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="941b5-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-226">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="941b5-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-227">Az.Resources</span></span>
    - <span data-ttu-id="941b5-228">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="941b5-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="941b5-229">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="941b5-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="941b5-230">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="941b5-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="941b5-231">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="941b5-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="941b5-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="941b5-232">Az.ServiceBus</span></span>
* <span data-ttu-id="941b5-233">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="941b5-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-234">Az.Sql</span></span>
* <span data-ttu-id="941b5-235">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="941b5-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="941b5-236">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="941b5-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="941b5-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="941b5-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="941b5-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="941b5-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="941b5-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="941b5-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="941b5-243">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="941b5-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-244">Az.Storage</span></span>
* <span data-ttu-id="941b5-245">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="941b5-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="941b5-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="941b5-247">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="941b5-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="941b5-248">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="941b5-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="941b5-249">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="941b5-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="941b5-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="941b5-252">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="941b5-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="941b5-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="941b5-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="941b5-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="941b5-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="941b5-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="941b5-255">Az.StorageSync</span></span>
* <span data-ttu-id="941b5-256">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="941b5-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="941b5-257">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-258">Az.Accounts</span></span>
* <span data-ttu-id="941b5-259">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="941b5-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="941b5-260">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="941b5-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="941b5-261">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="941b5-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="941b5-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="941b5-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="941b5-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="941b5-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-264">Az.Compute</span></span>
* <span data-ttu-id="941b5-265">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="941b5-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="941b5-266">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="941b5-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="941b5-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="941b5-267">Az.Dns</span></span>
* <span data-ttu-id="941b5-268">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="941b5-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="941b5-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="941b5-269">Az.EventGrid</span></span>
* <span data-ttu-id="941b5-270">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="941b5-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="941b5-271">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-271">New cmdlets:</span></span>
    - <span data-ttu-id="941b5-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="941b5-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="941b5-273">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="941b5-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="941b5-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="941b5-275">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="941b5-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="941b5-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="941b5-277">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="941b5-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="941b5-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="941b5-279">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="941b5-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="941b5-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="941b5-281">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="941b5-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="941b5-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="941b5-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="941b5-283">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="941b5-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="941b5-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="941b5-285">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="941b5-286">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="941b5-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="941b5-287">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="941b5-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="941b5-288">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="941b5-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="941b5-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="941b5-290">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="941b5-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="941b5-291">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="941b5-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="941b5-292">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="941b5-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="941b5-293">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="941b5-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="941b5-294">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="941b5-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="941b5-295">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="941b5-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="941b5-296">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="941b5-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="941b5-297">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="941b5-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="941b5-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="941b5-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="941b5-299">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="941b5-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="941b5-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="941b5-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="941b5-301">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="941b5-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="941b5-302">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="941b5-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="941b5-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="941b5-303">Az.FrontDoor</span></span>
* <span data-ttu-id="941b5-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="941b5-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="941b5-305">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="941b5-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="941b5-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="941b5-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="941b5-307">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="941b5-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-308">Az.Network</span></span>
* <span data-ttu-id="941b5-309">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="941b5-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="941b5-310">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-310">New cmdlets</span></span>
        - <span data-ttu-id="941b5-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="941b5-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="941b5-312">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="941b5-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="941b5-313">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-313">New cmdlets</span></span> 
        - <span data-ttu-id="941b5-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="941b5-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="941b5-315">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="941b5-316">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-316">New cmdlets</span></span> 
        - <span data-ttu-id="941b5-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="941b5-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="941b5-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="941b5-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="941b5-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="941b5-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="941b5-322">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="941b5-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="941b5-323">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-323">New cmdlets</span></span>
        - <span data-ttu-id="941b5-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="941b5-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="941b5-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="941b5-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="941b5-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="941b5-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="941b5-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="941b5-328">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="941b5-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="941b5-329">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="941b5-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="941b5-330">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="941b5-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="941b5-331">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="941b5-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="941b5-332">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="941b5-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="941b5-333">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="941b5-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="941b5-334">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="941b5-335">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="941b5-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="941b5-336">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="941b5-337">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="941b5-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="941b5-338">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="941b5-339">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="941b5-340">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="941b5-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="941b5-341">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="941b5-342">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="941b5-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="941b5-343">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="941b5-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="941b5-344">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="941b5-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="941b5-345">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="941b5-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="941b5-346">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="941b5-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="941b5-347">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="941b5-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="941b5-348">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="941b5-349">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="941b5-350">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="941b5-352">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="941b5-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-353">Az.Resources</span></span>
* <span data-ttu-id="941b5-354">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="941b5-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="941b5-355">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="941b5-356">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="941b5-357">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="941b5-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="941b5-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="941b5-359">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="941b5-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-360">Az.Sql</span></span>
* <span data-ttu-id="941b5-361">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="941b5-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="941b5-362">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="941b5-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="941b5-363">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="941b5-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="941b5-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="941b5-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="941b5-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="941b5-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="941b5-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="941b5-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="941b5-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="941b5-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="941b5-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="941b5-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-369">Az.Storage</span></span>
* <span data-ttu-id="941b5-370">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="941b5-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="941b5-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="941b5-372">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="941b5-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="941b5-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-374">Az.Websites</span></span>
* <span data-ttu-id="941b5-375">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="941b5-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="941b5-376">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="941b5-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="941b5-377">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="941b5-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="941b5-378">Az.Cdn</span></span>
* <span data-ttu-id="941b5-379">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="941b5-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-380">Az.Compute</span></span>
* <span data-ttu-id="941b5-381">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="941b5-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="941b5-382">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="941b5-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="941b5-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="941b5-383">Az.EventHub</span></span>
* <span data-ttu-id="941b5-384">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="941b5-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="941b5-385">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941b5-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-386">Az.Network</span></span>
* <span data-ttu-id="941b5-387">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="941b5-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="941b5-388">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="941b5-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="941b5-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="941b5-390">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="941b5-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-392">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="941b5-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="941b5-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="941b5-393">Az.ServiceBus</span></span>
* <span data-ttu-id="941b5-394">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941b5-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="941b5-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="941b5-396">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="941b5-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="941b5-397">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="941b5-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-398">Az.Sql</span></span>
* <span data-ttu-id="941b5-399">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="941b5-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="941b5-400">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="941b5-401">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="941b5-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="941b5-402">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="941b5-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-403">Az.Websites</span></span>
* <span data-ttu-id="941b5-404">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="941b5-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="941b5-405">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="941b5-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-406">Az.ApiManagement</span></span>
* <span data-ttu-id="941b5-407">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="941b5-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="941b5-408">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="941b5-409">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="941b5-410">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="941b5-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="941b5-411">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="941b5-412">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="941b5-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="941b5-413">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="941b5-414">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="941b5-415">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="941b5-416">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="941b5-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="941b5-417">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="941b5-418">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="941b5-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="941b5-419">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="941b5-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="941b5-420">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="941b5-421">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="941b5-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="941b5-422">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="941b5-423">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="941b5-424">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="941b5-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="941b5-425">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="941b5-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="941b5-426">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="941b5-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="941b5-427">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="941b5-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="941b5-428">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="941b5-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="941b5-429">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="941b5-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="941b5-430">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="941b5-431">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="941b5-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="941b5-432">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="941b5-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="941b5-433">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="941b5-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="941b5-434">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="941b5-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="941b5-435">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="941b5-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="941b5-436">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="941b5-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="941b5-437">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="941b5-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="941b5-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="941b5-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="941b5-439">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="941b5-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="941b5-440">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="941b5-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="941b5-441">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="941b5-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="941b5-442">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="941b5-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="941b5-443">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="941b5-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="941b5-444">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="941b5-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="941b5-445">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="941b5-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="941b5-446">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="941b5-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="941b5-447">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="941b5-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="941b5-448">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="941b5-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="941b5-449">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="941b5-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="941b5-450">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="941b5-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="941b5-451">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="941b5-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="941b5-452">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="941b5-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="941b5-453">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="941b5-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="941b5-454">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="941b5-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="941b5-455">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="941b5-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="941b5-456">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="941b5-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="941b5-457">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="941b5-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="941b5-458">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="941b5-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="941b5-459">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="941b5-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="941b5-460">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="941b5-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="941b5-461">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="941b5-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="941b5-462">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="941b5-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="941b5-463">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="941b5-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="941b5-464">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="941b5-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="941b5-465">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="941b5-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="941b5-466">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="941b5-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="941b5-467">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="941b5-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="941b5-468">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="941b5-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="941b5-469">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="941b5-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="941b5-470">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="941b5-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="941b5-471">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="941b5-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="941b5-472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="941b5-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="941b5-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="941b5-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="941b5-474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="941b5-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="941b5-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="941b5-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="941b5-476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="941b5-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="941b5-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="941b5-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="941b5-478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="941b5-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="941b5-479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="941b5-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="941b5-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="941b5-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="941b5-481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="941b5-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="941b5-482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="941b5-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="941b5-483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="941b5-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-484">Az.Automation</span></span>
* <span data-ttu-id="941b5-485">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="941b5-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="941b5-486">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="941b5-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="941b5-487">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="941b5-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="941b5-488">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="941b5-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="941b5-489">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="941b5-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="941b5-490">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="941b5-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="941b5-491">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="941b5-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-492">Az.Compute</span></span>
* <span data-ttu-id="941b5-493">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="941b5-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="941b5-494">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="941b5-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-496">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="941b5-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="941b5-497">Az.Monitor</span></span>
* <span data-ttu-id="941b5-498">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="941b5-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-499">Az.Network</span></span>
* <span data-ttu-id="941b5-500">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="941b5-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="941b5-501">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="941b5-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="941b5-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="941b5-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="941b5-503">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="941b5-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-504">Az.Resources</span></span>
* <span data-ttu-id="941b5-505">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="941b5-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-506">Az.Sql</span></span>
* <span data-ttu-id="941b5-507">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="941b5-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="941b5-508">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-509">Az.Accounts</span></span>
* <span data-ttu-id="941b5-510">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="941b5-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-512">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="941b5-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="941b5-513">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="941b5-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-514">Az.Compute</span></span>
* <span data-ttu-id="941b5-515">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="941b5-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="941b5-516">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="941b5-517">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="941b5-518">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="941b5-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="941b5-519">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="941b5-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="941b5-520">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="941b5-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="941b5-521">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="941b5-521">Breaking changes</span></span>
    - <span data-ttu-id="941b5-522">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="941b5-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="941b5-523">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="941b5-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="941b5-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="941b5-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="941b5-525">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="941b5-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="941b5-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="941b5-526">Az.Dns</span></span>
* <span data-ttu-id="941b5-527">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="941b5-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="941b5-528">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="941b5-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="941b5-529">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="941b5-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="941b5-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="941b5-530">Az.FrontDoor</span></span>
* <span data-ttu-id="941b5-531">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="941b5-532">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="941b5-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="941b5-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="941b5-533">Az.HDInsight</span></span>
* <span data-ttu-id="941b5-534">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="941b5-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="941b5-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="941b5-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="941b5-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="941b5-537">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="941b5-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="941b5-538">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="941b5-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="941b5-539">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="941b5-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="941b5-540">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="941b5-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="941b5-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="941b5-541">Az.Monitor</span></span>
* <span data-ttu-id="941b5-542">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="941b5-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="941b5-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="941b5-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="941b5-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="941b5-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="941b5-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="941b5-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="941b5-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="941b5-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="941b5-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="941b5-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="941b5-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="941b5-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="941b5-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="941b5-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="941b5-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="941b5-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="941b5-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="941b5-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="941b5-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="941b5-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="941b5-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="941b5-554">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="941b5-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="941b5-555">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="941b5-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-556">Az.Network</span></span>
* <span data-ttu-id="941b5-557">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="941b5-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="941b5-558">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-558">New cmdlets</span></span>
        - <span data-ttu-id="941b5-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="941b5-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="941b5-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="941b5-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="941b5-563">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="941b5-563">Updated cmdlets</span></span>
        - <span data-ttu-id="941b5-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="941b5-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="941b5-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="941b5-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="941b5-566">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="941b5-567">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="941b5-568">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="941b5-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="941b5-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="941b5-570">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="941b5-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="941b5-571">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="941b5-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="941b5-572">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="941b5-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-574">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="941b5-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="941b5-575">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="941b5-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="941b5-576">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="941b5-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="941b5-577">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="941b5-578">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="941b5-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="941b5-579">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="941b5-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="941b5-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="941b5-580">Az.Relay</span></span>
* <span data-ttu-id="941b5-581">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="941b5-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="941b5-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="941b5-582">Az.ServiceBus</span></span>
* <span data-ttu-id="941b5-583">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="941b5-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-584">Az.Storage</span></span>
* <span data-ttu-id="941b5-585">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="941b5-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="941b5-586">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="941b5-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="941b5-587">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="941b5-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="941b5-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="941b5-589">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="941b5-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="941b5-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="941b5-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="941b5-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-593">Az.Websites</span></span>
* <span data-ttu-id="941b5-594">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="941b5-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="941b5-595">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="941b5-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="941b5-596">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="941b5-597">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="941b5-597">Highlights since the last major release</span></span>
* <span data-ttu-id="941b5-598">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="941b5-598">General availability of `Az` module</span></span>
* <span data-ttu-id="941b5-599">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="941b5-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="941b5-600">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="941b5-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="941b5-601">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="941b5-602">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="941b5-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="941b5-603">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="941b5-604">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="941b5-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="941b5-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-605">Az.Accounts</span></span>
* <span data-ttu-id="941b5-606">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="941b5-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="941b5-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="941b5-607">Az.Batch</span></span>
* <span data-ttu-id="941b5-608">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="941b5-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="941b5-609">Az.Cdn</span></span>
* <span data-ttu-id="941b5-610">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-612">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-613">Az.Compute</span></span>
* <span data-ttu-id="941b5-614">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="941b5-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="941b5-615">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-616">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="941b5-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-617">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-618">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="941b5-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-620">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="941b5-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="941b5-621">Az.EventGrid</span></span>
* <span data-ttu-id="941b5-622">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="941b5-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="941b5-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="941b5-623">Az.EventHub</span></span>
* <span data-ttu-id="941b5-624">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="941b5-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="941b5-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="941b5-625">Az.HDInsight</span></span>
* <span data-ttu-id="941b5-626">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="941b5-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="941b5-627">Az.IotHub</span></span>
* <span data-ttu-id="941b5-628">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="941b5-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-629">Az.KeyVault</span></span>
* <span data-ttu-id="941b5-630">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-631">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="941b5-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="941b5-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="941b5-632">Az.MachineLearning</span></span>
* <span data-ttu-id="941b5-633">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="941b5-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="941b5-634">Az.Media</span></span>
* <span data-ttu-id="941b5-635">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="941b5-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="941b5-636">Az.Monitor</span></span>
  * <span data-ttu-id="941b5-637">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="941b5-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="941b5-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="941b5-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="941b5-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="941b5-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="941b5-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="941b5-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="941b5-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="941b5-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="941b5-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="941b5-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="941b5-643">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="941b5-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-644">Az.Network</span></span>
* <span data-ttu-id="941b5-645">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-646">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="941b5-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="941b5-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="941b5-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="941b5-648">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="941b5-650">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="941b5-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="941b5-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="941b5-652">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-654">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-655">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="941b5-656">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="941b5-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="941b5-657">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="941b5-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="941b5-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="941b5-658">Az.RedisCache</span></span>
* <span data-ttu-id="941b5-659">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-660">Az.Resources</span></span>
* <span data-ttu-id="941b5-661">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="941b5-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-662">Az.Sql</span></span>
* <span data-ttu-id="941b5-663">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="941b5-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="941b5-664">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-665">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="941b5-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="941b5-666">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="941b5-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="941b5-667">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="941b5-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="941b5-668">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="941b5-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="941b5-669">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="941b5-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-670">Az.Websites</span></span>
* <span data-ttu-id="941b5-671">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="941b5-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="941b5-672">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="941b5-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="941b5-673">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="941b5-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="941b5-674">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="941b5-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="941b5-675">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="941b5-676">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="941b5-676">Highlights since the last major release</span></span>
* <span data-ttu-id="941b5-677">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="941b5-677">General availability of `Az` module</span></span>
* <span data-ttu-id="941b5-678">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="941b5-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="941b5-679">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="941b5-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="941b5-680">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="941b5-681">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="941b5-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="941b5-682">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="941b5-683">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="941b5-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="941b5-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-684">Az.Accounts</span></span>
* <span data-ttu-id="941b5-685">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="941b5-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="941b5-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="941b5-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="941b5-687">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="941b5-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="941b5-688">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="941b5-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-689">Az.Automation</span></span>
* <span data-ttu-id="941b5-690">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="941b5-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="941b5-691">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="941b5-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="941b5-692">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-693">Az.Compute</span></span>
* <span data-ttu-id="941b5-694">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="941b5-695">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="941b5-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="941b5-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="941b5-697">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="941b5-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-698">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-699">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="941b5-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="941b5-700">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="941b5-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-701">Az.Resources</span></span>
* <span data-ttu-id="941b5-702">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="941b5-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="941b5-703">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="941b5-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="941b5-704">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="941b5-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="941b5-705">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="941b5-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="941b5-706">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="941b5-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="941b5-707">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="941b5-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-708">Az.Sql</span></span>
* <span data-ttu-id="941b5-709">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="941b5-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-710">Az.Storage</span></span>
* <span data-ttu-id="941b5-711">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="941b5-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="941b5-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="941b5-712">New-AzStorageContext</span></span>
* <span data-ttu-id="941b5-713">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="941b5-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="941b5-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="941b5-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="941b5-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="941b5-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="941b5-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="941b5-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="941b5-718">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="941b5-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="941b5-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="941b5-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="941b5-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="941b5-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="941b5-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="941b5-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="941b5-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="941b5-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="941b5-723">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="941b5-724">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="941b5-724">Highlights since the last major release</span></span>
* <span data-ttu-id="941b5-725">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="941b5-725">General availability of `Az` module</span></span>
* <span data-ttu-id="941b5-726">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="941b5-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="941b5-727">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="941b5-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="941b5-728">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="941b5-729">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="941b5-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="941b5-730">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="941b5-731">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="941b5-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-732">Az.Automation</span></span>
* <span data-ttu-id="941b5-733">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="941b5-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="941b5-734">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="941b5-734">Dynamic grouping</span></span>
    * <span data-ttu-id="941b5-735">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="941b5-735">Pre-Post script</span></span>
    * <span data-ttu-id="941b5-736">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="941b5-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-737">Az.Compute</span></span>
* <span data-ttu-id="941b5-738">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="941b5-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="941b5-739">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="941b5-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="941b5-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-740">Az.KeyVault</span></span>
* <span data-ttu-id="941b5-741">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-742">Az.Network</span></span>
* <span data-ttu-id="941b5-743">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="941b5-744">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="941b5-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-746">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="941b5-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="941b5-747">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="941b5-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-748">Az.Resources</span></span>
* <span data-ttu-id="941b5-749">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="941b5-750">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="941b5-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-751">Az.Sql</span></span>
* <span data-ttu-id="941b5-752">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="941b5-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-753">Az.Storage</span></span>
* <span data-ttu-id="941b5-754">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="941b5-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="941b5-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="941b5-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="941b5-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="941b5-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="941b5-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="941b5-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="941b5-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="941b5-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="941b5-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-761">Az.Websites</span></span>
* <span data-ttu-id="941b5-762">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="941b5-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="941b5-763">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-764">Az.Accounts</span></span>
* <span data-ttu-id="941b5-765">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="941b5-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="941b5-766">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-767">Az.Automation</span></span>
* <span data-ttu-id="941b5-768">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="941b5-769">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="941b5-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="941b5-770">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="941b5-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="941b5-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="941b5-771">Az.Cdn</span></span>
* <span data-ttu-id="941b5-772">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="941b5-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-773">Az.Compute</span></span>
* <span data-ttu-id="941b5-774">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="941b5-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-775">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-776">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="941b5-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="941b5-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="941b5-777">Az.LogicApp</span></span>
* <span data-ttu-id="941b5-778">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="941b5-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-779">Az.Network</span></span>
* <span data-ttu-id="941b5-780">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="941b5-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-782">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="941b5-783">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="941b5-783">SDK Update</span></span>
* <span data-ttu-id="941b5-784">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="941b5-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="941b5-785">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="941b5-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-786">Az.Resources</span></span>
* <span data-ttu-id="941b5-787">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="941b5-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="941b5-788">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="941b5-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="941b5-789">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="941b5-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="941b5-790">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="941b5-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="941b5-791">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="941b5-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="941b5-792">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="941b5-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-793">Az.Sql</span></span>
* <span data-ttu-id="941b5-794">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="941b5-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="941b5-795">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="941b5-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-796">Az.Storage</span></span>
* <span data-ttu-id="941b5-797">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="941b5-798">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="941b5-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="941b5-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="941b5-800">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="941b5-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-801">Az.Automation</span></span>
* <span data-ttu-id="941b5-802">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="941b5-803">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="941b5-804">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-806">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="941b5-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-807">Az.Compute</span></span>
* <span data-ttu-id="941b5-808">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="941b5-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="941b5-809">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="941b5-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="941b5-810">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="941b5-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="941b5-811">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="941b5-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-813">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="941b5-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="941b5-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="941b5-814">Az.EventHub</span></span>
* <span data-ttu-id="941b5-815">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="941b5-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="941b5-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-816">Az.KeyVault</span></span>
* <span data-ttu-id="941b5-817">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="941b5-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="941b5-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="941b5-818">Az.LogicApp</span></span>
* <span data-ttu-id="941b5-819">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="941b5-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="941b5-820">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="941b5-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="941b5-821">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="941b5-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="941b5-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="941b5-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="941b5-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="941b5-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="941b5-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="941b5-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="941b5-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="941b5-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="941b5-826">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="941b5-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="941b5-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="941b5-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="941b5-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="941b5-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="941b5-831">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="941b5-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="941b5-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="941b5-832">Az.Monitor</span></span>
* <span data-ttu-id="941b5-833">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="941b5-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-834">Az.Network</span></span>
* <span data-ttu-id="941b5-835">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="941b5-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="941b5-837">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="941b5-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="941b5-838">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="941b5-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="941b5-839">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="941b5-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="941b5-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-840">Az.Resources</span></span>
* <span data-ttu-id="941b5-841">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="941b5-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="941b5-842">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="941b5-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="941b5-843">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="941b5-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="941b5-844">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="941b5-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-845">Az.Sql</span></span>
* <span data-ttu-id="941b5-846">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="941b5-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="941b5-847">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="941b5-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-848">Az.Websites</span></span>
* <span data-ttu-id="941b5-849">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="941b5-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="941b5-850">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-851">Az.Accounts</span></span>
* <span data-ttu-id="941b5-852">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="941b5-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="941b5-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="941b5-853">Az.AnalysisServices</span></span>
<span data-ttu-id="941b5-854">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="941b5-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-855">Az.Compute</span></span>
* <span data-ttu-id="941b5-856">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="941b5-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="941b5-857">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="941b5-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="941b5-858">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="941b5-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-859">Az.RecoveryServices</span></span>
<span data-ttu-id="941b5-860">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="941b5-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-861">Az.Resources</span></span>
* <span data-ttu-id="941b5-862">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="941b5-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="941b5-863">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="941b5-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="941b5-864">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="941b5-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="941b5-865">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="941b5-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-866">Az.Sql</span></span>
* <span data-ttu-id="941b5-867">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="941b5-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="941b5-868">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="941b5-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="941b5-869">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="941b5-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="941b5-870">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-871">Az.Accounts</span></span>
* <span data-ttu-id="941b5-872">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="941b5-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="941b5-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="941b5-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="941b5-874">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="941b5-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="941b5-876">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="941b5-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="941b5-877">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-878">Az.Accounts</span></span>
* <span data-ttu-id="941b5-879">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="941b5-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="941b5-880">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="941b5-881">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="941b5-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="941b5-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="941b5-882">Az.Aks</span></span>
* <span data-ttu-id="941b5-883">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="941b5-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-884">Az.Automation</span></span>
* <span data-ttu-id="941b5-885">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="941b5-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="941b5-886">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="941b5-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="941b5-887">Az.Cdn</span></span>
* <span data-ttu-id="941b5-888">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-889">Az.Compute</span></span>
* <span data-ttu-id="941b5-890">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="941b5-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="941b5-891">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="941b5-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="941b5-892">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="941b5-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="941b5-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="941b5-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="941b5-894">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="941b5-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="941b5-895">Az.DataFactory</span></span>
* <span data-ttu-id="941b5-896">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="941b5-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-898">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="941b5-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="941b5-899">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="941b5-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="941b5-900">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="941b5-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="941b5-901">Az.IotHub</span></span>
* <span data-ttu-id="941b5-902">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="941b5-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="941b5-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-903">Az.KeyVault</span></span>
* <span data-ttu-id="941b5-904">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-905">Az.Network</span></span>
* <span data-ttu-id="941b5-906">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-907">Az.Resources</span></span>
* <span data-ttu-id="941b5-908">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="941b5-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="941b5-909">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="941b5-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="941b5-910">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="941b5-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="941b5-911">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="941b5-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="941b5-912">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="941b5-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="941b5-913">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="941b5-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="941b5-914">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="941b5-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="941b5-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="941b5-916">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="941b5-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="941b5-917">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="941b5-917">Fix some error messages.</span></span>
* <span data-ttu-id="941b5-918">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="941b5-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="941b5-919">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="941b5-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="941b5-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="941b5-920">Az.SignalR</span></span>
* <span data-ttu-id="941b5-921">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-922">Az.Sql</span></span>
* <span data-ttu-id="941b5-923">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="941b5-924">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="941b5-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="941b5-925">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="941b5-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="941b5-926">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="941b5-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-927">Az.Storage</span></span>
* <span data-ttu-id="941b5-928">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="941b5-929">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="941b5-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="941b5-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="941b5-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="941b5-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="941b5-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="941b5-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="941b5-932">Az.TrafficManager</span></span>
* <span data-ttu-id="941b5-933">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-934">Az.Websites</span></span>
* <span data-ttu-id="941b5-935">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="941b5-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="941b5-936">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="941b5-937">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="941b5-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="941b5-938">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="941b5-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="941b5-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-939">Az.Accounts</span></span>
* <span data-ttu-id="941b5-940">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="941b5-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-941">Az.Compute</span></span>
* <span data-ttu-id="941b5-942">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="941b5-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="941b5-943">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="941b5-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="941b5-944">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-946">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="941b5-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="941b5-947">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="941b5-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="941b5-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="941b5-948">Az.EventGrid</span></span>
* <span data-ttu-id="941b5-949">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="941b5-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="941b5-950">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="941b5-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="941b5-951">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="941b5-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="941b5-952">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="941b5-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="941b5-953">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="941b5-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="941b5-954">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="941b5-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="941b5-955">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="941b5-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="941b5-956">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="941b5-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="941b5-957">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="941b5-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="941b5-958">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="941b5-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="941b5-959">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="941b5-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="941b5-960">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="941b5-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="941b5-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="941b5-961">Az.IotHub</span></span>
* <span data-ttu-id="941b5-962">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="941b5-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="941b5-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="941b5-963">Az.LogicApp</span></span>
* <span data-ttu-id="941b5-964">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="941b5-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-965">Az.Resources</span></span>
* <span data-ttu-id="941b5-966">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="941b5-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="941b5-967">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="941b5-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="941b5-968">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="941b5-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="941b5-969">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="941b5-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="941b5-970">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="941b5-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="941b5-971">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="941b5-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="941b5-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="941b5-972">Az.SignalR</span></span>
* <span data-ttu-id="941b5-973">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-974">Az.Sql</span></span>
* <span data-ttu-id="941b5-975">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="941b5-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="941b5-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-976">Az.Storage</span></span>
* <span data-ttu-id="941b5-977">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="941b5-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="941b5-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="941b5-978">New-AzStorageContext</span></span>
* <span data-ttu-id="941b5-979">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="941b5-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="941b5-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="941b5-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-981">Az.Websites</span></span>
* <span data-ttu-id="941b5-982">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="941b5-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="941b5-983">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="941b5-984">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="941b5-985">Generale</span><span class="sxs-lookup"><span data-stu-id="941b5-985">General</span></span>

- <span data-ttu-id="941b5-986">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="941b5-986">General Availability of Az Module</span></span>
- <span data-ttu-id="941b5-987">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="941b5-987">Online help for each module</span></span>
- <span data-ttu-id="941b5-988">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="941b5-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="941b5-989">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="941b5-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="941b5-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-990">Az.Accounts</span></span>
- <span data-ttu-id="941b5-991">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="941b5-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="941b5-992">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="941b5-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="941b5-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-993">Az.ApiManagement</span></span>
- <span data-ttu-id="941b5-994">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="941b5-994">Fixes for #7002</span></span>
- <span data-ttu-id="941b5-995">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="941b5-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="941b5-996">Az.Batch</span></span>
- <span data-ttu-id="941b5-997">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="941b5-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="941b5-998">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="941b5-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="941b5-999">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="941b5-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="941b5-1000">Az.Billing</span></span>
- <span data-ttu-id="941b5-1001">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="941b5-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="941b5-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="941b5-1003">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="941b5-1004">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="941b5-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="941b5-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="941b5-1006">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="941b5-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="941b5-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="941b5-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="941b5-1008">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="941b5-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="941b5-1010">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="941b5-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="941b5-1011">Az.Monitor</span></span>
- <span data-ttu-id="941b5-1012">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="941b5-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="941b5-1013">Az.KeyVault</span></span>
- <span data-ttu-id="941b5-1014">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="941b5-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="941b5-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="941b5-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="941b5-1016">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="941b5-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="941b5-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="941b5-1017">Az.Media</span></span>
- <span data-ttu-id="941b5-1018">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="941b5-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="941b5-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-1019">Az.Network</span></span>
<span data-ttu-id="941b5-1020">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="941b5-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="941b5-1021">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="941b5-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="941b5-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="941b5-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="941b5-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="941b5-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="941b5-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="941b5-1030">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="941b5-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="941b5-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="941b5-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="941b5-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="941b5-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="941b5-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="941b5-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="941b5-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="941b5-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="941b5-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="941b5-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="941b5-1037">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="941b5-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="941b5-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="941b5-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="941b5-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="941b5-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="941b5-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="941b5-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="941b5-1041">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="941b5-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="941b5-1042">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="941b5-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="941b5-1044">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="941b5-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="941b5-1045">Az.Profile</span></span>
- <span data-ttu-id="941b5-1046">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="941b5-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="941b5-1048">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="941b5-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1049">Az.Resources</span></span>
- <span data-ttu-id="941b5-1050">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="941b5-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="941b5-1052">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="941b5-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="941b5-1053">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="941b5-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="941b5-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="941b5-1055">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="941b5-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="941b5-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-1056">Az.Sql</span></span>
- <span data-ttu-id="941b5-1057">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="941b5-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="941b5-1058">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="941b5-1059">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="941b5-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-1060">Az.Storage</span></span>
- <span data-ttu-id="941b5-1061">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="941b5-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-1062">Az.Websites</span></span>
- <span data-ttu-id="941b5-1063">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="941b5-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="941b5-1064">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="941b5-1065">Generale</span><span class="sxs-lookup"><span data-stu-id="941b5-1065">General</span></span>

* <span data-ttu-id="941b5-1066">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="941b5-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="941b5-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-1067">Az.Compute</span></span>

* <span data-ttu-id="941b5-1068">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="941b5-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="941b5-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="941b5-1070">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="941b5-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="941b5-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="941b5-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="941b5-1072">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="941b5-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="941b5-1073">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="941b5-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="941b5-1074">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="941b5-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="941b5-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="941b5-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="941b5-1076">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="941b5-1077">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="941b5-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="941b5-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1078">Az.Resources</span></span>

* <span data-ttu-id="941b5-1079">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="941b5-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="941b5-1080">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="941b5-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="941b5-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-1081">Az.Sql</span></span>

* <span data-ttu-id="941b5-1082">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="941b5-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="941b5-1083">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="941b5-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="941b5-1084">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="941b5-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="941b5-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-1085">Az.Storage</span></span>

* <span data-ttu-id="941b5-1086">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="941b5-1087">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="941b5-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="941b5-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="941b5-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="941b5-1089">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="941b5-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="941b5-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="941b5-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="941b5-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="941b5-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="941b5-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-1092">Az.Websites</span></span>

* <span data-ttu-id="941b5-1093">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="941b5-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="941b5-1094">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="941b5-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="941b5-1095">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="941b5-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="941b5-1096">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="941b5-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="941b5-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="941b5-1098">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="941b5-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="941b5-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="941b5-1099">Az.Automation</span></span>
* <span data-ttu-id="941b5-1100">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="941b5-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="941b5-1101">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="941b5-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="941b5-1102">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="941b5-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="941b5-1103">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="941b5-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="941b5-1104">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="941b5-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="941b5-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-1105">Az.Compute</span></span>
* <span data-ttu-id="941b5-1106">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="941b5-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="941b5-1107">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="941b5-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="941b5-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="941b5-1109">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="941b5-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="941b5-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="941b5-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="941b5-1111">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="941b5-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="941b5-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-1112">Az.Network</span></span>
* <span data-ttu-id="941b5-1113">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="941b5-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="941b5-1114">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="941b5-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="941b5-1115">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="941b5-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="941b5-1116">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="941b5-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="941b5-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="941b5-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="941b5-1118">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="941b5-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="941b5-1119">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="941b5-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="941b5-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="941b5-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="941b5-1121">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="941b5-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="941b5-1122">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="941b5-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="941b5-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="941b5-1123">Az.Relay</span></span>
* <span data-ttu-id="941b5-1124">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="941b5-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="941b5-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1125">Az.Resources</span></span>
* <span data-ttu-id="941b5-1126">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="941b5-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="941b5-1127">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="941b5-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="941b5-1128">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="941b5-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="941b5-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="941b5-1130">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="941b5-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="941b5-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-1131">Az.Sql</span></span>
* <span data-ttu-id="941b5-1132">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="941b5-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="941b5-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="941b5-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="941b5-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="941b5-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="941b5-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="941b5-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="941b5-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="941b5-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="941b5-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="941b5-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="941b5-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="941b5-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="941b5-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="941b5-1141">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="941b5-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="941b5-1142">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="941b5-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="941b5-1143">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="941b5-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="941b5-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="941b5-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="941b5-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="941b5-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="941b5-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="941b5-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="941b5-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="941b5-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="941b5-1148">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="941b5-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="941b5-1149">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="941b5-1150">Generale</span><span class="sxs-lookup"><span data-stu-id="941b5-1150">General</span></span>
* <span data-ttu-id="941b5-1151">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="941b5-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="941b5-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="941b5-1152">Az.Profile</span></span>
* <span data-ttu-id="941b5-1153">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="941b5-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="941b5-1154">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="941b5-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="941b5-1155">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="941b5-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="941b5-1156">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="941b5-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="941b5-1157">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="941b5-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="941b5-1158">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="941b5-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="941b5-1159">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="941b5-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-1161">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="941b5-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-1162">Az.Compute</span></span>
* <span data-ttu-id="941b5-1163">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="941b5-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="941b5-1164">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="941b5-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="941b5-1165">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="941b5-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-1167">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="941b5-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="941b5-1168">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="941b5-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="941b5-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="941b5-1169">Az.Insights</span></span>
* <span data-ttu-id="941b5-1170">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="941b5-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="941b5-1171">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="941b5-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="941b5-1172">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="941b5-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="941b5-1173">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="941b5-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-1174">Az.Network</span></span>
* <span data-ttu-id="941b5-1175">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="941b5-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="941b5-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="941b5-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="941b5-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="941b5-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="941b5-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="941b5-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="941b5-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="941b5-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="941b5-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="941b5-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="941b5-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="941b5-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="941b5-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="941b5-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="941b5-1183">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="941b5-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1184">Az.Resources</span></span>
* <span data-ttu-id="941b5-1185">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="941b5-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="941b5-1186">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="941b5-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="941b5-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="941b5-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="941b5-1188">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="941b5-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="941b5-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="941b5-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="941b5-1190">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="941b5-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="941b5-1191">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="941b5-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="941b5-1192">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="941b5-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="941b5-1193">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="941b5-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="941b5-1194">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="941b5-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="941b5-1195">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="941b5-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="941b5-1196">Az.Profile</span></span>
* <span data-ttu-id="941b5-1197">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="941b5-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="941b5-1198">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="941b5-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-1199">Az.Compute</span></span>
* <span data-ttu-id="941b5-1200">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="941b5-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="941b5-1201">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941b5-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="941b5-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="941b5-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="941b5-1203">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="941b5-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="941b5-1204">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="941b5-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="941b5-1205">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="941b5-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="941b5-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="941b5-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="941b5-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="941b5-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-1208">Az.Network</span></span>
* <span data-ttu-id="941b5-1209">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="941b5-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="941b5-1210">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941b5-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1211">Az.Resources</span></span>
* <span data-ttu-id="941b5-1212">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="941b5-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="941b5-1213">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="941b5-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="941b5-1214">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="941b5-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="941b5-1215">Azure.Storage</span></span>
* <span data-ttu-id="941b5-1216">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="941b5-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="941b5-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="941b5-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="941b5-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="941b5-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="941b5-1219">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="941b5-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="941b5-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="941b5-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="941b5-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="941b5-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="941b5-1222">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="941b5-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="941b5-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="941b5-1223">Az.Compute</span></span>
* <span data-ttu-id="941b5-1224">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="941b5-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="941b5-1225">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="941b5-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="941b5-1226">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="941b5-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="941b5-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="941b5-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="941b5-1228">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="941b5-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="941b5-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="941b5-1229">Az.Network</span></span>
* <span data-ttu-id="941b5-1230">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="941b5-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="941b5-1231">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="941b5-1231">new cmdlets added</span></span>
    - <span data-ttu-id="941b5-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="941b5-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="941b5-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="941b5-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="941b5-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="941b5-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="941b5-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="941b5-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="941b5-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="941b5-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="941b5-1238">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="941b5-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="941b5-1239">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="941b5-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="941b5-1240">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="941b5-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="941b5-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="941b5-1241">Az.RedisCache</span></span>
* <span data-ttu-id="941b5-1242">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="941b5-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="941b5-1243">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="941b5-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="941b5-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="941b5-1244">Az.Resources</span></span>
* <span data-ttu-id="941b5-1245">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="941b5-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="941b5-1246">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="941b5-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="941b5-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="941b5-1247">Az.Sql</span></span>
* <span data-ttu-id="941b5-1248">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="941b5-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="941b5-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="941b5-1249">Az.Websites</span></span>
* <span data-ttu-id="941b5-1250">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="941b5-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="941b5-1251">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="941b5-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="941b5-1252">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="941b5-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="941b5-1253">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="941b5-1253">Initial Release</span></span>